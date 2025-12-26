# PAGE 12 - SUPPORT (GLOBAL COMPONENT)

## CONTEXT
- Name: Support
- Presence: All pages, fixed/floating bottom-right
- Role: All authenticated users (admin & customer)
- Purpose: Contact support, raise tickets, FAQ access

## WIREFRAME
```
[Support floating button - headset icon] (bottom right)
  |
  v
+-------------------------------+
|   Besoin d'aide ?             |
|   [TextArea : votre question] |
|   [Email : auto-filled, ro]   |
|   [Envoyer]   [Annuler]       |
|   FAQ - lien                  |
+-------------------------------+
```

## UX/LOGIC
- Floating: appears everywhere (tab-index=high)
- Click opens modale, focus point direct sur textarea
- Email pré-rempli, read-only si loggé, editable sinon
- Send: disables btn, loader, affiche toast succès ou sticky erreur
- FAQ: lien (ouvrir nouvel onglet ou page)
- Escape ferme, click extérieur ferme si pas loading
- ARIA/focus trap totale, confirmation sonore/visuelle
- Track each event (sent, failed, opened, faq)

## API
- POST /support/ticket
- POST /support/message

---
To be paired with 12-Support-Component.schema.json

