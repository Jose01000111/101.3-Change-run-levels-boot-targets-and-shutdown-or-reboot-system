# 🧪 LPIC-1 Lab: Managing Runlevels, Boot Targets, and System Shutdown/Reboot

This repository contains my hands-on lab exercises for **LPIC-1 certification**, focusing on managing system runlevels (boot targets) and controlling shutdown/reboot processes on Linux using `systemd` and legacy tools.

I’ve included some helpful links to guide you through the lab and for studying afterward:

[LPIC-1 101.3 Lab](https://1drv.ms/w/c/354f1c8d534fbced/EQqfNBbLmmpNsTJLqNyGLN8B31VhWYOtii0oef8hxjR46A?e=7TDC7q)

---

[LPIC-1 101.3 notes](https://1drv.ms/w/c/354f1c8d534fbced/Ee_QXdk-4WtEt6R0c0udKC4BzTVg6EVnF-0wwHA72TAcMg?e=AiIFnH)

---

[Topic 101.3 Managing Runlevels, Boot Targets, and System Shutdown/Reboot LPI Exam Objectives](https://www.lpi.org/our-certifications/exam-101-102-objectives/#101.3_Change_runlevels_.2F_boot_targets_and_shutdown_or_reboot_system)

---

## 🚀 What I Did in This Lab

### 🔹 Part 1: Set the Default Runlevel / Boot Target  
I learned how to check and change the system’s default boot target with `systemctl`. I switched between **multi-user** (CLI) and **graphical** (GUI) modes, verified the default target symlink, and explored legacy SysVinit configs.

#### 🔹 Check current default target:

#### 🔹 Set default to multi-user (CLI-only):

#### 🔹 Set default to graphical (GUI):

#### 🔹 Confirm the default target symlink:

#### 🔹 (Optional) View legacy SysVinit file:

### 📚 What I Learned  
How to check and set default boot targets using `systemctl` and understand legacy SysVinit configurations.

---

### 🔄 Part 2: Change Runlevels / Boot Targets on the Fly  
I practiced immediately switching between system states using `systemctl isolate`, including **single-user (rescue)** and **emergency** modes, plus returning to **multi-user** and **graphical** targets. I also used `telinit` as a legacy alternative and manually booted into rescue mode via GRUB.

#### 🔸 Switch to single-user mode (rescue):

#### 🔸 Switch to emergency mode:

#### 🔸 Return to multi-user (no GUI):

#### 🔸 Switch to graphical target:

#### 🧯 (SysVinit alternative) Use telinit:

### 📚 What I Learned  
How to instantly switch runlevels using `systemctl isolate`, `telinit`, and manual GRUB boot options.

---

### 🔌 Part 3: Shutdown and Reboot from Command Line  
I explored commands to safely **shutdown**, **reboot**, **halt**, and **power off** the system (`shutdown`, `reboot`, `poweroff`, `halt`). I practiced scheduling and canceling shutdowns with user alerts. 

#### 🟡 Cancel scheduled shutdown

#### 🔁 Reboot immediately

#### 🔻 Power off immediately

#### 🔕 Halt system (no power off)

### 📚 What I Learned  
How to safely shutdown, reboot, halt, or power off the system immediately or on schedule with user notifications.

---

### 📢 Part 4: Alert Users Before Runlevel Changes  
I used `wall` to broadcast system alerts to logged-in users before rebooting/shutting down, combined this with `shutdown` notifications, and monitored active sessions with `who` and system uptime with `uptime`.

#### 💬 Notify logged-in users

#### 🔄 Combine with shutdown alert

#### 👥 See who is logged in

#### ⏱️ View system uptime

### 📚 What I Learned  
How to notify logged-in users of system events and check active users and uptime.

---

### 🧼 Part 5: Properly Terminate Processes  
I viewed running processes using `ps aux`, searched for specific processes with `pgrep`, and gracefully or forcefully terminated processes with `kill`, `killall`, and `htop`.

#### 📄 Show all running processes

#### 🔍 Find process by name

#### 🧯 Gracefully stop a process

#### 💥 Force kill a stuck process

#### 🧼 Kill all by process name

#### 📊 Use htop (install if needed)

### 📚 What I Learned  
How to view, find, and safely terminate processes using command-line tools and `htop`.

---

### ⚡ Part 6: ACPI Awareness and Management  
I checked the status of the ACPI daemon (`acpid`), installed and enabled it, examined ACPI event files (like power button events), and reviewed logs using `journalctl`. This helped me understand power event management on Linux.

#### 💤 Manage ACPI events (like power button press)

#### 🔍 Check if acpid is running

#### 📦 Install acpid

#### ▶️ Start and enable acpid

#### 📁 View ACPI event files

#### 📜 View power button event

#### 🧾 View logs

#### 📚 What I Learned  
How to manage ACPI events by using, configuring, and troubleshooting the `acpid` service.

---
