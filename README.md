# *Week 0* VSD RISC-V Tapeout Program ![Week 0](https://img.shields.io/badge/Installation%20of%20Tools-blue?link=https%3A%2F%2Fwww.vlsisystemdesign.com%2Fsoc-labs%2F)

## System Information:
<pre>
OS: Zorin OS 17.3 x86_64 (Ubuntu 22.04 LTS based)
Host: Inspiron 5509 
Kernel: 6.8.0-83-generic 
DE: GNOME 43.9 
Terminal: gnome-terminal 
CPU: 11th Gen Intel i5-1135G7 
GPU: Intel TigerLake-LP GT2 [Iris Xe Graphics] 
Memory: 7669MiB
</pre>
(System Information retrived using `neofetch`)

---

## Yosys Installation:

Download the oss-cad-suite-linux-x64-20250916.tar file from releases page of OSS-CAD-Suite repository \
It contains most of the Open-source tools for ASIC design with the latest updates, including *Yosys*, which we require.

Currently, this is the only effective way to install Yosys, suggested by the contributors themselves. \
Github Link: https://github.com/YosysHQ/oss-cad-suite-build#installation

The following commands are used to completely install Yosys (along with the tools in OSS-CAD-Suite)

```bash
cd ~/Downloads //The place the tar file is downloaded
tar -xvzf oss-cad-suite-linux-x64-20250916.tgz -C ~/Documents/Apps
```
I'll be storing it in `/Documents/Apps` folder, you may change it as per your liking 

```bash
vim ~/.bashrc //you may use gedit instead of vim
export PATH="$HOME/Documents/Apps/oss-cad-suite/bin:$PATH" //in the end of the file
```
then,

```bash
source ~/.bashrc
```
and with that Yosys installation is successfully done ✔️


Tool Check:

<img width="750" height="752" alt="Yosys" src="https://github.com/user-attachments/assets/0dbf43e4-5811-4fb0-a052-7bd51e7a7f5e" />



## Iverilog Installation:

Iverilog comes bundled with the OSS-CAD Suite, but the problem is, it comes with the latest version of 13 which isn't regarded as stable in Iverilog's documentation \
Thus, we have to manually revert back to a stable version. \
This is done by deleting all iverilog files that came bundled with OSS-CAD Suite (using the search function might be helpful) 

Then use the below script to install version 11 of iverilog.

```bash
sudo apt-get install iverilog
```

Tool Check:

<img width="746" height="1102" alt="Iverilog" src="https://github.com/user-attachments/assets/ee5b64db-8292-4a3c-8d71-6ddac9d19776" />


## GTKWave Installation:

GTKWave too comes bundled with OSS-CAD Suite, but this time with the version 3.4.0 which is stable. \
But just to be on the safer side it is recommended to delete the GTKWave files inside the OSS-CAD Suite folder \
and directly install GTKWave from the terminal using the following command 

```bash
sudo apt install gtkwave
```

This installs version 3.3.104 currently.


Tech Check:

<img width="1007" height="636" alt="GTKWave" src="https://github.com/user-attachments/assets/ccec1605-3b1f-4ef6-a1ca-53ea3d1eb70a" />




