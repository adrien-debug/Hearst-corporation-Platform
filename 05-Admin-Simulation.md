# PAGE 5 - ADMIN / SIMULATION

## CONTEXT
- Name: Simulation
- URL: `/admin/simulation`
- Access: Admin, per tenant
- Purpose: List, create, review and export mining project simulations

## WIREFRAME
```
+---------------------------------------------------------------+
| TOPBAR | SIDEBAR | [Simulation tab active]                   |
+---------------------------------------------------------------+
| [Simulation Table]  [Create simulation]                       |
| | ID | Prospect | Coin | Creator | Date | Actions (pdf/...)  |
| | ... | ...     | ...  | ...     | ...  | View/Download     |
|  [Search/filter][Pagination][Export]                          |
+---------------------------------------------------------------+
| When row clicked: Details modal, timeline, pdf, delete        |
+---------------------------------------------------------------+
| SUPPORT | FOOTER                                              |
+---------------------------------------------------------------+
```

## UX/LOGIC
- Table: filters by coin/prospect/date/creator, sortable, page selectors
- Create: modal, fields validated live, loading, disables on save
- Row: View details = full summary+download/export
- Export: All as CSV, single as PDF (actions menu)
- Empty/loading/error: full skeleton/table/alert as needed
- Modal = focus trap, escape close

## API
- /api/tenant/{tid}/simulations (GET/POST/...)

---
To be paired with 05-Admin-Simulation.schema.json




