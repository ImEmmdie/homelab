# Emmdie Homelab / workstation setup

Hey , here is a little list of my personal homelab , and the setup I'm running nothings too crazy I've been getting into homelab and self-hosted services for a while now some for years other just getting started.

# First my homelab

my homelab is consisted of 2 computer , main one is deimos second one is phobos

## homepage
![homepage](https://imgur.com/a/AdXpGp8)

## Deimos 
deimos run 24H non stop (unless theirs a power cut or something like this)
its a mini pc the minisforum NAB6 LITE mini PC 
Its running Proxmox and here are the specs and what services , containers, visual machines are running on it 

## specs

* 12th Gen Intel i5-12600H (16) @ 4.500GHz
* 32GB DDR4-3200
* 512GB NVME SSD KINGSTON
* 1TB HDD SATA HITACHI
* 1TB EXTERNAL HDD
* 1TB EXTERNAL HDD
* 4TB EXTERNAL HDD 
* 2x 2.5GB LAN ETHERNET PORT

## containers
* 201 (wireguard-vpn)
* 202 (pihole)
* 203 (tautulli)
* 204 (homepage)
* 205 (flaresolverr)
* 206 (overseerr)
* 207 (docker)
* 208 (flaresolverr-backup)

## virtual machines
* 230 (win-plex) only run plex
* --> 4TB USB HDD FOR PLEX LIBRARY
* 231 (win-torrent) run Sonarr, Radarr, Prowlarr
* 233 (win-handbrake) used to run handreak and manage files
* 240 (ubuntu-desktop)
* 250 (openmediavault)
* --> 1TB HDD SHARE "torrent" FOR TORRENTS ONLY
* 251 (openmediavault-time-machine) 
* --> 1TB EXTERNAL DRIVE FOR TIME MACHINE BACKUP ONLY
* 252 (openmediavault-nas) 
* --> 1TB EXTERNAL DRIVE FOR NAS STORAGE SHARE ONLY


## Using the 2.5GB port I'm able to pull thoses speed
![speedtest](https://i.imgur.com/GSAFgF2.png)



# PHOBOS

Desktop tower , dual boot proxmox (primary for wake on lan auto lunch) and windows 11 for casual gaming.
Do not run all the time turned on and off remotely when needed.

## specs

* INTEL i5-7400 (4) @ 3.500GHz
* 32GB DDR4-2133 MIX-MATCHED
* NVIDIA GEFORCE GTX 1060 6GB
* 1GB ETHERNET LAN
* 250GB SATA SSD Samsung 850-EVO 
* 500GB SATA SSD KINGSTON 
* 128GB SATA SSD TOSHIBA
* 2TB HDD WESTERN DIGITAL --> NAS SHARE
* 1TB HDD SEAGATE --> NAS SAHRE

## virtual machines
* 151 (win-plex) backup Plex vm in case of main server break 
* 152 (win-torrent) backup in case of main server break
* 153 (openmediavault-NAS) NAS storage share for largers files backup 
* --> 2TB HDD SHARE "phobos-nas" for storage only
* 154 (openmediavault-TM) Time Machine backup server for my mac's
* --> 1TB HDD SHARE "phobos-timemachine" for Time Machine backup only

## misc
* use this server to run some new services, try software and test things out in general before I get comfortable , knowledgeable enough to use on the main server

## neofetch of servers
![enter image description here](https://i.imgur.com/uj1oDq1.png)



# My devices 

here a little list of my devices I use daily(ish) I don't use windows computer anymore unless its for some gaming where I profit of high refresh rates for gaming I use geforce-now services so a lot of apple devices here.

if I need a specific software only running windows I will use windows VM on my server and remote connect to it from my laptop most of the time 

## Desk setup
* 2K IPS 144hz monitor ACER XV272U
* 1080P 60HZ vertical monitor Iiyama PL2283H
* Logitech Mx Master mouse
* Apple Magic Trackpad 
* Logitech Mx Key mini 
* no brand laptop stand and monitor stand 

* UGREEN Revodok 107 Hub USB C
-> PD 100w get power from 2020 MacBook Pro charging block , connected to 2K monitor , ethernet , usb cable for keyboard, trackpad charging
it is fixed under the laptop stand 
* another Ugreen usb c hub with only hdmi and usb ports
-> connected to vertical monitor only (use this usb c dongle as a travel dongle if needed 



## Main laptop 
* MacBook Air M2 16GB RAM 256GB SSD
* --> mostly used not docked but when it is use 2K monitor and iPad Air 13" for multiple screen usage on desk 
## Second laptop used as a desktop Mac
* MacBook Pro 2020 with a Intel i5-1038NG7 16GB RAM 512GB SSD
* used as a desktop computer almost all the time unless I go where I need a laptop where I don't want to risk accident or damage on my laptop
* --> connected to 2K monitor running at 120hz and the vertical 1080p monitor sometime use iPad Air 13" as third monitor but very rare
## Ipad
* iPad Air M2 13" 256GB with Apple Pencil pro 
* --> used as second portable screen if needed or at desk but main otherwise used for watching stuff and mainly drawing my tattoo designs
## Iphone
* iPhone 14 256GB 
