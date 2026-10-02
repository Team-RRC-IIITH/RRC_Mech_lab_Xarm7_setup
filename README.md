# RRC_Mech_lab_Xarm7_setup
docs and steps to follow while setting up the arm for manipulations

<img width="515" height="915" alt="image" src="https://github.com/user-attachments/assets/d4227295-ff21-4c97-a015-e03963c5162c" />

## hardware connections
### For Physical Connection 
- Plug one end of an `Ethernet cable` into the LAN port on the `xArm control box`.
- Plug the other end directly into your computer's Ethernet port (or via a compatible adapter).
- Avoid intermediate routers or switches if you need low latency for development.
- Turn on the xArm control box power switch and release the emergency stop. IP Configuration on Your Computer Find the default controller IP address `(typically 192.168.1.243)`, with the exact address printed on a sticker on the side of the control box).
- Open your computer's network settings and set your IPv4 address manually to be on the same subnet (for example, if the arm is `192.168.1.243`, set your PC to `192.168.1.10` in the IPv4 tab).
- Set the `Subnet Mask` to `255.255.255.0`. Disable any active proxy servers on your computer that might block local network traffic.
- Verify the connection by opening a terminal or command prompt and typing ping followed by the arm's IP address. For official troubleshooting steps, check the UFACTORY Help Center.
- Connecting via `xArm StudioLaunch` the `xArm Studio` software application on your computer.
- Click Search Server or enter the control box IP address manually into the connection field.
- Select the controller and click Connect to begin operating the robotic arm.
- **Note** `IPv4 manual` and `disable 802.1 security`

## Graphical Setup (NetworkManager)
- Open your system Settings and navigate to the Network or Wi-Fi & Network panel.
- Locate your wired Ethernet connection and click the Gear icon next to it.Select the IPv4 tab.Change the IPv4 Method from Automatic (DHCP) to Manual.
- Add the following network parameters in the Address rows:Address: 192.168.1.10 (or any unique address from .2 to .254, except the arm's specific IP)
- Netmask: 255.255.255.0
- Gateway: Leave blank or set to 192.168.1.1

<img width="973" height="631" alt="Screenshot from 2026-10-02 15-47-48" src="https://github.com/user-attachments/assets/e371d513-8db3-4d37-b3b4-9ab8fb5fec20" />
<img width="973" height="631" alt="Screenshot from 2026-10-02 15-47-56" src="https://github.com/user-attachments/assets/a70dc2dc-a215-4e25-aa75-d2bbed63a364" />

- Click Apply or Save, then turn the network interface off and back on to apply changes.
- Download `Ufactory studio` from [link](https://www.ufactory.us/ufactory-studio?srsltid=AU7gw4X6c6efC3o2TUn8Yie1jql0HsMmGesOPSMsKLmrybZtRBLqJsf-)
```
cd Donwloads
./UfactoryStudio-Linux-1.0.1.AppImage --no-sandbox
```
<img width="1283" height="832" alt="Screenshot from 2026-10-02 15-49-06" src="https://github.com/user-attachments/assets/3f8f29ad-3cfb-4019-88af-3acaa02b0ad3" />
- Robot access UI for gripper remeber to select G2 gripper
<img width="1914" height="1032" alt="image" src="https://github.com/user-attachments/assets/3eb00510-bea2-418c-bc96-2c155adb312b" />

