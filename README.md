
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

---

## ⚡ 核心物理逻辑：为什么这套系统能打 5 公里？ (Technical Manifesto)

很多勇士会质疑 5km 的可行性。作为架构师，我在此公开本项目的**三大物理支柱**，欢迎全球极客进行链路推算：

### 1. 为什么 5km 还有信号？ (单光子探测)
普通的 CMOS 传感器在 5km 处无法感光，但我们采用 **SPAD (单光子雪崩二极管)**。
* **物理事实：** 只要有一个光子撞击，SPAD 就能产生探测电流。
* **算法加持：** 配合 **TCSPC (时间相关单光子计数)**，我们在 5km 的背景噪声中寻找的是“时间相关性”。即使回波只有几个光子，只要它们符合我们的激光脉冲编码序列，系统就能报警。

### 2. 为什么能精准锁定？ (同轴光路 + MLA)
* **MLA (微透镜阵列):** 我们不使用单一的大透镜，而是使用集成微透镜将 VCSEL 激光束发散角压缩至 **0.5 mrad**。
* **同轴 (Coaxial):** 发射器和接收器共用中心轴线。5km 之外，差之毫秒失之千里。同轴设计确保了我们“看”到的地方就是“光”打到的地方，消除了视差。

### 3. 为什么能防太阳光干扰？ (窄门控技术)
* **纳秒级门控:** 系统只在激光发出的那几个纳秒内开启接收器。
* **窄带滤波:** 配合 850nm 窄带滤光片。
* **结果:** 我们只听“自己发出的回声”，对太阳光和背景噪声免疫。

---

## 🛡️ 勇士行动指南 (Warrior's Call to Action)

由于本项目目前处于 **架构公示阶段 (Arch-Release Phase)**，我直接在 README 中招募：

- **硬件组:** 谁能把概念图里的 SPAD 偏置电路画成 KiCad 原理图？
- **算法组:** 谁能写出第一段针对 ESP32 或 FPGA 的伪随机脉冲相关代码？
- **光学组:** 谁能用 Zemax 仿真一下 MLA 在 5km 处的弥散圆直径？

**请直接在 Issues 中留言，或通过 Pull Request 提交你的改进草图。**

<img width="1408" height="768" alt="反监视" src="https://github.com/user-attachments/assets/2c6b143e-c21a-4375-b177-486da1b5fd37" />

---

## ⚖️ License & Disclaimer (协议与免责)

* **License:** This project is licensed under **CERN-OHL-S v2**. (See the `LICENSE` file for full text).
* **Reciprocity:** If you modify the hardware or firmware, you **MUST** share the improvements under the same license.
* **Disclaimer:** Project Argus is for **privacy defense and educational purposes only**. Users are responsible for complying with local radio and laser safety regulations.

---

## 🔬 Deep Dive: The "Periscope + Cat-Eye" Synergy

<details>
<summary><b>Click to expand the core physics behind 5km detection</b></summary>

### The Fusion of Digital Periscope & Active Cat-Eye Detection

The Physics: A Fusion of Digital Periscope & Active Cat-Eye Detection
The core of Project Argus lies in a lethal combination of two optical principles, upgraded for the 21st century.

1. The "Digital Periscope" Logic (Coaxial Alignment)
Traditional surveillance is passive. Project Argus turns the table by using a Coaxial Optical Path.

The Principle: By aligning the VCSEL emitter and the SPAD detector on the exact same optical axis, we create a "Digital Periscope."

The Advantage: Whatever the system "sees," it is already "aiming" at. At a distance of 5km, even a 0.1-degree misalignment means missing the target by meters. Our coaxial architecture eliminates parallax error entirely, ensuring that the return signal from a tiny drone lens is captured with surgical precision.

2. The "Active Cat-Eye" Logic (Retroreflection)
Every camera lens—whether on a $500 DJI drone or a $10,000 telephoto setup—acts like a cat's eye.

The Phenomenon: When our encoded laser hits a remote CMOS sensor, the light is reflected back directly to the source along the incident path (Retroreflection).

The "Argus" Upgrade: We don't just look for a reflection; we use SPAD (Single-Photon Avalanche Diode) to detect individual photons returning from 5km away. By using TCSPC (Time-Correlated Single Photon Counting), we can identify a hidden lens even if it’s tucked behind a tinted car window or deep in a forest, as long as it has a line of sight.

🚀 Real-World Applications
This isn't just for anti-drone warfare. Because the physics of retroreflection is universal, the PhotonShield can be deployed for:

Privacy Shields for Vehicles: Detecting dashboard cameras or tailing vehicles in real-time.

Industrial Counter-Espionage: Identifying long-range telephoto lenses aiming at sensitive factory floors from distant hills.

Autonomous Perimeter Security: A "set and forget" tile that alerts you the moment any optical sensor "looks" at your property.

</details>

---
