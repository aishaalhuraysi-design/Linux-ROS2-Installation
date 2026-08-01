# Linux-ROS2-Installation
Installation guide for WSL2, Ubuntu 22.04 LTS, and ROS 2 Humble on Windows.
<div align="center">

# 🐧 Linux (WSL2) & ROS 2 Humble Installation

### Installing Ubuntu 22.04 LTS and ROS 2 Humble on Windows using WSL2

![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04%20LTS-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![ROS2](https://img.shields.io/badge/ROS2-Humble-22314E?style=for-the-badge&logo=ros&logoColor=white)
![WSL2](https://img.shields.io/badge/WSL2-Windows-blue?style=for-the-badge&logo=windows)

**Smart Methods Internship – Task 4**

</div>

---

# 📖 Overview

This repository documents the installation of **Ubuntu 22.04 LTS** on **Windows** using **Windows Subsystem for Linux (WSL2)** and the installation of **ROS 2 Humble**.

The project demonstrates the installation process, system configuration, verification commands, and testing ROS 2 after installation.

---

# 🎯 Objectives

- Enable Windows Subsystem for Linux (WSL2)
- Install Ubuntu 22.04 LTS
- Install ROS 2 Humble
- Configure the ROS environment
- Verify that ROS 2 is working successfully

---

# 🛠️ Software & Tools

- Windows 11
- WSL2
- Ubuntu 22.04 LTS
- ROS 2 Humble
- Bash Terminal
- Git
- GitHub

---

# 📂 Repository Structure

```text
Linux-ROS2-Installation/
│
├── README.md
└── screenshots/
    ├── system-update.png
    ├── install-ros.png
    ├── ros2-command.png
    ├── ros-distro.png
    └── listener.png
```

---

# 🚀 Step 1 – Update Ubuntu

After installing Ubuntu, the system packages were updated.

```bash
sudo apt update
sudo apt upgrade -y
```

### Screenshots

![](screenshots/system-update.png)

---

# 🤖 Step 2 – Install ROS 2 Humble

Required packages were installed, followed by the installation of ROS 2 Humble Desktop.

```bash
sudo apt install ros-humble-desktop -y
```

### Screenshots

![](screenshots/install-ros.png)

---

# ⚙️ Step 3 – Configure ROS Environment

The ROS environment was added to the Bash configuration file.

```bash
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

source ~/.bashrc
```

Then the ROS distribution was verified.

```bash
echo $ROS_DISTRO
```

Expected output

```text
humble
```

### Screenshots

![](screenshots/ros-distro.png)

---

# ✅ Step 4 – Verify ROS Installation

The available ROS commands were displayed.

```bash
ros2
```

### Screenshots

![](screenshots/ros2-command.png)

---

# 🧪 Step 5 – Test ROS

A ROS demo node was executed successfully to verify that the installation works correctly.

```bash
ros2 run demo_nodes_cpp listener
```

### Screenshots

![](screenshots/listener.png)

---

# ⚠️ Problems Encountered

During the installation process, a few issues were encountered:

- The WSL download initially timed out because of the internet connection.
- Ubuntu provisioning took several minutes during the first launch.
- The sudo password was rejected initially until the correct password was entered.
- The ROS installation required downloading many packages, so it took some time to complete.

All issues were resolved successfully.

---

# 📚 Technologies

- Ubuntu 22.04 LTS
- Linux
- WSL2
- ROS 2 Humble
- Bash
- Git
- GitHub

---

# 🎉 Conclusion

Ubuntu 22.04 LTS and ROS 2 Humble were successfully installed using WSL2.

The installation was verified by checking the ROS distribution, displaying ROS commands, and running a ROS demo node successfully.

---

<div align="center">

⭐ Thank you for visiting this repository.

</div>
