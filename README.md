# 🚢 Portainer Host Repository

![Build Status](https://github.com/OnyxJeff/docker-compose_templates/actions/workflows/validate-compose.yml/badge.svg)
![Maintenance](https://img.shields.io/maintenance/yes/2025.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![GitHub release](https://img.shields.io/github/v/release/OnyxJeff/docker-compose_templates)
![Issues](https://img.shields.io/github/issues/OnyxJeff/docker-compose_templates)

Welcome to **docker-compose_templates** — the single source of truth for all my Docker stack templates, optimized for deployment via Portainer.

## Why?

Instead of hunting for random YAML files scattered across the internet, this repo bundles all my curated, tested, and version-controlled Portainer stacks in one place. Deploy anything from lightweight services to complex multi-container apps with a single click.

## 📁 File Structure
```text
docker-compose_templates/
├── .github/workflows/     # CI for YAML validation
├── arr-suite/            # YAML for -darr-suite stack
├── network-solutions/     # YAML for network-solutions stack
└── README.md              # You're reading it!
```
---

## 📦 Included Templates

| Stack Name            | Description                                                   | Notes                                                                     |
| :---:                 | :---:                                                         | :---:                                                                     |
| **arr-suite**         | A full-featured media automation stack designed for Portainer | Normal port-forwarding and functional                                     |
| **network-solutions** | A portable PXE boot service containerized for Portainer       | Some setup in your router is required to load environment on your network |

*More stacks coming soon!*

---

## 🚀 Deployment

### 1. Clone this repo:
   ```bash
   git clone https://github.com/OnyxJeff/portainerhost.git
   cd portainerhost
   ```
### 2. Browse any stack folder (e.g., /arr-suite/)
### 3. Copy the contents of the corresponding .yml file into Portainer’s Stacks > Add Stack UI
### 4. Create or update .env files as needed (check each stack’s README)
### 5. Deploy and enjoy!

---

## 📜 License
MIT — Use it, fork it, build something rad with it.

---

📬 Maintained By
Jeff M. • [@OnyxJeff](https://www.github.com/onyxjeff)