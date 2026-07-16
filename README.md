# 🚀 Z-Bit VIP Tunnel - zaker240091-bit Edition

This repository contains a professional auto-installation script for SSH and Xray services, optimized for Ubuntu 22.04 and 24.04.

## 📝 Key Improvements & Fixes
This version, renamed to **Z-Bit VIP Tunnel**, includes several critical fixes and enhancements:
- **Connection Stability**: Switched from `restart` to `reload` for Xray services during account creation and renewal. This prevents existing users from being disconnected when a new account is added.
- **Config Detail Fix**: Fixed a bug where account details (UUID, Quota, IP Limit) would disappear after renewal. You can now view full configuration details at any time through the menu.
- **Rebranding**: Professional renaming and cleanup of all menu interfaces.
- **Repository Migration**: All internal script references and download links point to the `zaker240091-bit` GitHub repository.

---

## 💻 System Requirements
- **OS**: Ubuntu 22.04 LTS or Ubuntu 24.04 LTS (x86_64)
- **RAM**: Minimum 1GB
- **CPU**: Minimum 1 Core
- **Domain**: A domain name pointed to your VPS IP address is required for SSL/Xray services.

### Cloudflare Recommended Settings
To ensure full compatibility with Xray (WS/gRPC), use these settings:
- **SSL/TLS**: Full
- **gRPC**: On
- **WebSockets**: On
- **Always Use HTTPS**: Off (let the script handle it)

---

## 🛠️ Installation Guide

Login to your VPS via SSH as **root** and run the following command:

```bash
apt update -y && apt install -y wget curl ca-certificates && wget -q https://raw.githubusercontent.com/zaker240091-bit/z-bit-vip-tunnel/main/setup.sh && chmod +x setup.sh && ./setup.sh
```

---

## 📊 Services & Ports

| Service | Ports |
| :--- | :--- |
| **OpenSSH** | 22, 2222, 2223 |
| **Dropbear** | 109, 143 |
| **SSH WS (HTTP)** | 80, 55, 8880, 2082 |
| **SSH WSS (HTTPS)** | 443, 8443, 2087, 2096 |
| **Xray Vless/Vmess/Trojan** | 80 (None-TLS), 443 (TLS) |
| **Xray gRPC** | 443, 8443, 2087, 2096 |
| **OpenVPN TCP/UDP** | 1194 / 2200 |
| **SlowDNS** | 5300 (UDP) |

---

## ✨ Features
- ✅ **Auto-SSL**: Automatic Let's Encrypt certificate generation.
- ✅ **Monitoring**: Bandwidth usage tracking via Vnstat.
- ✅ **Security**: Fail2ban protection and IP limiting.
- ✅ **Maintenance**: Auto-delete expired users and scheduled reboots.
- ✅ **Optimization**: BBRplus and Swap memory (1GB) auto-configuration.
- ✅ **User Friendly**: Colorful and intuitive CLI menu system.

---

## 📞 Support & Contact
If you encounter any issues or need assistance, feel free to reach out:
- **Telegram**: [@zaker240091-bit](https://t.me/zaker240091-bit)
- **WhatsApp**: [+6282328013583](https://wa.me/6282328013583)

---

## 🙏 Credits
- **Original Base**: Arya Blitar
- **Modification & Maintenance**: zaker240091-bit

**Disclaimer**: This script is provided for educational purposes. Please use it responsibly.
