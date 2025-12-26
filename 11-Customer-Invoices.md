# PAGE 11 - CUSTOMER VIEW / INVOICES

## CONTEXT
- Name: Customer Invoices
- URL: `/admin/customer-view/:id/invoices`
- Role: Client/User
- Purpose: List, search, filter and export all invoicing history

## WIREFRAME
```
+-------------------------------------------------------------+
| NAVBAR [Invoices active] | PROFILE | SUPPORT               |
+-------------------------------------------------------------+
| [Filters: Status, Date range, Search #, Export CSV]         |
+-------------------------------------------------------------+
| [Invoices table]                                            |
| Number | Type | Date | Total | Status | Actions (PDF)       |
| INV-001 | ... | ...  | ...   | Paid   | [Download][View]    |
| ...     | ... | ...  | ...   | ...    | ...                 |
| Pagination | PerPage | ...                                 |
+-------------------------------------------------------------+
| SUPPORT FLOATING BUTTON                                     |
+-------------------------------------------------------------+
```

## UX/LOGIC
- All columns filterable/sortable. By default sort = newest first
- Export CSV (filters applied), Download PDF (single), View inline
- If no invoices found, empty state w/ help or doc
- Status: Paid/Pending/Overdue badge, color-coded for a11y
- Mobile/tablette support: table horizontal scroll, filters stacked
- Loading: skeletons, error: sticky + retry
- All actions have tooltips/aria

## API
- /api/customer/:id/invoices
- /api/customer/:id/invoices/download

---
To be paired with 11-Customer-Invoices.schema.json

