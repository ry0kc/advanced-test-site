+++
date = '2025-09-01T06:16:51-05:00'
draft = false
title = 'Home Server'
+++
### Home Server Project
8-31-2025

### Goal
To build and set up a server that:

- Hosts Home Assistant
- Hosts Jellyfin and media library
- Has remotely accessible storage for adding media

### Plan
1. Repurpose Linux PC with Windows 11
2. Prepare image on usb stick
3. Set bios to boot from image

### Obstacle 1
TPMS is not supported by the motherboard.
I attempted TPMS bypass images with no luck.
Installed Windows 10.
I should note, the process up to this point was taking a really long time.
I knew the resources needed for the server were minimal, but I didn't pay attention to the system specs.
The computer only had 2 GBs of RAM. Another stick of 4 was installed. This sped things up significantly.
I moved the server upstairs and in place, hooked up which was a PITA with the current TV placement.
I attempted to set up the virtual Home Assistant server and

### Obstacle 2
The underlying architecture does not meet the requirements of Oracle VirtualBox. After almost throwing the PC out the window several times, now it would have been appropriate.
The tower case and powersupply are still fine. Board has got to go.

### PC 2 or Plan B
I used a PC I had been setting up for retrogaming and stepmania. This was set up on popOS. Let's revise everything for Linux. NBD.
I created a share with Samba so media can be moved to the server. Jellyfin was installed and configured.
Oracle VirtualBox installed on this computer. I loaded my Home Assistant image I had previsouly set up on my main PC. Forgot my password, of course.
Home Assistant and Jellyfin are working

### Remote Access and Current Status
I'm working on setting up RDP or VNC on the server. I have gotten both to connect, but I currently get a blank screen.
- I need to set up titles and configure the Jellyfin library
- I need to rename, locate, reconnect and otherwise integrate smart devices with Home Assistant

### Update 9-4-25 and Tapo C210
- VNC is working on the server
- I've added my Tapo C210 cameras. They won't provide a live view on a dashboard. RTSP has been disabled or hidden with recent updates.
- Working on automating image capture
ChatGPT has been useful in this endevor. I feel like it has enabled me to see results faster. At the same time, the information provided is similar to if someone glanced over some write ups of similar setups.
The information was often out of date and incompatible. You can feel the edges of the ingested dataset. I am currently using the free version though. 

### Update 9-6-25 and Wyze v2
I have live view for both camera types. To get live views to work on a HA dashboard card, a RTSP is required. For Wyze I had to flash specific firmware.
- These will eventually be replaced with camera's that are independent of a cloud service
I reserved IPs in my router that came with my internet service.
- This will be replaced by my own router.
I added entries to the configuration.yaml of HA to add controls for the Tapo camera's.



