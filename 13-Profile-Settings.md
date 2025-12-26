# PAGE 13 - PROFILE & SETTINGS

## CONTEXT
- Name: Profile / Settings
- Presence: accesible nav+dropdown+dedicated page
- Role: Any logged user, admin or customer
- Purpose: See & manage personal and org info, change password, preferences

## WIREFRAME
```
+-------------------------------+
| Avatar [edit photo]           |
+-------------------------------+
| Name:  [__________]           |
| Email: [readonly]             |
| Langue [dropdown]             |
+-------------------------------+
| [Modifier le mot de passe]    |
| [Notifications settings]      |
| [Logout]                      |
+-------------------------------+
```

## UX/LOGIC
- Editable fields: nom/prénom (auto-save/live), langue
- Email = always readonly; badge if unverified
- Change password = modal: old, new, confirm, rules
- Notifications: toggles, push/email/sms, preferences from API
- Logout: bouton avec pop confirm, focus management pour clavier
- API calls async, disables submit during loading
- All modals ARIA/focus trap, escape/enter shortcuts
- Loading/error/success for every action

## API
- /api/account (GET/PUT)
- /api/account/password
- /api/account/lang

---
To be paired with 13-Profile-Settings.schema.json

