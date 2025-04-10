# Konzept Serverumgebung

## Resourcen

- Fritz!Box
- Firewall OPNsense
- Router ASUS RT-AC68U
- Proxmox Server
- USV
- NAS

### Fritz!Box

#### Portfreigabe (Router ASUS RT-AC68U)

 - HTTPS -> 192.168.178.74
 - Wireguard (51820/udp) -> 192.168.178.74

#### Service

- DynDNS -> hdxdata.ddnss.de -> Allinkl -> ras.hdxdata.com

### Router ASUS RT-AC68U

- WAN 192.168.178.74
- LAN 192.168.1.1

#### Portfreigabe
	
- HTTPS -> 192.168.1.12
- Wireguard (51820/udp) -> 192.168.1.15

#### VPN

- Wireguard -> NB-HDX-1

### Firewall OPNsense

- LAN 192.168.1.5
- WAN 192.168.178.10
- Hostname/Domain HDXsense / hdxdata.local
- root @dm...
- SSH Port 2525

## Server

### vServer

- Datenbank
- Docker
- PiHole / DNS Server / Wireguard
- Nextcloud

#### VM-HDX-15 (PiHole, DNS Server, Wireguard)

- Clients: SDXphone, HDXphone, NB-HDX-1, NB-HDX-2, NB-SDX-1, HDXpad
