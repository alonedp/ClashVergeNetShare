<p align="center">
  <img src="https://raw.githubusercontent.com/alonedp/ClashVergeNetShare/main/ClashVergeNetShare.png">
</p>

<h1 align="center">
  Mihomo TUN Mode + NetShare Proxy
</h1>

<p align="center">
  Linux traffic routing through Android NetShare using Clash Verge Rev + Mihomo
</p>


## About

A lightweight Mihomo configuration for sharing Android VPN connections with Linux through NetShare.

This project is made for devices that cannot use normal WiFi sharing or hotspot features.

It allows Linux systems to route all network traffic through an Android phone using NetShare HTTP Proxy.

## Features

```
- Mihomo TUN mode
- Full system traffic routing
- Android NetShare support
- Automatic DNS handling
- Clash Verge Rev GUI control
- Linux focused configuration
```

### Install [NetShare](https://play.google.com/store/apps/details?id=kha.prog.mikrotik&hl=en)

```
Connect to Wi-Fi
Open NetShare
✓ Enable "Share WiFi HotSpot"
```

Default proxy:

```
Address : 192.168.49.1
Port    : 8282
```

## Install [ClashVerge](https://github.com/clash-verge-rev/clash-verge-rev)

Copy URL:
```
https://raw.githubusercontent.com/alonedp/ClashVergeNetShare/refs/heads/main/NetShare.yaml
```

Import into Clash Verge Rev:

```
Profiles
   └── Import
          └── Paste NetShare.yaml URL
```


## Clash Verge Settings

Enable:
Enable ClashVerge Service

```
sudo systemctl start clash-verge-service.service
```

System TUN Mode

Select the imported profile and start TUN(Mihomo).

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

<p align="center">
  Made for Linux users who need simple Android-to-PC network sharing.
</p>
