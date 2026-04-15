
# Project Argus: Open-Source Optical Shielding 🛡️

**"If the sky is watching, we are the ones who blink back."**

Project Argus is a decentralized, open-source hardware initiative to build a solid-state optical radar. Our mission is to detect and neutralize intrusive UAV surveillance using the **Cat-eye Retroreflection effect**.



---

## 🛰️ Performance Tiers (性能指标)

We don't just "see" drones; we lock onto their optical souls.

* **🟢 1.0km - 1.5km (The Shield):** Real-time, high-confidence detection of consumer-grade CMOS sensors. Instant lock-on.
* **🟡 1.5km - 3.0km (The Watcher):** Reliable tracking of professional/industrial UAVs using TCSPC algorithms.
* **🔴 3.0km - 5.0km (The Horizon):** Limit detection for early warning against long-range tactical surveillance.

---

## 🛠️ Technical Architecture (技术架构)

This is a **Solid-State Optical Array**. No moving parts, zero CV latency.

* **Emitter:** High-power VCSEL Matrix (850nm) + Integrated Microlens Array (MLA) for ultra-collimated beam-steering.
* **Detector:** SPAD (Single-Photon Avalanche Diode) array with picosecond timing resolution.
* **Logic:** PRN (Pseudo-Random Noise) encoding + Time-Correlated Single Photon Counting (TCSPC) to pull signals out of solar noise.
* **Anti-Surveillance:** Coaxial optical path design allows for immediate laser dazzle/blind once a lens is confirmed.



---

## ⚔️ Call for Warriors (寻找勇士)

We are looking for experts to move from **Architecture** to **Action**:

1.  **Optics Wizards:** Simulation of MLA focal planes and beam divergence at 5km.
2.  **Hardware Hackers:** High-speed PCB design for SPAD quenching circuits and VCSEL drivers.
3.  **Signal Processors:** FPGA/DSP experts to implement real-time TCSPC and noise-floor reduction.
4.  **Embedded Fighters:** ESP32/C++ masters for system integration and telemetry.

---

## 📜 License

This project is licensed under **CERN-OHL-S v2 (Strongly Reciprocal)**. 

**The Rule:** If you use this shield, you share your improvements. No one owns the sky. We keep the defense open, forever.

---

## 🚀 Get Started

1.  Check the `/Hardware` folder for initial schematics.
2.  Read the `/Whitepaper` for the link-budget calculations at 5km.
3.  Join our developer group (Link in DM/Issues).

**"Privacy is a human right. Physics is our weapon."**


# Project Argus 🛡️

## ## 1. 系统概念架构 (System Conceptual Architecture)

这是我们实现 1.5km-5km 梯度防御的**核心物理逻辑**。

![Project Argus Conceptual Schematic](images/conceptual_schematic.png)

### 🧩 核心架构模块解析：
1.  **同轴 VCSEL-MLA 发射端 (Coaxial Emitter):** * 采用 **850nm VCSEL 阵列**，配合集成微透镜 (MLA) 实现超低发散角（<0.5 mrad）。
    * **核心创新：** 发射与接收光轴**完全重合（同轴）**。这消除了 5km 处的视差误差，并实现了“发现即瞄准”。
2.  **SPAD 单光子接收端 (SPAD Receiver):**
    * 使用 **SPAD (单光子雪崩二极管) 阵列**，具有近乎无穷大的增益，专门捕获 5km 处回弹的极微弱光子。
    * **信号路径：** SPAD -> 超高速比较器 -> FPGA (LVDS)。
3.  **FPGA 信号处理核心 (Signal Processing Core):**
    * **TCSPC (时间相关单光子计数) 算法：** 在时间域上对脉冲进行互相关累积，把目标从太阳噪声中“拔”出来。
    * **PRN (伪随机序列) 编码：** 激光不是乱闪，是有密码的，从而实现 5km 链路的身份验证。
<img width="1408" height="768" alt="反监视" src="https://github.com/user-attachments/assets/2c6b143e-c21a-4375-b177-486da1b5fd37" />
