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
-darr/
├── docker/             # YAML stack for Sonarr/Radarr/Lidarr/Bazarr
└── README.md           # You're reading it!

## 🔧 Requirements

- Docker + Portainer
- NGINX Proxy Manager (optional but recommended)
- Transmission/qBittorrent in a separate stack

## 🚀 Deployment

- In Portainer, go to Stacks > Add Stack
- Name your stack (e.g., darr-stack)
- Paste in the contents of the YAML file
- Deploy the stack

## 🌐 Access (default ports)
| Service | Port | URL |
| ------- | ---- | --- |
| Sonarr | 8989 | http://<your-ip>:8989 |
| Radarr | 7878 | http://<your-ip>:7878 |
| Lidarr | 8686 | http://<your-ip>:8686 |
| Bazarr | 6767 | http://<your-ip>:6767 |

## 🔒 Reverse Proxy Setup (Optional)
Use NGINX Proxy Manager to forward custom domains to these ports and add SSL support.

## 📜 License
MIT — Automate your media empire.

📬 Maintained By
Jeff M. • @OnyxJeff