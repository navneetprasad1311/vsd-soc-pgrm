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

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys 
sudo apt install make 
sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make 
sudo make install
```

Tool Check:

<img width="774" height="626" alt="Yosys" src="https://github.com/user-attachments/assets/004d1f6e-e1a5-4319-8ad5-10009335cacf" />



## Iverilog Installation:

```bash
sudo apt-get install iverilog
```

Tool Check:

<img width="746" height="1102" alt="Iverilog" src="https://github.com/user-attachments/assets/ee5b64db-8292-4a3c-8d71-6ddac9d19776" />


## GTKWave Installation:

```bash
sudo apt update
sudo apt install gtkwave
```

Tech Check:

<img width="750" height="266" alt="GTKWave" src="https://github.com/user-attachments/assets/2ec7fdc6-54d8-4812-ac74-ce7ecb6bece3" />
<img width="1020" height="654" alt="GTKWaveWindow" src="https://github.com/user-attachments/assets/4b172af1-5a03-4b11-ab22-17a3a0ec9df9" />



