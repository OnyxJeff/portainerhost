# 🐙 Gitea Stack for Portainer

[![Docker](https://img.shields.io/badge/Docker-Gitea-blue?logo=docker)](https://hub.docker.com/r/gitea/gitea)
[![MariaDB](https://img.shields.io/badge/Database-MariaDB-blue?logo=mariadb)](https://hub.docker.com/_/mariadb)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

A self-contained Gitea Git service stack built for Portainer. This stack includes:

- ✅ Gitea (web UI + SSH support)
- ✅ MariaDB backend
- ✅ Persistent volumes
- ✅ Port override for Gitea web interface (`5123`)
- ✅ Reverse proxy ready (NGINX Proxy Manager compatible)

## 📁 File Structure
```text
gitea/
├── docker/             # YAML-based gitea and mariadb stack
└── README.md           # You're reading it!
```

---

## 🔧 Requirements

- Docker + Portainer
- Optional: NGINX Proxy Manager for domain routing + SSL

## 🚀 Deployment

1. In Portainer, go to **Stacks** > **Add Stack**
2. Name your stack (e.g., `gitea`)
3. Paste in the contents of `gitea-stack.yml`
4. Deploy the stack

You can also clone this repo and deploy via CLI:

```bash
docker compose -f gitea-stack.yml up -d
```
---

## 🌐 Access
| Service | Port | URL Example |
|---------|------|-------------|
| Gitea Web UI | 5123 | http://<your-ip>:5123 |
| Gitea SSH | 2222 | ssh://git@<your-ip>:2222/repo.git |

## 🔒 Reverse Proxy Setup (Optional)
If you're using NGINX Proxy Manager:
- Set domain: 'service name'.yourdomain.com
- Forward Host: 'your-local-ip'
- Forward Port: 'service port'

Enable:
- Websockets
- SSL (Let's Encrypt)
- Force HTTPS

## 🔐 Environment Variables

Create a `gitea.env` file based on the included `gitea.env.example`, and store it in the same directory as `docker-compose.yml`.

**Do not commit your real `gitea.env` file.**

## 🧠 Notes
Uses MariaDB, which is Gitea-compatible and lightweight.
Data is persisted via Docker volumes (gitea-data, gitea-db).
Default web UI is exposed on 5123 to avoid common port collisions.

## 📜 License
MIT — Use it, fork it, build something rad with it.

📬 Maintained By
Jeff M. • [@OnyxJeff](https://www.github.com/onyxjeff)