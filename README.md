# 🚢 Portainer Templates Repository

![Build Status](https://github.com/OnyxJeff/portainer_templates/actions/workflows/validate-compose.yml/badge.svg)
![Maintenance](https://img.shields.io/maintenance/yes/2025.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![GitHub release](https://img.shields.io/github/v/release/OnyxJeff/portainer_templates)
![Issues](https://img.shields.io/github/issues/OnyxJeff/portainer_templates)

Welcome to **portainer_templates** — the single source of truth for all my Docker stack templates, optimized for deployment via Portainer.

## Why?

Instead of hunting for random YAML files scattered across the internet, this repo bundles all my curated, tested, and version-controlled Portainer stacks in one place. Deploy anything from lightweight services to complex multi-container apps with a single click.

## 📁 File Structure
```text
portainer_templates/
├── .github/workflows/     # CI for YAML validation
├── darr/                  # YAML for -darr-stack container
├── gitea/                 # YAML for gitea container
├── netbootxyz/            # YAML for netboot-xyz container
├── nginxproxymanager/     # YAML for nginx-proxy-manager container
└── README.md              # You're reading it!
```
---

## 📦 Included Templates

| Stack Name | Description                          | Notes                     |
|------------|------------------------------------|---------------------------|
| **Gitea**  | Self-hosted Git service with MariaDB backend | Port override on 5123, ready for NGINX Proxy Manager |
| **-darr-stack** | A full-featured media automation stack designed for Portainer | Normal port-forwarding and functional |
| **netboot-xyz** | A portable PXE boot service containerized for Portainer | Some setup in your router is required to load environment on your network |
| **nginx-proxy-manager** | An easy-to-use NGINX reverse proxy container with a full web UI for managing domains, SSL certs, and routing | Make sure to make a DNS record for this on your DHCP server and setup additional records as needed |

*More stacks coming soon!*

---

## 🚀 Deployment

1. Clone this repo:
   ```bash
   git clone https://github.com/OnyxJeff/portainer_templates.git
   cd portainer_templates
   ```
2. Browse any stack folder (e.g., /gitea/)
3. Copy the contents of the corresponding .yml file into Portainer’s Stacks > Add Stack UI
4. Create or update .env files as needed (check each stack’s README)
5. Deploy and enjoy!

---

## 📜 License
MIT — Use it, fork it, build something rad with it.

📬 Maintained By
Jeff M. • [@OnyxJeff](https://www.github.com/onyxjeff)