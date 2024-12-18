# My homelab 

## homepage
![homepage](https://i.imgur.com/6jCQPl1.png)


# Main "deimos"

minisforum NAB6 LITE mini PC

On all the time 24/7 

## specs

* 12th Gen Intel i5-12600H (16) @ 4.500GHz
* 32GB DDR4-3200
* 512GB NVME SSD KINGSTON
* 1TB HDD SATA HITACHI
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

## virtual machines
* 230 (win-plex)
* 231 (win-torrent)
* 233 (win-nas-manager)
* 240 (ubuntu-desktop)
* 250 (openmediavault)
* --> 1TB HDD SHARE "torrent"
* 251 (openmediavault time machine)
* --> 1TB EXTERNAL DRIVE FOR TIME MACHINE BACKUP 



## internet speed
![speedtest](https://i.imgur.com/GSAFgF2.png)




# PHOBOS

Desktop tower , dual boot proxmox (primary for wake on lan auto lunch) and windows 10 for casual gaming.
Do not run all the time turned on and off remotely when needed.

## specs

* INTEL i5-7400 (4) @ 3.500GHz
* 32GB DDR4-2133 MIX-MATCHED
* NVIDIA GEFORCE GTX 1060 6GB
* 1GB ETHERNET LAN
* 250GB SATA SSD Samsung 850-EVO --> WINDOWS VM
* 500GB SATA SSD KINGSTON  --> WIN10 BOOT DRIVE
* 128GB SATA SSD TOSHIBA --> PROXMOX BOOT DRIVE
* 128GB SATA SSD ADATA --> MISC VM FOR TEST 
* 2TB HDD WESTERN DIGITAL --> NAS SHARE
* 1TB HDD SEAGATE --> NAS SAHRE

## permanent vm
* OpenMediavault  
* windows for 4K torrenting with 250gb sata ssd assign for download
--- --> 2TB SHARE "NAS2TO" / 1TB SHARE "NAS2TO"

## misc
* use to create some various VM and CT to try things or mess around 



## NAS SHARES
![enter image description here](https://i.imgur.com/yf1YOoi.png)



## network shares
* deimos torrent
--> 1TB HDD share for torrent for temporary movies/show and download then transferred to 4TB EXT drive with all Plex libraries
* deimos Mac backup
--> 1TB HDD share for Time Machine backup for my Mac's 



* phobos
--> NAS1TO timemachine share
--> NAS2TO global has share for backup and misc


## neofetch of servers
![enter image description here](https://i.imgur.com/uj1oDq1.png)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc3NDQ1MjQwNiwtNTQwMjYyOTQwLDE3Nz
gzNjYyMDEsMjA0MzE0OTA5LC0xODUyNjcxNjgwLC01NTIwODIx
MDksLTIwMjQzOTE2ODksMTk2MjQ0NDkxOCwyNzYwODYzMDMsNz
UwNTU0NTQwXX0=
-->