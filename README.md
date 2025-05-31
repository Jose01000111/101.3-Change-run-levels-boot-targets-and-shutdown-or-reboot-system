# 🧪 LPIC-1 Lab: Managing Runlevels, Boot Targets, and System Shutdown/Reboot

This repository contains my hands-on lab exercises for **LPIC-1 certification**, focusing on managing system runlevels (boot targets) and controlling shutdown/reboot processes on Linux using `systemd` and legacy tools.

---

## 🚀 What I Did in This Lab

### 🔹 Part 1: Set the Default Runlevel / Boot Target  
I learned how to check and change the system’s default boot target with `systemctl`. I switched between **multi-user** (CLI) and **graphical** (GUI) modes, verified the default target symlink, and explored legacy SysVinit configs.

#### 📚 What I Learned  
How to check and set default boot targets using `systemctl` and understand legacy SysVinit configurations.

---

### 🔄 Part 2: Change Runlevels / Boot Targets on the Fly  
I practiced immediately switching between system states using `systemctl isolate`, including **single-user (rescue)** and **emergency** modes, plus returning to **multi-user** and **graphical** targets. I also used `telinit` as a legacy alternative and manually booted into rescue mode via GRUB.

#### 📚 What I Learned  
How to instantly switch runlevels using `systemctl isolate`, `telinit`, and manual GRUB boot options.

---

### 🔌 Part 3: Shutdown and Reboot from Command Line  
I explored commands to safely **shutdown**, **reboot**, **halt**, and **power off** the system (`shutdown`, `reboot`, `poweroff`, `halt`). I practiced scheduling and canceling shutdowns with user alerts.

#### 📚 What I Learned  
How to safely shutdown, reboot, halt, or power off the system immediately or on schedule with user notifications.

---

### 📢 Part 4: Alert Users Before Runlevel Changes  
I used `wall` to broadcast system alerts to logged-in users before rebooting/shutting down, combined this with `shutdown` notifications, and monitored active sessions with `who` and system uptime with `uptime`.

#### 📚 What I Learned  
How to notify logged-in users of system events and check active users and uptime.

---

### 🧼 Part 5: Properly Terminate Processes  
I viewed running processes using `ps aux`, searched for specific processes with `pgrep`, and gracefully or forcefully terminated processes with `kill`, `killall`, and `htop`.

#### 📚 What I Learned  
How to view, find, and safely terminate processes using command-line tools and `htop`.

---

### ⚡ Part 6: ACPI Awareness and Management  
I checked the status of the ACPI daemon (`acpid`), installed and enabled it, examined ACPI event files (like power button events), and reviewed logs using `journalctl`. This helped me understand power event management on Linux.

#### 📚 What I Learned  
How to manage ACPI events by using, configuring, and troubleshooting the `acpid` service.

---

---
