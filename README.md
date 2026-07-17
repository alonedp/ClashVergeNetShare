<p align="center">
  <img src="https://github.com/alonedp/alonedp/blob/main/webscrapper.png">
</p>

# Mihomo TUN Mode + NetShare Proxy (Linux)

A simple Mihomo/Clash Verge Rev configuration for sharing Android VPN connections with Linux through NetShare.

This project is designed for devices that cannot use normal WiFi sharing or hotspot features.  
It allows Linux systems to route all network traffic through an Android device using NetShare.

## Features

• Mihomo TUN mode support  
• Automatic routing through Clash Verge Rev  
• DNS handling with Mihomo  
• Android NetShare HTTP proxy support  
• Designed for Linux systems


## Requirements

### Linux

Required:

- Linux distribution (Arch, Debian, Ubuntu, Fedora, etc.)
- sudo/root access
- NetworkManager
- systemd-resolved (recommended)


### Android

Install:

NetShare - no-root-tethering

Enable:

• WiFi sharing  
• HTTP Proxy

Default proxy:

```
Address: 192.168.49.1
Port: 8282
```


## Install Clash Verge Rev

Download:

https://github.com/clash-verge-rev/clash-verge-rev/releases


Arch Linux:

```bash
yay -S clash-verge-rev
```

or install the package from the official releases page.


## Configuration

Download the project configuration:

https://github.com/alonedp/alonedp/blob/main/netshare.yaml


Import into Clash Verge Rev:

```
Profiles → Import → Select netshare.yaml
```


## Clash Verge Settings

Enable:

```
✓ System Proxy
✓ TUN Mode
✓ Service Mode
```

Select the imported profile and start Mihomo.


## Verify Installation

Check TUN interface:

```bash
ip addr | grep Mihomo
```

Expected output:

```
Mihomo: UP
inet 198.18.0.1/30
```


Test connection:

```bash
curl http://example.com
```

If the page loads, the tunnel is working correctly.


## Project Repository

Repository:

https://github.com/alonedp/alonedp


Configuration file:

https://github.com/alonedp/alonedp/blob/main/netshare.yaml
