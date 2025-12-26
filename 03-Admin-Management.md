# PAGE 3 - ADMIN / MANAGEMENT

## CONTEXT
- Name: Admin Management
- URL: `/admin/management`
- Access: Admin, by tenant context
- Purpose: Full management of client, prospects, affiliates, suppliers, whitelabels and sub-accounts.

## WIREFRAME
```
+-----------------------------------------------------------+
|   TOPBAR: Logo | Profile | Logout                        |
|-----------------------------------------------------------|
| SIDEBAR: [Management active]                             |
|-----------------------------------------------------------|
| Tabs: Clients | Prospects | Affiliates | Sub-Accounts      |
|       Suppliers | Contracts | Whitelabels                 |
|-----------------------------------------------------------|
| Active tab table/list view; Add button; search; filters   |
| (each resource = one view, always same controls UX)        |
+-----------------------------------------------------------+
|  Table example: Clients                                   |
|  | Name | Email | Company | Username | Actions (CRUD)      |
|  [Add client]  [Search...]  [Pagination selector]         |
|-----------------------------------------------------------|
+-----------------------------------------------------------+
```

## UX/LOGIC
- Tab strip at top; switch table/data context (state in URL)
- Table: batch select, mass action, real-time filter/search, column sorting
- Add/Edit opens form modal (focus 1st field, tab navigation)
- Prospects: pipeline/kanban optional   
- Empty: “No [type] yet. Add your first…”
- Loading: skeleton, spinner in add modal
- Error: top sticky retryable alerts; per-field inline if validation fails
- Bulk actions possible

## ACCESSIBILITY/RESPONSIVE
- Table scroll, tap for action on mobile
- Modals: focus trap, escape to close 
- ARIA labels for all buttons, tabs, etc.

## API
- /api/tenant/{tid}/clients | /prospects | /affiliates | /suppliers ... (GET/POST/PUT/DEL)

---
To be paired with 03-Admin-Management.schema.json




