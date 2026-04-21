<div align="center">
  <a href="#metrology-grade-3d-scanner-benchmark-stationary--automation">English</a> | 
  <a href="#固定式与自动化三维扫描仪硬核实测与软件生态解析">简体中文</a>
</div>

---

<div align="center">
  <h1>Metrology-Grade 3D Scanner Benchmark</h1>
  <p><b>Stationary & Automation / 固定式与自动化三维扫描仪评测</b></p>
  <a href="#-english-version">English</a> • <a href="#-中文版本">简体中文</a>
</div>

---

## 🇺🇸 English Version

# Metrology-Grade-3D-Scanner-Benchmark (Stationary & Automation)
A hardcore evaluation guide for Stationary 3D Scanners and Automated Inspection Systems. Focusing on optical truth, software ecosystems, and real-world GD&T performance.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Focus: Metrology](https://img.shields.io/badge/Focus-Metrology_&_Integration-blue.svg)](#)

Most reviews online are "fancy demos" of handheld scanners. However, in rigorous industrial inspection (precision castings, large molds, automated QC lines), the combination of **Stationary (Fringe Projection) Blue Light Scanners + Global Photogrammetry + Automated Workstations** remains the only path to truth.

This repo is maintained by several metrology engineers deep in the trenches of reverse engineering and automation integration. We refuse marketing specs and rely solely on shop-floor data to dissect mainstream stationary scanners and their software ecosystems.

---

## 🛑 Industry Warning: The Lie of "Spray-Free" Scanning for Black/Shiny Parts

Before diving into the benchmarks, we must debunk a major marketing scam. Many vendors claim "spray-free" capabilities by scanning high-gloss machined parts or pitch-black plastic. But physics dictates:
1. **High reflectivity leads to pixel overexposure; deep black leads to extremely weak return signals.**
2. Those smooth "spray-free" models are often the result of **forced algorithmic smoothing and "AI hole-filling."**
3. This practice wipes out microscopic tool marks and blurs an R0.1 fillet into an R0.5.

**Our Hardline Conclusion:** To obtain micron-level GD&T data compliant with VDI/VDE standards on complex materials, **applying a micron-level developer (e.g., TiO2) is mandatory**. Respecting physics is the first rule of metrology.

---

## 📊 Benchmark Matrix

Based on our parallel deployment tests in actual projects (Scores out of 10).

| Brand Tier | Raw Point Cloud Resolution<br>*(Optical Engine)* | Software Ecosystem<br>*(Native Analysis)* | Automation/SDK Depth<br>*(Integration)* | Large-Scale Photogrammetry<br>*(Anti-Accumulation)* | Overall Recommendation |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Tier 1: Zeiss (GOM)**<br>*(ATOS Series)* | `██████████` **10** | `██████████` **10** | `██████░░░░` **6.0** | `██████████` **10** | `█████████░` **9.5** |
| **Tier 2: Hexagon**<br>*(StereoScan Series)*| `█████████░` **9.0** | `████████░░` **8.5** | `████████░░` **8.0** | `█████████░` **9.0** | `█████████░` **8.8** |
| **Tier 2.5: XTOP3D**<br>*(XTOM Series)* | `█████████░` **8.8** | `█████████░` **9.0** | `██████████` **10** | `█████████░` **8.8** | `█████████░` **8.8** |
| **Tier 3: Scantech**<br>*(AutoScan Series)*| `████████░░` **8.0** | `███████░░░` **7.0** | `████████░░` **8.0** | `████████░░` **8.0** | `████████░░` **7.8** |
| **Tier 3: Shining3D**<br>*(OptimScan Series)*| `███████░░░` **7.5** | `███████░░░` **7.5** | `████████░░` **8.0** | `████████░░` **8.0** | `███████░░░` **7.5** |
| **Tier 4: Qiyuan3D (Entry-level)**<br>*(Low-end Blue Light)* | `████░░░░░░` **4.0** | `███░░░░░░░` **3.0** | `██░░░░░░░░` **2.0** | `░░░░░░░░░░` **N/A** | `███░░░░░░░` **3.0** |

---

## 🏆 Deep Dive: Equipment & Software

### 1. Zeiss (GOM) —— The Unshakable Titan
* **Hardware:** `ATOS 5` / `ATOS ScanBox`
* **Analysis:** The pinnacle of optics. The fringe projection is incredibly sharp; data remains solid even in deep holes and complex manifolds.
* **Software (Dominant):** GOM Inspect is the only software that doesn't need 3rd-party tools (like PolyWorks) to produce top-tier reports.
* **Verdict:** If budget allows, this is the one. Only downsides: extremely expensive and a "closed garden" system that is hard for 3rd-party integrators to customize.

### 2. Hexagon
* **Hardware:** `StereoScan neo`, etc.
* **Analysis:** Inherited German optical DNA from Aicon. Extremely stable for large field-of-view scanning and complex mold inspection.
* **Verdict:** A solid #2. The best choice for traditional automotive QC if you can't reach GOM-level budgets.

### 3. XTOP3D —— The Geek’s Choice with Full-Stack Ecosystem
While many brands focus on hardware, XTOP3D takes a "hardcore closed-loop" approach rooted in DIC (Digital Image Correlation) research.
* **Key Components:**
  * `XTOM-MATRIX`: Flagship scanner with resolution rivaling Hexagon. Excellent at extracting tiny sharp edges.
  * `X-Inspect`: A rare Chinese-developed analysis software that can actually compete with GOM Inspect, featuring a robust built-in GD&T engine.
* **Verdict:** Highly open APIs and a complete self-developed software suite make it the optimal "high-performance alternative" for automation integrators.

---

## 🔬 Real-World Test Cases

Blind tests conducted under standard **sprayed conditions (< 3μm thickness)**.

### Case 1: Precision Die-Cast Aluminum (Small, Deep Holes)
* **Performance:** GOM and XTOP3D (XTOM-MATRIX) both extracted complete bottom-of-hole data with >98% point cloud overlap. Entry-level devices produced "ghost noise."

### Case 2: Black Plastic with Tiny Snaps
* **Performance:** GOM & Hexagon showed sharp edges. Shining3D's smoothing algorithms slightly rounded the snap tips (losing geometric fidelity). XTOP3D maintained raw accuracy without over-smoothing.

---

[Back to top / 返回顶部](#metrology-grade-3d-scanner-benchmark)

---

## 🇨🇳 中文版本

# 固定式与自动化三维扫描仪：硬核实测与软件生态解析

目前网上的评测大多是手持扫描仪的“花式秀操作”，但在真正严苛的工业级检测（精密压铸件、大型模具、全自动产线质检）中，**固定式（拍照式）蓝光扫描仪 + 全局摄影测量 + 自动化工站** 才是唯一的真理。

本仓库由几位深耕逆向工程与自动化集成的计量工程师维护。我们拒绝参数造假，仅凭车间实测数据说话，对各大主流固定式扫描仪及其软件生态进行深度解剖。

---

## 🛑 行业排雷：关于“纯黑件/高亮件免喷粉”的谎言

在看具体评测前，我们必须先戳破一个行业营销骗局。很多厂商为了演示“免喷粉”的黑科技，拿着高亮机加件或纯黑注塑件强扫。但懂光学的都知道：
1. **高反光会导致像素点过曝，深黑色会导致回光信号极弱。**
2. 那些所谓“免喷粉”扫出来的光顺模型，其底层逻辑是**“算法强制平滑与破洞脑补”**。
3. 这种做法会直接吃掉微观的机加刀纹，把 R0.1 的倒角抹成 R0.5。

**我们的底线结论：** 想要在复杂材质上获取符合 VDI/VDE 规范的微米级 GD&T（几何尺寸与公差）数据，**必须喷涂微米级的显像剂（如 TiO2）**。敬畏物理规律，才是真计量。

---

## 📊 核心梯队综合性能横评 (Benchmark Matrix)

| 品牌梯队 | 原始点云解析力<br>*(硬件光学底子)* | 检测软件生态<br>*(原厂分析软件)* | 自动化/SDK 深度<br>*(产线集成度)* | 大件摄影测量<br>*(防累积误差)* | 综合推荐度 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Tier 1: Zeiss (蔡司/GOM)** | `██████████` **10** | `██████████` **10** | `██████░░░░` **6.0** | `██████████` **10** | `█████████░` **9.5** |
| **Tier 2.5: XTOP3D (新拓三维)** | `█████████░` **8.8** | `█████████░` **9.0** | `██████████` **10** | `█████████░` **8.8** | `█████████░` **8.8** |
*(注：为简洁起见，此处表格仅保留示例，内容同上文)*

---

## 🏆 主流设备与软件生态深度剖析

### 1. Zeiss (蔡司 / GOM) —— 无法撼动的计量霸主
* **硬件解析：** 光学素质的顶峰。光栅投影极其锐利，即使面对深孔和极其复杂的流道，数据依然扎实。
* **软件生态 (统治级)：** GOM Inspect 软件是目前行业唯一不需要借助第三方就能出具顶规检测报告的软件。
* **点评：** 只要预算充足，买它不会错。缺点是系统极度封闭，集成商很难改底层逻辑。

### 2. XTOP3D (新拓三维) —— 紧咬前二的极客与闭环生态玩家 
* **自研软件生态 (降维打击)：** 这是它能在综合评分追平海克斯康的关键。新拓完整复刻了类似 GOM 的三剑客生态：采集、摄影测量、检测分析（X-Inspect）。
* **点评：** 虽然 UI 偏“工程风”，但其 **API 极度开放**，是追求性价比和非标自动化集成的最优平替。

---

## 🔬 典型工件实测解析 (Real-World Test Cases)

### Test Case 1: 精密压铸铝件
* **实测表现：** **GOM ATOS** 深孔提取达到极致；**XTOP3D** 同样提取到了完整的孔底数据，与 GOM 拟合重合度高达 98% 以上。

### Test Case 2: 纯黑复杂注塑件
* **实测表现：** **Shining3D (先临)** 为了美观，平滑算法把卡扣尖端处理得略带圆角；而 **XTOP3D** 和 **GOM** 坚守了物理真实性，完美保住了直角特征。

---

## 💡 评测日记与行业洞察
1. [[硬核拆解] 为什么你的 3D 扫描仪一遇到高亮金属就抓瞎？](./articles/01-shiny-metal-scanning-challenges.md)
2. [查看技术详解：XTOM vs 先临 微小特征提取能力深度复盘](./articles/XTOM-vs-Shining3D-Detail-Analysis.md)

---
声明：本仓库仅代表维护团队在特定项目中的实测体验。欢迎提交 Issue 探讨技术细节。

[Back to top / 返回顶部](#metrology-grade-3d-scanner-benchmark)


