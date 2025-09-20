# *Week 0* VSD RISC-V Tapeout Program ![Tool Installation Status](https://img.shields.io/badge/Installation_of_Tools-Done-green)

This document describes the setup and verification of the required tools for the VSD RISC-V Tapeout program, \
keeping it Professional Informative Simple and Sweet  (please don't make an acronym out of this!)

## Table of Contents

1. [System Information](#system-information)
2. [Yosys](#yosys-installation)
   - [Installation of Yosys](#installation)
   - [Tool Check](#tool-check)
3. [Iverilog](#iverilog-installation)
   - [Installation of Iverilog](#installation-1)
   - [Tool Check](#tool-check-1)
4. [GTKWave](#gtkwave-installation)
   - [Installation of GTKWave](#installation-2)
   - [Tool Check](#tool-check-2)

---

## System Information:
Retrieved using `neofetch`

|OS        | Zorin OS 17.3 x86_64 (Ubuntu 22.04 LTS based) |
|-----------|--------|
| Host      | Inspiron 5509 |
| Kernel    | 6.8.0-83-generic |
| DE        | GNOME 43.9 |
| Terminal  | gnome-terminal |
| CPU       | Intel i5-1135G7 (11th Gen) |
| GPU       | Intel TigerLake-LP GT2 [Iris Xe Graphics] |
| Memory    | 7.7 GB |

Running Linux natively using Dual Boot.

---

## Yosys Installation:

Download the `oss-cad-suite-linux-x64-20250916.tgz` file from releases page of [OSS-CAD-Suite](https://github.com/YosysHQ/oss-cad-suite-build) repository \
It contains most of the Open-source tools for ASIC design with the latest updates, including *Yosys*, which we require.

Currently, this is the only effective way to install Yosys, suggested by the contributors themselves. \
Installation guide for your reference: https://github.com/YosysHQ/oss-cad-suite-build#installation

### Installation:

The following commands are used to completely install Yosys (along with the other tools in OSS-CAD-Suite)

```bash
cd ~/Downloads 
# The place the tgz file is downloaded
tar -xvzf oss-cad-suite-linux-x64-20250916.tgz -C ~/Documents/Apps
```
I'll be storing it in `/Documents/Apps` folder, you may change it as per your liking 

```bash
vim ~/.bashrc 
# You may use gedit instead of vim
```
```bash
export PATH="$HOME/Documents/Apps/oss-cad-suite/bin:$PATH" 
# At the end of the file that opened
```
then,

```bash
source ~/.bashrc
```
and with that Yosys installation is successfully done ✔️


### Tool Check:

```bash
yosys
license
```

<img width="750" height="752" alt="Yosys" src="https://github.com/user-attachments/assets/0dbf43e4-5811-4fb0-a052-7bd51e7a7f5e" />

---

## Iverilog Installation:

Iverilog comes bundled with the OSS-CAD Suite, but the problem is, it comes with the latest version of 13 which isn't regarded as stable in Iverilog's documentation \
Thus, we have to manually revert back to a stable version. \
This is done by deleting all iverilog files that came bundled with OSS-CAD Suite (using the search function might be helpful) 

### Installation:

Use the below script to install version 11 of iverilog.

```bash
sudo apt update
sudo apt-get install iverilog
```

### Tool Check:

```bash
iverilog -V
```

<img width="746" height="1102" alt="Iverilog" src="https://github.com/user-attachments/assets/ee5b64db-8292-4a3c-8d71-6ddac9d19776" />

---

## GTKWave Installation:

GTKWave too comes bundled with OSS-CAD Suite, but this time with the version 3.4.0 which is stable. \
But just to be on the safer side it is recommended to delete the GTKWave files inside the OSS-CAD Suite folder

### Installation:

Directly install GTKWave from the terminal using the following command 

```bash
sudo apt update
sudo apt install gtkwave
```

This installs version 3.3.104 currently.

### Tool Check:

```bash
gtkwave
```

<img width="1007" height="636" alt="GTKWave" src="https://github.com/user-attachments/assets/ccec1605-3b1f-4ef6-a1ca-53ea3d1eb70a" />

---

## Tool Summary

| Tool     | Command              | Installed Version | Working |
|----------|--------------------|-----------------|------|
| Yosys    | `yosys -V`          | 0.57    | ☑️ |
| Iverilog | `iverilog -V`       | 11               | ☑️ |
| GTKWave  | `gtkwave -V` | 3.3.104          | ☑️ |

---

## Notes / Troubleshooting

- Ensure OSS-CAD Suite versions of Iverilog and GTKWave are removed before installing.
- If a command is not found, check that PATH was correctly updated and run `source ~/.bashrc`.
- GTKWave version may differ if installed via OSS-CAD Suite vs `apt`.
