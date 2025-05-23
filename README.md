# 🚢 Portainer Templates Repository

![Build Status](https://github.com/OnyxJeff/portainer_templates/actions/workflows/validate-compose.yml/badge.svg)
![Maintenance](https://img.shields.io/maintenance/yes/2025.svg)
![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)
![GitHub release](https://img.shields.io/github/v/release/OnyxJeff/portainer_templates)

Welcome to **portainer_templates** — the single source of truth for all my Docker stack templates, optimized for deployment via Portainer.

## Why?

Instead of hunting for random YAML files scattered across the internet, this repo bundles all my curated, tested, and version-controlled Portainer stacks in one place. Deploy anything from lightweight services to complex multi-container apps with a single click.

---

## 📦 Included Templates

| Stack Name | Description                          | Notes                     |
|------------|------------------------------------|---------------------------|
| **Gitea**  | Self-hosted Git service with MariaDB backend | Port override on 5123, ready for NGINX Proxy Manager |

*More stacks coming soon!*

---

## 🚀 Quickstart

1. Clone this repo:
   ```bash
   git clone https://github.com/OnyxJeff/portainer_templates.git
   cd portainer_templates

2. Browse any stack folder (e.g., /gitea/)

3. Copy the gitea-stack.yml contents into Portainer’s Stacks > Add Stack UI

4. Create or update .env files as needed (check each stack’s README)

5. Deploy and enjoy!

## 📜 License
MIT — Use it, fork it, build something rad with it.

📬 Maintained By
Jeff M. • [@OnyxJeff](https://www.github.com/onyxjeff)