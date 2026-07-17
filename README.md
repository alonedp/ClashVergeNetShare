<p align="center">
  <img src="https://github.com/alonedp/alonedp/blob/main/webscrapper.png">
</p>

<h1 align="center">
  ╭━━━ ✦ Mihomo TUN Mode + NetShare Proxy ✦ ━━━╮
</h1>

<p align="center">
  Linux traffic routing through Android NetShare using Clash Verge Rev + Mihomo
</p>


## ✦ About

A lightweight Mihomo configuration for sharing Android VPN connections with Linux through NetShare.

This project is made for devices that cannot use normal WiFi sharing or hotspot features.

It allows Linux systems to route all network traffic through an Android phone using NetShare HTTP Proxy.

```
Android (NetShare)
        │
        │ HTTP Proxy
        ▼
Linux → Clash Verge Rev → Mihomo TUN → Internet
```


## ✦ Features

```
✦ Mihomo TUN mode
✦ Full system traffic routing
✦ Android NetShare support
✦ Automatic DNS handling
✦ Clash Verge Rev GUI control
✦ Linux focused configuration
```


## ✦ Requirements

### Linux

Required:

```
✓ Linux distribution
✓ sudo/root access
✓ NetworkManager
✓ systemd-resolved (recommended)
```


### Android

Install:

```
NetShare - no-root-tethering
```

Enable:

```
✓ WiFi sharing
✓ HTTP Proxy
```

Default proxy:

```
Address : 192.168.49.1
Port    : 8282
```


## ✦ Install Clash Verge Rev

Official project:

https://github.com/clash-verge-rev/clash-verge-rev

Download:

https://github.com/clash-verge-rev/clash-verge-rev/releases


Arch Linux:

```bash
yay -S clash-verge-rev
```

Other distributions:

Download the correct package from the official releases page.

Clash Verge Rev supports Linux, Windows and macOS. :contentReference[oaicite:0]{index=0}


## ✦ Configuration

Download the configuration file from this project:

```
https://github.com/alonedp/ClashVerfeNetShare/blob/main/netshare.yaml
```


Import into Clash Verge Rev:

```
Profiles
   └── Import
          └── Select netshare.yaml
```


## ✦ Clash Verge Settings

Enable:

```
✓ System Proxy
✓ TUN Mode
✓ Service Mode
```


Select the imported profile and start Mihomo.


## ✦ Verify

Check TUN interface:

```bash
ip addr | grep Mihomo
```


Expected:

```
Mihomo: UP
inet 198.18.0.1/30
```


Test connection:

```bash
curl http://example.com
```


If the page loads successfully:

```
✓ Tunnel is working
✓ DNS is working
✓ Traffic is routed through NetShare
```


## ✦ Project Links

Repository:

```
https://github.com/alonedp/ClashVerfeNetShare/tree/main
```


Configuration:

```
https://github.com/alonedp/ClashVerfeNetShare/blob/main/netshare.yaml
```


## ✦ Credits

Built with:

```
✦ Clash Verge Rev
✦ Mihomo Core
✦ NetShare Android
✦ Linux TUN Networking
```


<p align="center">
  ✧ ─────────────── ✦ ─────────────── ✧
</p>

<p align="center">
  Made for Linux users who need simple Android-to-PC network sharing.
</p>
