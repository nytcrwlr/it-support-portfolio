# Standard Operating Procedure (SOP)
## Basic Troubleshooting Guide (Windows & Linux)

### **Introduction**
This SOP outlines common troubleshooting steps for resolving basic system issues on **Windows** and **Linux** operating systems. The guide covers boot issues, display problems, network connectivity errors, and system performance optimizations.

---

## **1. Troubleshooting Boot Issues**
### **Windows Boot Issues**
**Symptoms:**
- Stuck on the Windows logo
- "Operating System Not Found" error
- Blue Screen of Death (BSOD) at startup

**Resolution Steps:**
1. Boot into **Windows Recovery Mode** (Shift + Restart).
2. Open **Command Prompt** and run:
   ```powershell
   bootrec /fixmbr
   bootrec /fixboot
   bootrec /scanos
   bootrec /rebuildbcd
   ```
3. If the issue persists, use **Startup Repair** from Recovery Mode.

### **Linux Boot Issues**
**Symptoms:**
- Stuck on GRUB bootloader
- "Kernel Panic" error
- Black screen after selecting Ubuntu

**Resolution Steps:**
1. Boot into **Recovery Mode** (Hold Shift while booting).
2. Select **Root Shell** and run:
   ```bash
   sudo grub-install /dev/sda
   sudo update-grub
   ```
3. Restart the system:  
   ```bash
   sudo reboot
   ```

---

## **2. Troubleshooting Display Issues**
### **Windows Display Issues**
**Symptoms:**
- Blank screen or flickering display
- Low resolution with no option to change

**Resolution Steps:**
1. Boot into **Safe Mode** and uninstall the GPU driver:
   ```powershell
   devmgmt.msc
   ```
   - Locate **Display Adapters** → Right-click **Uninstall Driver**
2. Restart and reinstall the GPU driver from the manufacturer’s website.

### **Linux Display Issues**
**Symptoms:**
- No graphical user interface (GUI)
- Screen resolution is incorrect

**Resolution Steps:**
1. Boot into terminal mode (**Ctrl + Alt + F3**).
2. Reinstall the graphics driver:
   ```bash
   sudo ubuntu-drivers autoinstall
   ```
3. Restart the system:
   ```bash
   sudo reboot
   ```

---

## **3. Troubleshooting Network Connectivity Issues**
### **Windows Network Issues**
**Symptoms:**
- No internet access
- "Unidentified Network" error

**Resolution Steps:**
1. Open **Command Prompt** as Administrator and reset network settings:
   ```powershell
   netsh winsock reset
   ipconfig /flushdns
   ipconfig /release
   ipconfig /renew
   ```
2. Restart the computer and reconnect to the network.

### **Linux Network Issues**
**Symptoms:**
- No Wi-Fi or Ethernet connectivity
- "Device not managed" error

**Resolution Steps:**
1. Restart the **Network Manager**:
   ```bash
   sudo systemctl restart NetworkManager
   ```
2. Renew the IP address:
   ```bash
   sudo dhclient -r && sudo dhclient
   ```

---

## **4. Optimizing System Performance**
### **Windows Performance Optimization**
1. Open **Task Manager** (`Ctrl + Shift + Esc`) → End high-CPU processes.
2. Disable unnecessary startup applications:
   ```powershell
   taskmgr
   ```
3. Run **Disk Cleanup**:
   ```powershell
   cleanmgr
   ```

### **Linux Performance Optimization**
1. Remove unnecessary files and packages:
   ```bash
   sudo apt autoremove && sudo apt autoclean
   ```
2. Check running processes:
   ```bash
   top
   ```
3. Restart the system for changes to take effect:
   ```bash
   sudo reboot
   ```
