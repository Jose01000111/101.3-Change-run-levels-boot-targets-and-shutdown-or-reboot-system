# 🧪 LPIC-1 Lab: Managing Runlevels, Boot Targets, and System Shutdown/Reboot

This project contains my hands-on lab exercises for **LPIC-1 certification**, focusing on managing system runlevels (boot targets) and controlling shutdown/reboot processes on Linux using `systemd` and legacy tools.

I’ve included some helpful links to guide you through the lab and for studying afterward:

[LPIC-1 101.3 Lab](https://1drv.ms/w/c/354f1c8d534fbced/EQqfNBbLmmpNsTJLqNyGLN8B31VhWYOtii0oef8hxjR46A?e=7TDC7q)

---

[Objective: 101.3 Notes](https://1drv.ms/w/c/354f1c8d534fbced/Ecoc8OrwTAhFtrOjv7kP9a0B6TBTXFq_DxSAIxlLZuZhrg?e=oxo6MT)

---

[Objective: 101.3 Managing Runlevels, Boot Targets, and System Shutdown/Reboot LPI Exam Objectives](https://www.lpi.org/our-certifications/exam-101-102-objectives/#101.3_Change_runlevels_.2F_boot_targets_and_shutdown_or_reboot_system)

---

## 🚀 What I Did in This Lab

### 🔹 Part 1: Set the Default Runlevel / Boot Target  
I learned how to check and change the system’s default boot target with `systemctl`. I switched between **multi-user** (CLI) and **graphical** (GUI) modes, verified the default target symlink, and explored legacy SysVinit configs.

#### 🔹 Check current default target:

#### 🔹 Set default to multi-user (CLI-only):

![KfwXFGa](https://github.com/user-attachments/assets/cac4c5ba-cf29-4365-ad86-6fdad99b0cae)

#### 🔹 Set default to graphical (GUI):

#### 🔹 Confirm the default target symlink:

![89gwe0p](https://github.com/user-attachments/assets/543c70b7-8278-47ad-8673-b7bea02c94a7)

#### 🔹 (Optional) View legacy SysVinit file: (I used an Ubuntu machine therefore: Instead of /etc/inittab, Ubuntu uses systemd targets to manage boot levels.)
![iYcMnz8](https://github.com/user-attachments/assets/3823a697-a6ed-4e46-8a3d-6316f2c14496)

### 📚 What I Learned  
How to check and set default boot targets using `systemctl` and understand legacy SysVinit configurations.

---

### 🔄 Part 2: Change Runlevels / Boot Targets on the Fly  
I practiced immediately switching between system states using `systemctl isolate`, including **single-user (rescue)** and **emergency** modes, plus returning to **multi-user** and **graphical** targets. I also used `telinit` as a legacy alternative and manually booted into rescue mode via GRUB.

#### 🔸 Switch to single-user mode (rescue):


#### 🔸 Switch to emergency mode:

#### 🔸 Return to multi-user (no GUI):

![UelJGPH](https://github.com/user-attachments/assets/a71e1340-ab0f-4273-811b-ae1821292bdb)

#### 🔸 Switch to graphical target:

#### 🧯 (SysVinit alternative) Use telinit:

![mWTFD7k](https://github.com/user-attachments/assets/3a499f77-b903-4014-a1fd-f9d3ef4331ab)

### 📚 What I Learned  
How to instantly switch runlevels using `systemctl isolate`, `telinit`, and manual GRUB boot options.

---

### 🔌 Part 3: Shutdown and Reboot from Command Line  
I explored commands to safely **shutdown**, **reboot**, **halt**, and **power off** the system (`shutdown`, `reboot`, `poweroff`, `halt`). I practiced scheduling and canceling shutdowns with user alerts. 

#### 🟡 Cancel scheduled shutdown

#### 🔁 Reboot immediately

![wHrpj1f](https://github.com/user-attachments/assets/aa150a75-8b9b-4c83-853d-42d7e320619e)

#### 🔻 Power off immediately (unable to screenshot) 

#### 🔕 Halt system (no power off) What does halt do?
halt immediately stops the CPU without necessarily powering off the machine.

![XESGTwr](https://github.com/user-attachments/assets/5ed74d2d-1561-477c-9d7e-14b9be6e4586)

### 📚 What I Learned  
How to safely shutdown, reboot, halt, or power off the system immediately or on schedule with user notifications.

---

### 📢 Part 4: Alert Users Before Runlevel Changes  
I used `wall` to broadcast system alerts to logged-in users before rebooting/shutting down, combined this with `shutdown` notifications, and monitored active sessions with `who` and system uptime with `uptime`.

#### 💬 Notify logged-in users

#### 🔄 Combine with shutdown alert

![ZKtsEUq](https://github.com/user-attachments/assets/0ae3b5af-9912-4db8-bcfe-ba14a0a02372)

#### 👥 See who is logged in

#### ⏱️ View system uptime

![LHrDdjU](https://github.com/user-attachments/assets/0def8d59-b527-4efd-ba8d-7d1ac0e88287)

### 📚 What I Learned  
How to notify logged-in users of system events and check active users and uptime.

---

### 🧼 Part 5: Properly Terminate Processes  
I viewed running processes using `ps aux`, searched for specific processes with `pgrep`, and gracefully or forcefully terminated processes with `kill`, `killall`, and `htop`.

#### 📄 Show all running processes

![GrRbvYO](https://github.com/user-attachments/assets/9e9d1640-3611-4136-95d7-08384c8dfb26)

#### 🔍 Find process by name

![FVnUQtP](https://github.com/user-attachments/assets/beabdc29-1a84-4b33-b193-7a834c521264)

#### 🧯 Gracefully stop a process

#### 💥 Force kill a stuck process

#### 🧼 Kill all by process name (Didn't actually kill any proces, safe example)

![gw2YbkH](https://github.com/user-attachments/assets/6d187329-9cc9-4430-843f-4f698b429803)

#### 📊 Use htop (install if needed)

![umVbXYf](https://github.com/user-attachments/assets/b539042e-dfec-44a1-980d-f1bad4a1d04a)

### 📚 What I Learned  
How to view, find, and safely terminate processes using command-line tools and `htop`.

---

### ⚡ Part 6: ACPI Awareness and Management  
I checked the status of the ACPI daemon (`acpid`), installed and enabled it, examined ACPI event files (like power button events), and reviewed logs using `journalctl`. This helped me understand power event management on Linux.

#### 💤 Manage ACPI events (like power button press)

#### 📦 Install acpid

![8LXr8GO](https://github.com/user-attachments/assets/2514fb2a-0551-4ff6-b04c-b78658b7480c)

#### 🔍 Check if acpid is running

![4V5CK9L](https://github.com/user-attachments/assets/3e49d756-6e72-4acd-a828-8d8e1ebc3514)

#### ▶️ Start and enable acpid

![ibvioN7](https://github.com/user-attachments/assets/8788db52-e114-4cec-b5ac-dccb6c795110)

#### 📜 View power button event

![ww7FIsp](https://github.com/user-attachments/assets/1a24ecf7-abb2-4a0a-a035-f837290abfd7)

#### 🧾 View logs

![xqYtx1d](https://github.com/user-attachments/assets/9c8abd0e-1e7b-4fb1-9365-15e0ac4dc8b1)

#### 📚 What I Learned  
How to manage ACPI events by using, configuring, and troubleshooting the `acpid` service.

---
