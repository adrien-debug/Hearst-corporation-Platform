# PAGE 1 - LOGIN / AUTHENTIFICATION

## CONTEXTE
- Nom : Login
- URL : `/login`
- Accès : Public, multi-tenant-ready
- Rôles : admin, client, superadmin... (avant identification)

## WIREFRAME (ASCII)
```
+-----------------------------+
|       LOGO HEARST/tenant    |
|     Connexion / Bienvenue   |
|  [ Email___________ ]       |
|  [ Mot de passe___👁️]     |
|  [x] Se souvenir de moi     |
|  [ Se connecter ⏳  ]       |
| Mot de passe oublié ?       |
| S’inscrire                  |
+-----------------------------+
[Select tenant, si multi-org] |
+-----------------------------+
Footer : RGPD, langue, support|
+-----------------------------+
```

## UX/FONCTION RÈGLES
- Valid email live, password min 8 chars + force-meter
- Eye toggle, tooltip, autofill géré secure
- Loading: spinner, disables
- ErrorBox detail: mauvais pass, lockout, mauvais tenant
- Redirection contextuelle
- Accessibilité parfaite (labels, ARIA)
- Responsive mobile/tablette
- Multi-tenant : logo, wording, liens dynamiques

## MICROCOPY (Exemples)
- "Saisissez votre email et mot de passe"
- "Mot de passe oublié ?"
- "Champs obligatoires"
- "Identifiants invalides"
- "Connexion en cours…"

## ÉTATS
- idle / filling / loading / error / success / maintenance

## TRACKING/LOG
- login_attempt, login_success, login_error, tenant_switch

## API /
- POST /auth/login (payload: email, password, tenantId)

---
À associer au json schema 01-Login.schema.json




