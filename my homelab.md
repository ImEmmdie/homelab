# Emmdie Homelab / workstation setup

Hey , here is a little list of my personal homelab , and the setup I'm running nothings too crazy I've been getting into homelab and self-hosted services for a while now some for years other just getting started.

I've been a "data hoarder" for a long time and been into self-hosting for years and i've been playing around with it and learning too.
I've been using my "old" computer at first to make my first servers etc, Now i'm trying to make it the most practical, efficient and "most stable" i can while still having fun messing around with different stuff.

Won't get too crazy with powerfull machine or most importantly power hungry ones because electricy is expensive and my main focus is having something powerfull enough for my needs and future needs while still having a minimum/low power consuption overall because the main server and nas run 24/7 if i were to add stuff would follow my idea of using the minimum power draw posible.

# next step to improve

I'm improving everything step by step when i can my next improvements would be :

* Changing my current ISP plan currently have 2GB down and 1GB up but can have for same price or even little less a 8GBdown/1GBup won't do it just yet because i'm waiting to see if i can find a plan with a higher then 1GB upload speed 

* Not Using my ISP provider router even tho it is a quite good one i wanna have more control and having one where i can set things myself would be nice but this will most probably happen when i don't live with my family members because i don't wanna be called each time internet is down and i have to manual find the issue or go to the house ;)  

* getting a UPS for power loss (just to protect the hardware and data loss because where i live i'm not proned to them often or at all unless theirs a weather issue but warned about beforehand)

* Probably will be done soon but add 2 M.2 SSD's for the UGREEN NAS i don't know yet how to set them up either create a full NVME SSD storage pool for fast file transfer or use 1 SSD for HDD caching and 1 SSD for some fast storage pool without backup or maybe used to run some DOCKER APP or VM off the NAS 

* Upgrading to a 2.5GB/10GB switch so that my NAS is able to benefit from it.

*  Im looking into a SUPER LOW power consuption server (probably a PI) or other mini-pc with a external HDD that would be hosted at a family or friends house for data replication of my IMPORTANT data in case of emergency for now my solution have been COLD storage located at family/friends house and CLOUD storage for backup but having a LIVE backup option is gonna be on my next to do list.

* Maybe in the not near future get a second server for PLEX only where i could use Transcoding if i need to because for now i don't need it but as it grow bigger with more user i might need it later.

* Modeling a custom rack that could be 3D printed.

* Getting a 3D printer for various project i have and mostly make stuff to tidy up my homelab and make it more "compact" and clean looking but also some other personal project i've had for some time now.

* Just added the NAS in MAY 2025 and i'm gonna probably be fine with that much storage for quite some times but who knows maybe as my data usage get greaters might need to get a second NAS ^-^ won't be SOON at all ! 

# First my homelab

my homelab is consisted of 1 server and a Ugreen NAS for storage my second computer (desktop tower) is also used sometimes but rarely only for testing , main one is deimos second one is phobos

## homepage
![homepage](https://i.imgur.com/ciSFnxj.png)

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
* 231 (win-torrent) run Sonarr, Radarr, Prowlarr
* 233 (win-handbrake) used to run handreak and manage files
* 240 (ubuntu-desktop)
* 250 (openmediavault)
* --> 1TB HDD SHARE "torrent" FOR TORRENTS ONLY "BACKUP NOW"
* 251 (openmediavault-time-machine) 
* --> 1TB EXTERNAL DRIVE FOR TIME MACHINE BACKUP ONLY
* 252 (openmediavault-nas) 
* --> 1TB EXTERNAL DRIVE FOR NAS STORAGE SHARE ONLY


## Using the 2.5GB port I'm able to pull thoses speed 
* Im using french ISP router (will upgrade later) have a subsciption for 2GB download and 1GB upload
![speedtest](https://i.imgur.com/P8iInEY.png)

# NAS

UGREEN dXP4800
4HDD SLOT 2 M.2 SSD SLOT upgradable RAM

Configured in RAID 5 (3 Drive for storage 1 drive for parity in case of failure) 21.5TB USABLE

for now do not use the M.2 SSD but will later be used when i get a better network switch capable of over 1GB because my router only have 1 10GB port 

will be used for fast SSD only volume NAS probably no backup only tempary fast storage / working directory 

## specs

* Intel(R) N100 4c/4t
* 8GB DDR5
* 2x 2.5GB LAN
* 4 x Seagate BarraCuda 8TB
* 2x M.2 SSD SLOT (not used)

## storage pool

![storage pool](https://i.imgur.com/dk913HI.png)

## Network Shares
* Plex 
* Personal/Backup data 
* TimeMachineBackup
* NAS (used for quick transfer between different machines)


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
![](https://i.imgur.com/uj1oDq1.png)



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
* MacBook Air 2022 M2 16GB RAM 256GB SSD
* --> mostly used not docked but when it is use 2K monitor and iPad Air 13" for multiple screen usage on desk 

* specs:
![](https://i.imgur.com/JpH2osA.png)

## Second laptop used as a desktop Mac
* MacBook Pro 2020 with a Intel i5-1038NG7 16GB RAM 512GB SSD
* used as a desktop computer almost all the time unless I go where I need a laptop where I don't want to risk accident or damage on my laptop
* --> connected to 2K monitor running at 120hz and the vertical 1080p monitor sometime use iPad Air 13" as third monitor but very rare

* specs:
![](https://i.imgur.com/VIFkM3G.png)
## Ipad
* iPad Air M2 13" 256GB with Apple Pencil pro 
* --> used as second portable screen if needed or at desk but otherwise used for watching stuff and mainly drawing my tattoo designs

## Iphone
* iPhone 14 256GB 
