# MyBot Community Plugins Directory

Welcome to the official open-source plugins catalog for **MyBot Studio** — the self-hosted, visual no-code Telegram bot engine.

This repository serves as the central directory where creators, developers, and the community submit, discover, and maintain modular extensions for MyBot.

---

## 🧩 How It Works

Plugins in MyBot extend the visual studio canvas with custom nodes, admin panels, payment gateways, analytics tools, and external API connectors.

Every plugin is a self-contained directory containing:
1. `plugin.json` — metadata (name, version, author, description, category, inputs, outputs, UI hooks).
2. Backend handlers (Python / FastAPI router / DAG node execution logic).
3. Frontend components (React canvas node or dashboard extension, optional).

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

## 🤝 Contribution & Maintenance Rules

We welcome community contributions. To keep the ecosystem reliable and transparent:

1. **Pull Request Submissions**:
   - To add a plugin, create a new folder under `plugins/<your-plugin-id>/` and submit a Pull Request.
   - Please include clear documentation, valid configuration schema, and test coverage.

2. **Open Source & Non-Commercial**:
   - All plugins hosted in this repository are **free and open-source** under the GNU AGPL-3.0 (or compatible OSI) license.
   - Commercial / paid / proprietary plugins are **not accepted** in this public index. Authors wishing to distribute commercial extensions or monetize custom software should host their own services, platforms, or websites.

3. **Community Maintenance**:
   - Submitting a plugin here grants the community permission to maintain, bug-fix, and keep it updated with newer MyBot engine versions if the original author becomes inactive.
   - The core MyBot team does not endorse, guarantee, or take legal liability for third-party external services, advertisements, APIs, or content delivered through third-party community plugins.

4. **Security & Quality Standards**:
   - No obfuscated, encrypted, or remote-executable bytecode.
   - No telemetry, unauthorized data scraping, token exfiltration, or backdoors. Every PR is subject to automated security analysis and code review.

---

## 📦 How to Install a Plugin in MyBot Studio

From your MyBot dashboard:
1. Navigate to **Plugins** in the sidebar.
2. Search for the plugin title or paste its GitHub repository / folder link.
3. Click **Install / Activate**. The node will instantly appear on your canvas.

---

## 📄 License

This repository and its included extensions are licensed under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [LICENSE](LICENSE) for details.
