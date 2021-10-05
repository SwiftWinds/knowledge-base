# 1. Safety

## i. Ear protection

- Earplugs are a must! It might not seem that loud, but it's loud enough that staying there for several hours could lead to temporary or even permanent ear damage.


## ii. Hand protection

- Be sure to wear gloves while carrying or moving servers. Not only to protect your skin but to provide better grip 
  
## iii. Heavy servers

- For 3U servers or heavy 2U servers (or if you're moving several servers), use the server lift.

# 2. Server

## i. General

### a. Installation

- Don’t put server backwards. Look at other servers in the cabinet or row to find correct direction.
- Make sure all the racks are in the same level

### b. Wiring

- **MOST IMPORTANT THING**: Be sure to follow guidelines for wiring. If none are make sure to communicate with others that are wiring and create guidelines
    - Server
        - All the IPMI cable goes from the top right and wiring through the bottom of the server.
        - All the IPMI cable goes from the top right and wiring through the bottom of the server.
    - Switches
        - All the IPMI cable goes from the top right opening and wiring through the bottom of the switches.
        - All the optical cable goes from the top left opening and wiring from the top of the switches.
- Try to keep any ports and lights easily viewable for future use. 

## ii. Dell

- 1 node: slide out the server until it gets stuck. Then press the light blue parts on both sides of the server until it clicks, then continue sliding out
- 4 nodes: press the tab on the IO side of the server, then slide out.

## iii. Supermicro
- 4 nodes: Press tab 

- 12 nodes: Counting is increasing left to right starting from 1. To take out the node press the tab at the top of the node and pull. In order to install Hard drives for these nodes you need to pull out the entire node.

# 3. Switch 

## i. General

## ii. Wire types

- yellow cable are usually 单模

## iii. Module types

- 850nm 多模
- 1310nm 单模 10km
- 1550nm 单模 40km

![光纤](https://github.com/dingbangchen/refactored-octo-succotash/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-10-04%20180411.png) 

![光纤2](https://github.com/dingbangchen/refactored-octo-succotash/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-10-04%20180459.png)

![模块](https://github.com/dingbangchen/refactored-octo-succotash/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-10-04%20180437.png)

# 4. Parts

## i. General

- always put back to Inventory
  
- link to the inventory [Inventory](http://154.196.160.212:5000/oo/r/626452047190864799#tid=1)
## ii. CPU

### a. Positioning
- Both the CPU and the CPU slot have a positioning triangle. When installing make sure the triangles are in the same direction.
### b. Thermal paste
- Make sure that the CPU has some thermal paste applied to the top.
## iii. RAM

### a. General

- There's a couple things that you need to pay attention when installing RAM into server: Whether it's DDR3 or DDR4, How much memory it provides, and the speed of the ram. This information is all listed on the sticker attached (10600 and 12800)


### b. DDR3 (PC3)
- The easiest way to identify DDR3 is by the sticker. If there is no sticker, you can tell by the distance between the prongs. The gap in DDR3 is closer to the edge than in DDR4

### c. DDR4 (PC4)

- Gap in DDR4 is closer to center of RAM stick compared to the DDR3 sticks.

### d. EDIMM & RDIMM

- make sure when installing RAMs(Especially HUAWEI servers, pay attention to the ram see if it has the ECC on it)
## iv. Disk

### a. General

### b. SSD

### c. HDD

- Don't use Seagate ST035 or ST048 disks

### d. M.2

- Remember to put in the correct slot

# 5. Software

## i. IPMI

- [Node identification]()

- [Steps for doing IPMI](https://docs.google.com/document/d/1aHn1oQaDHm5yOgLh7WIOlRoP-4z-t4HVKkUXfEiADAg/edit)


## ii. Ping test

### a. Mac

### b. Windows

- open the network setting -> then open ethernet setting-> change the ip address, ip mask and subnet address(remember to choose the ip that doesn't in use of this cabinet)
- then open `cmd` , type `ping ...... -t` to see if the packages were sent. Type `ctrl c` to quit testing.

## iii. SSH

1. Open your terminal (`cmd` on Windows and `Terminal` on macOS) and type: `ssh -p 19080 root@154.36.250.164`. It should look like this:
![SSH screenshot](https://lh4.googleusercontent.com/yrFKo2DtJO-v4gohdR-cPH-XgF6F61WVlI3o2WyXvQAxbpdVZjgikufEvbsEyVeyKD0sG66gRW1qRAjUuMoEy98sXyMCPGxM-QKlvtXcWWW5UAHAks0Wqy8pAf5KG65W5DbGJIc=s0)
2. Enter password `vr3tbacqad`
3. Enter `./check.sh [name of the rack]`. It should look like this:
![check.sh screenshot](https://lh6.googleusercontent.com/fbxd1MLGC_rU0gfuqaJmBdcykEEyDlryLcbmDDsLGhqOm0wJIiNx7JQZ0AKL8y4-8h0jHbnmDhccbF1s7wYsBHiIO9EVDmhVJJsR88PoJXDOI9ctMvzlvdoAywkn5MIH4gwDGv0=s0)

## iv. Flash drive (for setting IPMI username/password)

## v. BIOS update
