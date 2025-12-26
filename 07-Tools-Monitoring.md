# PAGE 7 - TOOLS DETAIL : MONITORING DASHBOARD

## CONTEXT
- Name: Monitoring Dashboard
- URL: `/admin/tools/monitoring`
- Access: Admin panel 
- Purpose: Real-time mining ops view: active workers, contracts, earnings, alerts

## WIREFRAME
```
+--------------------------------------------------------------+
| HEADER (retour Tools) + User profile                         |
|--------------------------------------------------------------|
| [Monitoring Dashboard - Title]                               |
|--------------------------------------------------------------|
| [KPI Cards: Workers | Active contracts | Earnings]           |
|--------------------------------------------------------------|
| [Realtime Table] | Worker | Uptime | Status | Error |        |
|--------------------------------------------------------------|
| [Line Graph: Earnings/Hashrate over time]                    |
| (toggle Y axis/data)                                         |
|--------------------------------------------------------------|
| [Filters: pool, farm, client, dates] [Clear all]             |
|--------------------------------------------------------------|
| ALERTS: warnings/errors in a list or highlighted badge        |
+--------------------------------------------------------------+
```

## UX/LOGIC
- KPI refresh schedule (e.g. every 20s by default)
- Table auto-updates, highlights row if new event/status detected
- Graph: switch variable, zoom/pan, tooltip hover details
- Filters: combine, always resettable
- Alerts sticky or top popper; error = "Lost connection, retry"
- Accessibility: ARIA table/grid, live region KPIs
- Responsive: grid cards stack, table/graph scroll
- Multi-tenant: filtered data per context; role gate

## API
- /api/tools/monitoring/overview?tenant={}
- /api/tools/monitoring/workers?filter=...
---
To be paired with 07-Tools-Monitoring.schema.json




