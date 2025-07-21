# 🎬 -darr Stack for Portainer

[![Docker](https://img.shields.io/badge/Docker-Media-orange?logo=docker)](https://www.docker.com/)
[![Sonarr](https://img.shields.io/badge/Sonarr-orange?logo=sonarr)](https://hub.docker.com/r/mdhiggins/sonarr-sma)
[![Radarr](https://img.shields.io/badge/Radarr-yellow?logo=radarr)](https://hub.docker.com/r/mdhiggins/radarr-sma)
[![Lidarr](https://img.shields.io/badge/Lidarr-yellow?logo=lidarr)](https://hub.docker.com/r/linuxserver/lidarr)
[![Bazarr](https://img.shields.io/badge/Bazarr-green?logo=bazarr)](https://hub.docker.com/r/linuxserver/bazarr)
[![Homarr](https://img.shields.io/badge/Homarr-green?logo=homarr)](https://hub.docker.com/r/homarr-labs/homarr)
[![Jackett](https://img.shields.io/badge/Jackett-blue?logo=jackett)](https://hub.docker.com/r/linuxserver/jackett)
[![Overseerr](https://img.shields.io/badge/Overseerr-blue?logo=overseerr)](https://hub.docker.com/r/linuxserver/overseerr)
[![Prowlarr](https://img.shields.io/badge/Prowlarr-purple?logo=prowlarr)](https://hub.docker.com/r/linuxserver/prowlarr)
[![Tautulli](https://img.shields.io/badge/tautulli-purple?logo=tautulli)](https://hub.docker.com/r/linuxserver/tautulli)

A full-featured media automation stack designed for Portainer. This stack includes:

- ✅ Sonarr, Radarr, Homarr, Overseerr, Prowlarr
- ✅ Optional: Lidarr, Bazarr, Jackett, Tautulli
- ✅ Persistent volumes
- ✅ Easy reverse proxy support
- ✅ Built to work with Transmission or qBittorrent (not included)

## 📁 File Structure
```text
_arr-suite/
├── docker/             # YAML stack for Sonarr/Radarr/Lidarr/Bazarr
└── README.md           # You're reading it!
```
---

## 🔧 Requirements
- Docker + Portainer
- NGINX Proxy Manager (optional but recommended)
- Transmission/qBittorrent in a separate stack

## 🔐 Environment Variables

Create a `stack.env` file based on the included `stack.env.example`, and store it in the same directory as `docker-compose.yml`.

## 🚀 Deployment

1. In Portainer, go to Stacks > Add Stack
2. Name your stack (e.g., darr-stack)
3. Paste in the contents of the YAML file
4. Deploy the stack

You can also clone this repo and deploy via CLI:

```bash
docker compose -f docker-compose.yml up -d
```
---

## 🌐 Access (default ports)
| Service   | Port | URL                         |
|:---:      |:---: |:---:                        |
| Sonarr    | 8989 | http://'your-local-ip':8989 |
| Radarr    | 7878 | http://'your-local-ip':7878 |
| Homarr    | 7575 | http://'your-local-up':7575 |
| Overseerr | 5055 | http://'your-local-up':5055 |
| Prowlarr  | 9696 | http://'your-local-up':9696 |
| Lidarr    | 8686 | http://'your-local-ip':8686 |
| Bazarr    | 6767 | http://'your-local-ip':6767 |
| Jackett   | 9117 | http://'your-local-up':9117 |
| Tautulli  | 8181 | http://'your-local-up':8181 |

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