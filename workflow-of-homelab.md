# Little rundown of how i runs everuthing

I run everything in my homelab localy , everything in VM or CT 
nothing exept the PLEX server is going outside my network directly 

All my homelab equipement is setup with Wake On Lan ON so they can be turned on if they were turned off for any reason.

the windows VM i run all have VPN all the time running 

i have 3 VPN set up 2 of them are WIREGUARD VPN, main one is set up on my proxmox server deimos , second one is on my desktop pc phobos as backup. And the third one for last resort option is a openvpn directly setup on my ISP router that is turned off but could turn it on using machines in my house via teamviewer access in case i'm not at home or near.

i access my Windows VM mostly via windows RDP, but i have also parsec and teamviewers setup on them in case RDP is having issue 

for the linux CT i use SSH all the time i rarely use proxmox web unless i need to set something up or create new VM's / CT's 

I use wireguard VPN to remotly access everything either on my laptops if i don't have access to my laptops and need to i use wireguard on my ipad or iphone , i can acess windows remote desktop while using wireguard if i need to or acess proxmox server directly either via ios app or via SSH

