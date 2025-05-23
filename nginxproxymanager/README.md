# 🌐 NGINX Proxy Manager for Portainer

[![Docker](https://img.shields.io/badge/Docker-ReverseProxy-blue?logo=docker)](https://hub.docker.com/r/jc21/nginx-proxy-manager)
[![NGINX](https://img.shields.io/badge/NGINX-Proxy-green?logo=nginx)](https://nginxproxymanager.com/)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

An easy-to-use NGINX reverse proxy container with a full web UI for managing domains, SSL certs, and routing.

- ✅ UI-based domain & SSL management
- ✅ Built-in Let's Encrypt support
- ✅ Custom port mapping
- ✅ Persistent volumes for config

## 📁 File Structure
```text
nginxproxymanager/
├── docker/             # YAML for nginx-proxy-manager container
└── README.md           # You're reading it!
```
---

## 🔧 Requirements
- Docker + Portainer
- Port 80 and 443 exposed
- DNS pointed to your server IP

## 🚀 Deployment
1. In Portainer, go to Stacks > Add Stack
2. Name your stack (e.g., npm)
3. Paste in the contents of nginxproxymanager-stack.yml
4. Deploy and access via the default port

## 🌐 Access
| Service | Port | URL |
|---------|------|-----|
| Admin Web UI | 81 | http://<your-ip>:81 |
| HTTP Routing | 80 | Your domain |
| HTTPS Routing | 443 | Your domain |

## 🔒 Initial Login
- Email: admin@example.com
- Password: changeme
(You’ll be prompted to reset on first login.)

---

## 📜 License
MIT — Point domains like a boss.

📬 Maintained By
Jeff M. • @OnyxJeff