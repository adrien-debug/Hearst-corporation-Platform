# PAGE 2 - ADMIN / OPERATIONS DASHBOARD

## CONTEXT
- Name: Admin Operations
- URL: `/admin/operation`
- Access: Admins, tenant specific
- Main objective: Global mining/business overview & first entry after login

## WIREFRAME (ASCII/SKETCH)
```
+-------------------------------------------------------------+
|        HEADER: Logo | Profile | Logout                      |
|-------------------------------------------------------------|
| SIDEBAR: [Operations] [Management] [Opportunities] ...      |
|           (Operations HIGHLIGHTED)                          |
|-------------------------------------------------------------|
|    KPIs:  [Total Investments] / [BTC Hashrate] / [Kaspa]    |
|-------------------------------------------------------------|
| [Customers Table]        [Add][Search] [Pagination]         |
| | Name | Company | $ | Actions (View/Edit/Delete) |         |
|-------------------------------------------------------------|
| [Contracts Table]        [Search][ExportCSV][Pagination]     |
| | Name | User | Coin | Machines | Power | $...| Actions |   |
|-------------------------------------------------------------|
| [Pie : Miner by Brand]   [Pie: Miner by Country]             |
+-------------------------------------------------------------+
| SUPPORT      FOOTER                                         |
+-------------------------------------------------------------+
```

## UX / STATES
- Header: tenant logo, profile actions, switch tenant
- KPI cards: color + trend, info tooltip, real-time refresh (polling)
- Customers table: batch select, mass delete, column sort, search debounce
- Contracts: multi-columns, filter/sort/CSV, scrollable, responsive sticky head
- Pie charts: auto-update, legend clickable, tooltips, a11y compliant
- Loading: skeletons for all grids/graphs
- Error: sticky retryable alerts
- Support widget always present
- Multi-tenant: all data per current tenant only

## ACCESSIBILITY
- Keyboard navigation (tab/index/cell-select)
- ARIA roles for all widgets
- Responsive: cards/tables/graphs stack, mobile scroll

## STATES
- idle, loading, error, data-empty, batch-mode (customers/contracts)

## COPY - Tooltips/Alerts
- "Export as CSV"
- "No data for selected period"
- "Customer deleted"
- "Actions require confirmation"

## API
- GET `/api/tenants/{tid}/customers`
- GET `/api/tenants/{tid}/contracts`  
- GET `/api/miners/stats`  
- POST/PUT/DELETE as needed

---
To be paired with 02-Admin-Operations.schema.json




