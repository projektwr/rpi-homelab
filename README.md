# Minimalist, lightweight Raspberry Pi Homelab

A lightweight, containerized homelab running on **Raspberry Pi 5** (services). Designed for low power consumption, modular organization, and easy recreation.

---

## 🛠️ Hardware & Architecture

* **Primary Node (Raspberry Pi 5 - 8GB RAM):**
  * **OS:** Raspberry Pi OS (Headless)
  * **Storage:** NVMe HAT + 2x External HDDs/SSDs for media storage
  * **Role:** Runs Docker containerized services managed via a root orchestrator and acts as the primary DNS server using Pi-Hole DNS sinkhole and Unbound DNS server.
---

## 📂 Repository Structure

```text
homelab/
├── docker-compose.yml          # Root orchestrator (uses Docker include)
├── .env.example                # Template for shared environment variables
├── general/                    # Core utilities & dashboards (e.g., Homepage)
├── automation/                 # Arr stack & background tasks
├── media/                      # Jellyfin media streaming server
├── network/                    # Pi-hole & Unbound local DNS configurations
└── vpn-killswitch/             # Gluetun VPN routing stack
