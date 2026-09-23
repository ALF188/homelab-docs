# Network Map
``` mermaid 
flowchart TB
    WAN["WAN<br/>(UWP)"]
    PI["Raspberry Pi 4<br/>Model B"]
    OPENWRT["OpenWRT"]
    SWITCH["TP-Link Ethernet Switch"]
    PC["PC"]
    ROUTER["TP-Link Router"]
    AP["AP<br/>&quot;Keep it on the Download&quot;"]
    HP["HP EliteDesk"]
    UNUSED1["Unused Port"]
    UNUSED2["Unused Port"]
    PROXMOX["Proxmox"]
    VMBR0["vmbr0"]
    SERVICES["Services"]
    VMBR1["vmbr1"]
    MULLVAD["Mullvad VPN"]
    OPENWRT_VM["OpenWRT<br/>VM"]
    JELLYFIN["Jellyfin<br/>LXC"]
    TAILSCALE["Tailscale VPN LXC"]
    UBUNTU["Ubuntu VM"]

    WAN --> PI
    PI --> OPENWRT
    OPENWRT --> SWITCH

    SWITCH --> ROUTER
    SWITCH --> PC
    SWITCH --> HP
    SWITCH --> UNUSED1
    SWITCH --> UNUSED2

    ROUTER --> AP
    HP --> PROXMOX

    PROXMOX --> VMBR0
    PROXMOX --> VMBR1

    VMBR0 --> SERVICES

    VMBR1 --> OPENWRT_VM
    VMBR1 --> MULLVAD

    MULLVAD --> OPENWRT_VM

    OPENWRT_VM --> JELLYFIN
    OPENWRT_VM --> TAILSCALE
    OPENWRT_VM --> UBUNTU
```