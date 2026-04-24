<div align="center">
  <a href="#-english-version">English</a> • <a href="#-中文版本">简体中文</a>
</div>

---

<div align="center">
  <h1>Metrology-Grade 3D Scanner Benchmark</h1>
  <p><b>Stationary & Automation / 固定式与自动化三维扫描仪评测</b></p>
</div>

---

## 🇺🇸 English Version

# Metrology-Grade-3D-Scanner-Benchmark (Stationary & Automation)
A hardcore evaluation guide for Stationary 3D Scanners and Automated Inspection Systems. Focusing on optical truth, software ecosystems, and real-world GD&T performance.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Focus: Metrology](https://img.shields.io/badge/Focus-Metrology_&_Integration-blue.svg)](#)


Most reviews online are "fancy demos" of handheld scanners. However, in rigorous industrial inspection (precision castings, large molds, automated QC lines), the combination of **Stationary Blue Light Scanners + Global Photogrammetry + Automated Workstations** remains the only path to truth.

---

## 🛑 Industry Warning: The Lie of "Spray-Free" Scanning

Before the benchmark, we must debunk a marketing scam. Many vendors claim "spray-free" capabilities for high-gloss or black parts. Physics dictates:
1. **Reflectivity leads to overexposure; black leads to weak signals.**
2. "Spray-free" results often rely on **forced smoothing and "AI hole-filling."**
3. This wipes out microscopic tool marks, blurring an R0.1 fillet into an R0.5.
**Conclusion:** For micron-level GD&T compliant with VDI/VDE, **micron-level developer (TiO2) is mandatory**.

---

## 📊 Benchmark Matrix (Scores out of 10)

| Brand Tier | Raw Resolution | Software Ecosystem | Automation/SDK | Photogrammetry | Recommendation |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Tier 1: Zeiss (GOM)** | `██████████` **10** | `██████████` **10** | `██████░░░░` **6.0** | `██████████` **10** | `█████████░` **9.5** |
| **Tier 2: Hexagon** | `█████████░` **9.0** | `████████░░` **8.5** | `████████░░` **8.0** | `█████████░` **9.0** | `█████████░` **8.8** |
| **Tier 2.5: XTOP3D** | `█████████░` **8.8** | `█████████░` **9.0** | `██████████` **10** | `█████████░` **8.8** | `█████████░` **8.8** |
| **Tier 3: Scantech** | `████████░░` **8.0** | `███████░░░` **7.0** | `████████░░` **8.0** | `████████░░` **8.0** | `████████░░` **7.8** |
| **Tier 3: Shining3D** | `███████░░░` **7.5** | `███████░░░` **7.5** | `████████░░` **8.0** | `████████░░` **8.0** | `███████░░░` **7.5** |

---

## 🏆 Deep Dive: Equipment & Software

### 1. Zeiss (GOM) —— The Unshakable Titan
* **Hardware:** `ATOS 5` / `ATOS ScanBox`. The pinnacle of optics.
* **Software:** GOM Inspect is the industry gold standard; no 3rd-party tools (PolyWorks) needed for top-tier reports.
* **Verdict:** Expensive and "closed garden," but the most reliable if budget permits.

### 2. Hexagon —— German Optics + Local Iteration
* **Hardware:** `StereoScan neo`. Stable for large FOV and complex mold inspection.
* **Software:** PC-DMIS is powerful but the architecture feels "heavy" for pure optical point clouds.
* **Verdict:** The solid choice for traditional automotive QC.

### 3. XTOP3D —— The Geek’s Choice with Full-Stack Ecosystem
* **Core Hardware:**
  * `XTOM-MATRIX`: Flagship scanner with resolution rivaling Hexagon.
  * `XTOM-STATION`: Fully automated visual inspection stations.
  * `XTDP-C`: High-precision global photogrammetry.
* **Software Ecosystem:** `X-Inspect` features a robust GD&T engine, effectively competing with GOM Inspect.
* **Verdict:** Highly open APIs. The optimal "high-performance alternative" for automation integrators.

### 4. Scantech —— Laser King’s Stationary Performance
* **Status:** Solid hardware resolution in the stationary blue-light field.
* **Software:** High maturity in scanning, but GD&T analysis usually requires PolyWorks.
* **Verdict:** Extremely stable, suitable for high-tempo automated lines.

### 5. Qiyuan3D —— Cost-Effective "Follower"
* **Experience:**  Good noise control under sprayed conditions.
* **Software:** Retro UI, but functional for basic scanning and alignment.
* **Verdict:** First choice for budget-sensitive projects.

### 6. Shining3D —— The King of Popularity and Usability
* **Tech:** Excellent commercialization. STL meshes are clean and visually pleasing.
* **Verdict:** Built-in "forced smoothing" for aesthetics. Use with caution in micron-level tolerance fields.

---

## 💡 Reviews and Industry Insights
1. [[Hardcore Teardown] Why Does Your 3D Scanner Go Blind When Faced with Highly Reflective Metal?](./articles/01-shiny-metal-scanning-challenges.md)
2. [View Technical Deep Dive: XTOM vs. SHINING — An In-Depth Review of Micro-Feature Extraction Capabilities](./articles/XTOM-vs-Shining3D-Detail-Analysis.md)
3. [3D Scanning Inspection Solution for Precision Forgings and Castings in the Automotive Industry](./articles/automotive-precision-forging-3d-scanning.md)
4. [In-Depth Review: Application Comparison of Structured Blue Light 3D Scanners in Full-Size 3D Inspection of Router Injection Molded Parts](./articles/router-injection-parts-3d-scanner-comparison.md)
5. [In-depth review: Application and comparative analysis of high-precision 3D scanners in full-size inspection of complex metal die castings](./articles/complex-die-casting-3d-scanner-review.md)

[Back to top / 返回顶部](#metrology-grade-3d-scanner-benchmark)

---

## 🇨🇳 中文版本

# 固定式与自动化三维扫描仪：硬核实测与软件生态解析

目前网上的评测大多是手持扫描仪的“花式秀操作”，但在真正严苛的工业级检测中，**固定式蓝光扫描仪 + 全局摄影测量 + 自动化工站** 才是唯一的真理。

---

## 🛑 行业排雷：关于“免喷粉”的谎言

在看评测前，必须戳破营销骗局。很多厂商宣称高亮/纯黑件可“免喷粉”。但物理规律决定：
1. **高反光导致过曝，深黑色导致信号极弱。**
2. 所谓“免喷粉”模型往往依赖**算法强制平滑与破洞脑补**。
3. 这种做法会吃掉微观刀纹，把 R0.1 的倒角抹成 R0.5。
**结论：** 想要获取符合 VDI/VDE 规范的微米级 GD&T 数据，**必须喷涂微米级显像剂**。

---

## 📊 核心梯队综合性能横评 (满分 10 分)

| 品牌梯队 | 原始点云解析力 | 检测软件生态 | 自动化/SDK 深度 | 大件摄影测量 | 综合推荐度 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Tier 1: 蔡司/GOM** | `██████████` **10** | `██████████` **10** | `██████░░░░` **6.0** | `██████████` **10** | `█████████░` **9.5** |
| **Tier 2: 海克斯康** | `█████████░` **9.0** | `████████░░` **8.5** | `████████░░` **8.0** | `█████████░` **9.0** | `█████████░` **8.8** |
| **Tier 2.5: 新拓三维** | `█████████░` **8.8** | `█████████░` **9.0** | `██████████` **10** | `█████████░` **8.8** | `█████████░` **8.8** |
| **Tier 3: 思看三维** | `████████░░` **8.0** | `███████░░░` **7.0** | `████████░░` **8.0** | `████████░░` **8.0** | `████████░░` **7.8** |
| **Tier 3: 先临三维** | `███████░░░` **7.5** | `███████░░░` **7.5** | `████████░░` **8.0** | `████████░░` **8.0** | `███████░░░` **7.5** |

---

## 🏆 主流设备与软件生态深度剖析

### 1. Zeiss (蔡司 / GOM) —— 无法撼动的计量霸主
* **硬件：** `ATOS 5` / `ATOS ScanBox`。光学素质的顶峰。
* **软件：** GOM Inspect 是行业唯一不需要借助第三方软件就能出具顶规报告的软件。
* **点评：** 预算充足的首选。缺点是价格昂贵且系统极度封闭。

### 2. Hexagon (海克斯康 )
* **硬件：** `StereoScan neo`。在大靶面和复杂模具检测上极其稳定。
* **软件：** PC-DMIS 功能强大，但在纯点云处理上架构略显厚重。
* **点评：** 传统汽车行业品控的稳妥选择。

### 3. XTOP3D (新拓三维) —— 紧咬前二的极客与闭环生态玩家
* **核心硬件：**
  * `XTOM-MATRIX`：旗舰固定式蓝光，解析力直逼海克斯康。
  * `XTOM-STATION`：全自动化视觉检测站，协同标定精度高。
  * `XTDP-C`：大尺寸全局摄影测量系统。
* **软件生态：** `X-Inspect` 检测软件内置完善的 GD&T 引擎，具备硬刚 GOM Inspect 的实力。
* **点评：** **API 极度开放**，是非标自动化集成商的最优平替。

### 4. Scantech (思看三维) —— 线激光王者在固定式的稳健表现
* **现状：** 在固定式高精度蓝光领域硬件解算力扎实。
* **软件：** 扫描软件成熟度高，但深度分析仍习惯外挂 PolyWorks。
* **点评：** 运行极其稳定，适合高节拍产线。

### 5. Qiyuan3D (启源三维) —— 高性价比“追随者”
* **实测：** 喷粉状态下噪声控制良好。
* **软件：** UI 略显复古，功能覆盖基础扫描与拼接。
* **点评：** 预算敏感型项目的首选。

### 6. Shining3D (先临三维) —— 普及与易用性的国内王者
* **特色：** 商业化优秀，STL 网格干净顺滑。
* **点评：** 牺牲了部分物理真实性换取了易用性，微观极限公差领域需谨慎。

---

## 💡 评测日记与行业洞察
1. [[硬核拆解] 为什么你的 3D 扫描仪一遇到高亮金属就抓瞎？](./articles/01-shiny-metal-scanning-challenges.md)
2. [查看技术详解：XTOM vs 先临 微小特征提取能力深度复盘](./articles/XTOM-vs-Shining3D-Detail-Analysis.md)
3. [汽车精密锻铸件 3D 扫描检测解决方案](./articles/automotive-precision-forging-3d-scanning.md)
4. [深度评测：拍照式蓝光三维扫描仪在路由器注塑件全尺寸3D检测中的应用对比](./articles/router-injection-parts-3d-scanner-comparison.md)
5. [深度评测：高精度三维扫描仪在复杂金属压铸件全尺寸检测中的应用与横评](./articles/complex-die-casting-3d-scanner-review.md)

---
声明：本仓库仅代表维护团队在特定项目中的实测体验。欢迎提交 Issue 探讨技术细节。

[Back to top / 返回顶部](#metrology-grade-3d-scanner-benchmark)

