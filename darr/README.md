# 🎬 -darr Stack for Portainer

[![Docker](https://img.shields.io/badge/Docker-Media-blue?logo=docker)](https://www.docker.com/)
[![Sonarr](https://img.shields.io/badge/Sonarr-blue?logo=sonarr)](https://hub.docker.com/r/linuxserver/sonarr)
[![Radarr](https://img.shields.io/badge/Radarr-orange?logo=radarr)](https://hub.docker.com/r/linuxserver/radarr)
[![Lidarr](https://img.shields.io/badge/Lidarr-pink?logo=lidarr)](https://hub.docker.com/r/linuxserver/lidarr)
[![Bazarr](https://img.shields.io/badge/Bazarr-yellow?logo=bazarr)](https://hub.docker.com/r/linuxserver/bazarr)

A full-featured media automation stack designed for Portainer. This stack includes:

- ✅ Sonarr, Radarr, Lidarr, Bazarr
- ✅ Optional: Readarr, Prowlarr
- ✅ Persistent volumes
- ✅ Easy reverse proxy support
- ✅ Built to work with Transmission or qBittorrent (not included)

## 📁 File Structure
```text
darr/
├── docker/             # YAML stack for Sonarr/Radarr/Lidarr/Bazarr
└── README.md           # You're reading it!
```
---

## 🔧 Requirements
- Docker + Portainer
- NGINX Proxy Manager (optional but recommended)
- Transmission/qBittorrent in a separate stack

## 🚀 Deployment

1. In Portainer, go to Stacks > Add Stack
2. Name your stack (e.g., darr-stack)
3. Paste in the contents of the YAML file
4. Deploy the stack

You can also clone this repo and deploy via CLI:

```bash
docker compose -f darr-stack.yml up -d
```
---

## 🌐 Access (default ports)
| Service | Port | URL |
|---------|------|-----|
| Sonarr | 8989 | http://'your-local-ip':8989 |
| Radarr | 7878 | http://'your-local-ip':7878 |
| Lidarr | 8686 | http://'your-local-ip':8686 |
| Bazarr | 6767 | http://'your-local-ip':6767 |

## 🔒 Reverse Proxy Setup (Optional)
If you're using NGINX Proxy Manager:
- Set domain: 'service name'.yourdomain.com
- Forward Host: 'your-local-ip'
- Forward Port: 'service port'

Enable:
- Websockets
- SSL (Let's Encrypt)
- Force HTTPS

---

## 📜 License
MIT — Automate your media empire.

📬 Maintained By
Jeff M. • @OnyxJeff