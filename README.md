# RRC_Mech_lab_Xarm7_setup
docs and steps to follow while setting up the arm for manipulations

<img width="515" height="915" alt="image" src="https://github.com/user-attachments/assets/d4227295-ff21-4c97-a015-e03963c5162c" />

## hardware connections
- For Physical Connection : Plug one end of an Ethernet cable into the LAN port on the xArm control box.
- Plug the other end directly into your computer's Ethernet port (or via a compatible adapter).
- Avoid intermediate routers or switches if you need low latency for development.
- Turn on the xArm control box power switch and release the emergency stop. IP Configuration on Your ComputerFind the default controller IP address (typically 192.168.1.243), with the exact address printed on a sticker on the side of the control box).
- Open your computer's network settings and set your IPv4 address manually to be on the same subnet (for example, if the arm is 192.168.1.243, set your PC to 192.168.1.10 in the IPv4 tab).
- Set the Subnet Mask to 255.255.255.0. Disable any active proxy servers on your computer that might block local network traffic.
- Verify the connection by opening a terminal or command prompt and typing ping followed by the arm's IP address. For official troubleshooting steps, check the UFACTORY Help Center.
- Connecting via xArm StudioLaunch the xArm Studio software application on your computer.
- Click Search Server or enter the control box IP address manually into the connection field.
- Select the controller and click Connect to begin operating the robotic arm.
- **Note** IPv4 manual and disable 802.1 security

## Graphical Setup (NetworkManager)
- Open your system Settings and navigate to the Network or Wi-Fi & Network panel.
- Locate your wired Ethernet connection and click the Gear icon next to it.Select the IPv4 tab.Change the IPv4 Method from Automatic (DHCP) to Manual.
- Add the following network parameters in the Address rows:Address: 192.168.1.10 (or any unique address from .2 to .254, except the arm's specific IP)
- Netmask: 255.255.255.0Gateway: Leave blank or set to 192.168.1.1
- Click Apply or Save, then turn the network interface off and back on to apply changes.
