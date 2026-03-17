# wpa2-enterprise-radius-lab
WPA2-Enterprise network with RADIUS authentication - Lab implementation
#  WPA2-Enterprise & RADIUS Authentication Lab

> Migrating from shared-key (PSK) to individual identity-based Wi-Fi authentication

##  Architecture
- **Access Point:** Router YAHYA — IP: 192.168.10.2
- **RADIUS Server:** IP: 192.168.10.20 — Secret: ****
- **SSID:** YAHYA — Security: WPA2-Enterprise

##  Tech Used
- FreeRADIUS Server
- Wi-Fi Router (WPA2-Enterprise mode)
- Windows Client + WPC300N adapter

##  Configuration Steps
| Step | Description |
|------|-------------|
| Blueprint 1 | RADIUS Server: AAA service + users (user1/****, user2/****) |
| Blueprint 2 | Router: WPA2-Enterprise mode + RADIUS IP |
| Blueprint 3 | Client: Wi-Fi profile + EAP authentication |

##  Lessons Learned
- Shared Secret must be **identical** on router AND server
- Disable all open SSIDs (5G/Guest) to avoid security bypass
- Client gets IP from DHCP **only after** successful authentication

##  Proof of Success
- ✔️ Connected to SSID `YAHYA`
- ✔️ IP assigned: `192.168.10.101`
- ✔️ Ping `192.168.10.20` → Response < 1ms
