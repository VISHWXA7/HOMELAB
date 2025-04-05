<h1 align="center">🚀 My Homelab Setup</h1>

<p align="center">
  <img src="https://img.shields.io/badge/OS-Ubuntu%20%7C%20Proxmox-orange?style=for-the-badge&logo=linux" />
  <img src="https://img.shields.io/badge/Storage-TrueNAS-blue?style=for-the-badge&logo=freenas" />
  <img src="https://img.shields.io/badge/Containers-Docker-blue?style=for-the-badge&logo=docker" />
</p>

## 🏠 Overview
This homelab is designed to explore **virtualization, storage solutions, and containerized applications**. The setup consists of:

- **Proxmox** as the hypervisor
- **Two Virtual Machines (VMs):**
  - **TrueNAS** for network-attached storage (NAS)
  - **Ubuntu Server** running Docker for hosting applications

---

## ⚙️ Homelab Architecture

```mermaid
graph TD;
    A[Proxmox Hypervisor] -->|VM 1| B[TrueNAS - Storage Server];
    A -->|VM 2| C[Ubuntu Server - Docker Host];
    C -->|Container 1| D[MySQL Database];
    C -->|Container 2| E[Nginx Proxy];
    C -->|Container 3| F[Other Apps];
```

---

## 📌 Virtual Machines

### 🗄️ TrueNAS (Storage)
- Handles file sharing across the network
- Uses **ZFS** for reliability & performance
- Provides **SMB & NFS** shares

### 🖥️ Ubuntu Server (Docker Host)
- Runs multiple Docker containers
- Hosts **MySQL, Nginx, and custom applications**
- Managed using **Portainer**

---

## 📦 Docker Containers
| Container  | Purpose |
|------------|---------|
| 🐳 **MySQL** | Database for apps |
| 🌍 **Nginx** | Reverse proxy for web services |
| 📂 **Portainer** | Web UI for managing Docker |
| 🛠️ **Custom Apps** | Various self-hosted tools |

---

## 🔗 Resources & Documentation
- **Proxmox Setup Guide:** [Official Docs](https://pve.proxmox.com/wiki/Main_Page)
- **TrueNAS Configuration:** [TrueNAS Docs](https://www.truenas.com/docs/)
- **Docker Best Practices:** [Docker Docs](https://docs.docker.com/)

---

- Add **Home Assistant** for smart home automation
- Implement **CI/CD pipelines** for self-hosted apps
- Integrate **monitoring tools** (Grafana + Prometheus)

<p align="center">💻 Built with ❤️ by <strong>Your Name</strong></p>
