# Prompt Builder for Manager.io Extensions

> **Build custom Manager.io extensions in minutes — no API knowledge required.**
> Explore any endpoint, inspect its schema, and generate a complete AI prompt that produces a ready-to-install extension.

![Version](https://img.shields.io/badge/version-1.0-blue)
![Platform](https://img.shields.io/badge/platform-Manager.io-orange)
![Type](https://img.shields.io/badge/type-Single%20HTML%20File-brightgreen)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## What It Does

A single-file extension that runs inside Manager.io. It turns the Manager.io API into something anyone can work with — explore endpoints visually, pick the fields you need, and get a structured AI prompt that Claude, ChatGPT, or Gemini can turn into a working `.html` extension.

**Workflow**

1. **Load** any `/api4/` endpoint — one click or typed
2. **Inspect** the live JSON — every field, type, and sample value
3. **Select** the fields you need from the sidebar
4. **Generate** a complete AI prompt via the built-in Builder
5. **Paste** into your AI → receive a working extension → install it back

---

## Features

| | Feature | Description |
|---|---|---|
| 🔍 | **API Explorer** | Browse any `/api4/` endpoint with JSON syntax highlighting |
| ⚡ | **Quick Endpoints** | One-click shortcuts for all common list and report endpoints |
| ⬇ | **Load All** | Follows pagination tokens automatically — no 50-record limit |
| 🗂 | **Schema Inspector** | Every field path, data type, and sample value in a clean sidebar |
| 📋 | **Context Buffer** | Combine multiple endpoints into a single prompt |
| 🤖 | **AI Builder** | 5-step wizard that outputs a complete copy-paste prompt |
| 🟢 | **Live Connection Check** | Confirms it's actually connected to Manager.io |
| 🔒 | **Security Layer** | Origin-pinned postMessage, CSP, XSS-safe rendering, GET-only |

---

## Quick Start

**1. Install**

Manager.io → **Settings → Extensions → Add New Extension** → paste URL:

```
https://ksl1816.github.io/manager-extension-toolkit/
```

**2. Use it**

Click any quick endpoint → inspect the schema → tick the fields you want → click the floating **⎘ AI Context Buffer** button → switch to the **AI Builder** tab → fill in the 5 steps → **⚡ Generate**.

Copy the output, paste it into Claude / ChatGPT / Gemini, save the returned HTML, and install it back into Manager.io.

> 📖 Click **"How to Use"** inside the extension for the full built-in guide.

---

## Supported Endpoints

**Lists:** `customer-batch` · `supplier-batch` · `sales-invoice-batch` · `purchase-invoice-batch` · `receipt-batch` · `payment-batch` · `inventory-item-batch` · `employee-batch` · `bank-or-cash-account-batch` · `journal-entry-batch` · `sales-quote-batch` · `sales-order-batch` · `purchase-order-batch` · `expense-claim-batch`

**Reports:** `aged-receivables-batch` · `aged-payables-batch` · `trial-balance-batch` · `profit-and-loss-statement-batch` · `balance-sheet-batch` · `general-ledger-transactions-batch`

**Meta:** `businesses`

Any other valid `/api4/` endpoint can be typed manually.

---

## Security

All API calls go through Manager.io's `postMessage` bridge. Active runtime protections:

- **Origin-pinned postMessage** — host origin locked after the first response; spoofed messages are dropped
- **Read-only access** — GET requests only, nothing can be modified in Manager.io
- **Endpoint validation** — blocks `javascript:`, `data:`, and other dangerous schemes before any call is made
- **Strict CSP** — no outbound network calls except Google Fonts (style only)
- **XSS-safe rendering** — all JSON values HTML-escaped before DOM insertion
- **Zero tracking** — no analytics, cookies, or telemetry

Click the **🔒 Secure** badge in the top bar to inspect the active layer live.

---

## Technical Notes

- **Zero dependencies** — pure HTML, CSS, vanilla JavaScript
- **Single file** — works as static hosting anywhere (GitHub Pages, Netlify, Vercel)
- **AI-agnostic** — the generated prompt works with any LLM
- **Responsive** — sidebar collapses on small screens

---

## Custom Development

This tool is **free forever**. If you'd rather have a production-ready extension designed, built, and tested for your specific workflow, custom development is available.

**→ [ksl1816.github.io/ksl-solution-site](https://ksl1816.github.io/ksl-solution-site/)**

---

## License

MIT — free to use, modify, and distribute.

---

## Author

**ksl1816** — [github.com/ksl1816](https://github.com/ksl1816)

*Contributions, bug reports, and feature suggestions welcome.*
