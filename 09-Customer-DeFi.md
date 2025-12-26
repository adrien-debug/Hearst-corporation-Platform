# PAGE 9 - CUSTOMER VIEW / DEFI DASHBOARD

## CONTEXT
- Name: Customer DeFi
- URL: `/admin/customer-view/:id/defi`
- Role: Client/User
- Purpose: DeFi collateral and lending protocol overview

## WIREFRAME
```
+----------------------------------------------------------+
| NAVBAR | PROFILE | SUPPORT (DeFi active)                |
+----------------------------------------------------------+
| [Wallet Card] [Copy] [QR]                               |
| [ETH: 0xabc... (full, tooltip, copy, qr-modal)]         |
|---------------------------------------------------------|
| [3 KPIs]: BTC Collateral | USD Borrowed | LTV (%)       |
|---------------------------------------------------------|
| Tabs: Morpho | Compound | ...                           |
| [Active tab]: supplied, borrowed, value, health factor  |
| [Warning/Alert if undercollateralized or error]         |
| [Actions: Repay, Add Collateral if exposed]             |
| [Positions table/details]                               |
|---------------------------------------------------------|
| [Support Floating]                                      |
+---------------------------------------------------------+
```

## UX/LOGIC
- ETH address : copy/QR, tooltip, linked state
- KPIs: tooltips, color-coded
- Tab per protocol, dynamic per config
- Actions contextual (enable/disable from backend/protocol state)
- Error, loading, empty state managed per section
- Accessibility ARIA labels, mobile stacking, all content focusable
- Data fetch: /defi/overview, /defi/protocols/{id}

---
To be paired with 09-Customer-DeFi.schema.json

