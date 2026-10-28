# homelab
This is an overview of my home server infrastructure running on bare-metal Proxmox VE. Maybe this could help or inspire someone.

## Hardware
* Model: Fujitsu Esprimo Q556
* Hypervisor: Proxmox VE

## Architecture & Services
Instead of total separation through Linux containers without a UI, most services run as add-ons inside Home Assistant.

* **Home Assistant:** Smart home hub bridging IoT devices across Apple HomeKit and Yandex Smart Home.
* **Scrypted:** RTSP camera feed pipeline streaming directly to Apple TV via HomeKit Secure Video (HSV). It provides secure access to my home cameras and private facial recognition.
* **AdGuard Home:** Local DNS proxy and ad-blocking.
* **Tailscale:** Isolated container providing zero-trust remote access.
* **Matrix Synapse:** Private, end-to-end encrypted messaging server.
* **Cloudflare Tunnels:** Secure zero-trust access for web services via custom domain without opening public ports.

## Repository Structure
* `/home-assistant/` - Sanitized automation YAML configs.
* `/network/` - Network topology diagram & DNS configuration notes.

