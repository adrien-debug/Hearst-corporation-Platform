# PAGE 6 - ADMIN / TOOLS

## CONTEXT
- Name: Admin Tools
- URL: `/admin/tools`
- Access: Admin, tenant
- Purpose: Entry point for admin automation tools: monitoring, electricity, marketing AI...

## WIREFRAME
```
+--------------------------------------------------------+
| TOPBAR | PROFILE | LOGOUT                              |
|--------------------------------------------------------|
| SIDEBAR [Tools Active]                                 |
|--------------------------------------------------------|
| [Tools flex grid: Card per tool]                       |
|  [Monitoring Dashboard] [Launch] [Description]          |
|  [Electricity Web App ] [Launch] [Description]          |
|  [Marketing AI      ] [Launch] [Description]            |
| ...                                                    |
+--------------------------------------------------------+
| SUPPORT | FOOTER                                       |
+--------------------------------------------------------+
```

## UX/LOGIC
- All tools as cards: icon, description, Launch button
- Launch: opens in-page, modal ou nouvelle page (selon outil)
- Aria-label, Tooltip, info popin par action
- Accessible, mobile grid layout, responsive stacking
- Loading transitions, spinner appearing on tool load
- Permissions: tools visibility/context filtered by admin rights

## API
- Appelle chaque tool via endpoint ou lien sécurisé

---
To be paired with 06-Admin-Tools.schema.json




