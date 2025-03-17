# Standard Operating Procedure (SOP): OS Installation & Troubleshooting

**Author:** Dave Andrew
**Date:** March 17, 2025  

---

## **1️⃣ How to Install Windows 10/11 (Step-by-Step Guide)**

### **Prerequisites:**
- Bootable USB with Windows 10/11 ISO (Created using the Media Creation Tool)
- PC with a minimum of 4GB RAM and 64GB storage
- Backup of all important files (if reinstalling)

### **Installation Steps:**
1. **Create Bootable USB:**
   - Download the **Windows Media Creation Tool** from Microsoft’s official site.
   - Use the tool to create a **bootable USB drive**.

2. **Enter BIOS & Set Boot Priority:**
   - Restart the PC and press **F2, F12, DEL, or ESC** (depends on motherboard) to enter BIOS.
   - Set the **USB drive** as the primary boot device.

3. **Start Windows Installation:**
   - Boot from the USB and click **Install Now**.
   - Select **Custom Installation** if performing a clean install.
   - Format the target drive if necessary and select it for installation.

4. **Complete Setup:**
   - Wait for the installation to complete (system will restart multiple times).
   - Follow the **on-screen prompts** to configure **language, keyboard, and user settings**.
   - Activate Windows using a valid license key.

5. **Install Drivers & Updates:**
   - Connect to the internet and run **Windows Update**.
   - Manually install missing drivers (Display, Network, Audio) via **Device Manager**.

---

## **2️⃣ How to Install Ubuntu Linux (Step-by-Step Guide)**

### **Prerequisites:**
- Bootable USB with Ubuntu ISO (Created using **Rufus or Etcher**)
- PC with at least **4GB RAM and 25GB free disk space**

### **Installation Steps:**
1. **Create Bootable USB:**
   - Download the latest **Ubuntu ISO** from the official Ubuntu website.
   - Use **Rufus or Etcher** to create a bootable USB.

2. **Enter BIOS & Set Boot Priority:**
   - Restart the PC and enter BIOS using **F2, F12, DEL, or ESC**.
   - Set **USB drive** as the first boot device.

3. **Start Ubuntu Installation:**
   - Select **Try Ubuntu** to test before installation.
   - Click **Install Ubuntu** and select **Erase Disk** (for clean installation) or **Install alongside existing OS**.

4. **Set Up System Preferences:**
   - Choose a **timezone**, create a **username & password**.
   - Wait for installation to complete and reboot when prompted.

5. **Install Updates & Drivers:**
   - Open **Terminal** and run:
     ```sh
     sudo apt update && sudo apt upgrade -y
     ```
   - Install missing drivers using:
     ```sh
     sudo ubuntu-drivers autoinstall
     ```

---

## **3️⃣ Troubleshooting OS Installation Issues**

### **Common Windows Installation Issues & Fixes**
| Issue | Solution |
|--------|---------|
| Windows setup stuck | Restart installation, use a different USB drive |
| No drives detected | Load SATA/NVMe drivers from motherboard’s website |
| Boot loop after install | Check BIOS Boot Order, disable Secure Boot |
| Activation issues | Ensure internet connection, verify license key |
| Missing drivers | Download drivers from manufacturer’s support page |

### **Common Linux Installation Issues & Fixes**
| Issue | Solution |
|--------|---------|
| No WiFi detected | Install drivers with `sudo apt install firmware-linux` |
| Bootloader issues | Reinstall GRUB with `sudo grub-install /dev/sda` |
| Black screen after install | Boot in safe mode and install graphics drivers |
| Keyboard/mouse not working | Try a different USB port, check BIOS USB settings |

---

## **4️⃣ Common Driver Problems & Solutions**

### **Windows Driver Issues:**
| Issue | Solution |
|--------|---------|
| No audio output detected | Install latest audio drivers from Device Manager |
| No internet connection | Install Ethernet/WiFi drivers manually |
| Display resolution stuck | Update GPU drivers from NVIDIA/AMD/Intel |
| Unknown devices in Device Manager | Use **Windows Update** or vendor’s driver support page |

### **Linux Driver Issues:**
| Issue | Solution |
|--------|---------|
| WiFi not working | Use `lspci` to identify the card and install appropriate drivers |
| No sound | Check `alsamixer` settings, install `pulseaudio` |
| Bluetooth issues | Restart Bluetooth service using `sudo systemctl restart bluetooth` |
| Printer not detected | Install printer drivers using `sudo apt install cups` |

---


