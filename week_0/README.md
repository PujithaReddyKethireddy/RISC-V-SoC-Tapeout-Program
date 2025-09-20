# 🖥️ Week 0 — Environment Setup & Tools Installation (Up to GTKWave)

This folder documents my **Week 0 progress** in the **VSD RISC-V SoC Tapeout Program**.  
Focus: Setting up the Linux environment and installing essential open-source EDA tools: **Yosys**, **Icarus Verilog (iverilog)**, and **GTKWave**.

---

## 📌 Week 0 Objectives
- Verify system requirements for VSD tools
- Install Yosys, Icarus Verilog, and GTKWave
- Test installations and document outputs
- Prepare a professional structure for future weeks

---

## 🛠️ System Requirements

| Component | Specification |
|-----------|---------------|
| OS        | Ubuntu 20.04+ |
| RAM       | 6GB           |
| HDD       | 50GB          |
| CPU       | 4 vCPU        |

> Screenshot: `Screenshots/system_check.png`

---

## 🛠️ Tool Installation

### 1. **Yosys**
Steps to install Yosys:
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make (If make is not installed please install it)
sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev 
make config-gcc
make
git submodule update --init --recursive
sudo make install 
yosys -V

```
### 2. **Icarus Verilog**
Steps to install Icarus Verilog:
```bash
sudo apt-get update
sudo apt-get install -y iverilog
iverilog -v

```
### 3. **GTKwave**
Steps to install GTKwave:
```bash

sudo apt-get update
sudo apt install -y gtkwave
gtkwave --version

