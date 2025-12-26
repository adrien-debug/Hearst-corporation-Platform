# PAGE 4 - ADMIN / OPPORTUNITIES

## CONTEXT
- Name: Admin Opportunities
- URL: `/admin/opportunities`
- Access: Admin / tenant context
- Purpose: Manage hosting business offers and hardware inventories

## WIREFRAME
```
+--------------------------------------------------------+
| TOPBAR | SIDEBAR | [Opportunities tab active]          |
+--------------------------------------------------------+
| Tabs: Hosting Opportunities | Hardware Devices         |
+--------------------------------------------------------+
| Table: Hosting Opportunities                          |
| | Name | Supplier | Country | $/kWh | Priority | ...  |
| | ... | ...      | ...     | ...   | [View/Edit/Del] |
|  [Add new] [Search] [Filter] [Pagination]              |
+--------------------------------------------------------+
| Table: Hardware Devices                                |
| | Device | Coin | Hashrate | Power | [Edit/Del]      |
| | ...   | ...  | ...      | ...   | ...              |
|  [Add device] [Search/Filter] [Pagination]             |
+--------------------------------------------------------+
| SUPPORT | FOOTER                                       |
+--------------------------------------------------------+
```

## UX/LOGIC
- Tabs switch context (tab index in URL/query)
- Tables: full CRUD ops, batch select, column sort, instant filter
- Add/Edit: form modal, required = name, price, supplier, hardware model...
- Filters: by country, by price, by type
- Empty: "No items yet, add..." 
- Errors: sticky, inline, alerts
- Loading: skeletons
- Multi-tenant: all offers/devices are scoped
- Responsive: horizontal scroll on mobile, table stacking

## API
- /api/tenant/{id}/opportunities (GET/POST/DEL/...)
- /api/tenant/{id}/devices

---
To be paired with 04-Admin-Opportunities.schema.json




