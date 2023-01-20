# Building Linux Distribution for Up-Board Using the Yocto Project

**hardware:**

* https://up-board.org/#upcommunity
* https://up-board.org/


**This README file contains information on building the meta-up-board BSP layer**

**meta-up-board BSP layer:**

Supported hardware versions for Yocto 2.5 (sumo)
      

• Clone Poky using Git

• Clone meta-intel.git

• Clone layers for OE-core universe for Sumo

• Clone meta-virtualization and openembedded-core for 	Docker containers

• Clone UP Board BSP layer for Sumo
      
**Yocto image for each UP machine:**
      
• Building your Yocto image for UP machine
    
    TEMPLATECONF=meta-up-board/conf source oe-init-build-env
    MACHINE=up-core-plus bitbake upboard-image-sato
      
**Bootable USB flash device:**

• :Booting the live USB image
      
      #dd if=core-image-sato-up-board.hddimg of=/dev/sdf
      
      #sync, 
      
      #eject /dev/sdf
 
**Connecitvity firmware:**

• Connectivity firmware is included to enable WiFi and Bluetooth for UPCorePlus boards

WiFi:

* Scan your available WiFi networks:

Bluetooth:

    # systemctl restart firmware-ampak-ap6355.service
    # rfkill unblock bluetooth
    # hciconfig hci0
    # hcitool scan


