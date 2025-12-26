# PAGE 10 - CUSTOMER VIEW / CONTRACTS

## CONTEXT
- Name: Customer Contracts
- URL: `/admin/customer-view/:id/contracts`
- Role: Client/User
- Purpose: List and manage contract entries, see distribution, export, drilldown

## WIREFRAME
```
+------------------------------------------------------------------+
| NAVBAR [Contracts active] | PROFILE | SUPPORT                   |
+------------------------------------------------------------------+
| Filters: contract, machine, country, crypto, status, daterange   |
|------------------------------------------------------------------|
| Contracts table                                                  |
| Name | Status | Coin | Model | N. Machines | Cost | ... Actions  |
| ...  | ...    | ...  | ...   | ...         | ...  | ...         |
| Export CSV/PDF  | Pagination | Search                              |
|------------------------------------------------------------------|
| Distribution widget: Pie country/machine, legend, click drilldown |
|------------------------------------------------------------------|
| Modal full contract details: kpis, timeline, breakdown           |
+------------------------------------------------------------------+
```

## UX/LOGIC
- Filters (all types), search, sort, export
- Table: columns moveable, sticky, scrollable
- Distribution: clickable legend, show #/country etc.
- Details modal: open on click, stats, timeline, downloadable info
- Empty state: “No contracts yet. Admin must create.”
- Responsive/mobile: table scrolls horizontally, pie below on dx <600px
- Error/loading/success: explicit, all a11y

## API
- /api/customer/:id/contracts (GET/POST/EXPORT)

---
To be paired with 10-Customer-Contracts.schema.json

