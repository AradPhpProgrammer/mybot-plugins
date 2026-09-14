# MyBot Community Plugins Directory

Welcome to the official open-source plugins catalog for **MyBot Studio** — the self-hosted, visual no-code Telegram bot engine.

This repository is a central index where creators, developers, and the community publish, discover, and maintain modular extensions for MyBot.

> 🌐 **Languages:** [English](README.en.md) · [فارسی](README.fa.md) · [Русский](README.ru.md) · [العربية](README.ar.md)

---

## 🧩 How It Works

Plugins extend the visual MyBot studio canvas with **custom nodes**, admin panels, payment gateways, analytics tools, and external API connectors.

A plugin is a self-contained folder containing:
1. `plugin.json` — metadata (name, version, author, description, category, inputs/outputs, UI hooks).
2. Backend handlers (FastAPI router / DAG node execution logic).
3. Frontend components (React canvas node or dashboard extension).

```
plugins/
├── my-awesome-plugin/
│   ├── plugin.json
│   ├── __init__.py
│   ├── node.py
│   └── README.md
```

### Manifest Example (`plugin.json`)

```json
{
  "id": "my_weather_node",
  "name": "Live Weather Provider",
  "version": "1.0.0",
  "author": "YourName",
  "category": "services",
  "description": "Fetches real-time weather forecasts based on user location.",
  "type": "canvas_node",
  "entrypoint": "node.py",
  "license": "AGPL-3.0"
}
```

---

## 📁 Folder Structure

Plugins are organized by category (see `categories.json` as the single source of truth):

| Folder | Category | Examples |
|---|---|---|
| `plugins/payments/` | Payment gateways & crypto | ZarinPal, TRON, wallet connectors |
| `plugins/analytics/` | Analytics, tracking & dashboards | user counters, event logs |
| `plugins/services/` | External services & APIs | AI, weather, webhooks |
| `plugins/admin/` | Admin, anti-spam & moderation | user bans, channel subscriptions, admin alerts |
| `plugins/messengers/` | Messengers & tickets | live support, cross-platform bridges |
| `plugins/community/` | Games & utilities | calculators, fun nodes |

---

## 🤝 Contribution & Maintenance Rules

To keep the ecosystem reliable and transparent:

1. **Pull Request Submissions**: to add a plugin, create a folder under `plugins/<plugin-id>/` and submit a PR with clear documentation, a valid configuration schema, and tests.

2. **Open Source & Non-Commercial**: all plugins hosted here are **free and open-source** under GNU AGPL-3.0 (or a compatible OSI license). **Commercial, paid, or proprietary** plugins are **not accepted** in this public index. Authors who wish to distribute commercial extensions or monetize their work must run their own service, platform, or website.

3. **Community Maintenance**: submitting a plugin grants the community permission to bug-fix, preserve, and update it against newer MyBot engine versions if the original author becomes inactive. The core MyBot team does not endorse, guarantee, or take legal liability for third-party services, advertisements, APIs, or content delivered through community plugins.

4. **Security & Quality Standards**:
   - No obfuscated, encrypted, or remote-executable bytecode (beyond permitted server-side APIs).
   - No telemetry, unauthorized data scraping, token exfiltration, or backdoors. Every PR is reviewed by automated security analysis and code review.

---

## 📦 Installing a Plugin in MyBot Studio

From your MyBot dashboard:
1. Go to **Plugins** in the sidebar.
2. Search for the plugin title or paste its GitHub repository / folder link.
3. Click **Install / Activate**. The node appears instantly on your canvas.

---

## 📄 License

This repository and its extensions are licensed under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [LICENSE](LICENSE).