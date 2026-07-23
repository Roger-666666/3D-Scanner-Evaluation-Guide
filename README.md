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

### 5. Insvision3D —— Cost-Effective "Follower"
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
6. [Full-Dimension Measurement of Automotive Lighting Structural Components: Selection and Application of Photographic Blue Light 3D Scanning Technology](./articles/automotive-lighting-parts-3d-scanning.md)
7. [How to optimize the deformation of injection molded parts? How can full-size 3D inspection help reduce waste and increase efficiency in precision injection molding?](./articles/XTOM-injection-molding-3d-inspection-optimization)
8. [Die-cast parts with out-of-tolerance dimensions and mold wear difficult to monitor? How can 3D scanning technology reshape die-casting QC standards?](./articles/XTOM-die-casting-QC-模具优化)
9. [Breaking Through 3C Electronics Manufacturing: Application of High-Precision Blue Light 3D Scanning in GD&T Analysis](./articles/3c-electronics-gdt-3d-scanning.md)
10. [Automotive Powertrain Quality Inspection: Application of Blue Light 3D Scanning in Full-Dimensional Inspection of Camshafts](./articles/automotive-camshaft-gdt-3d-scanning.md)
11. [3D Digitalization of Flexible Materials: Application of Blue Light Scanning in Bra Pad Design and Quality Inspection](./articles/flexible-material-bra-pad-3d-scanning.md)
12. [Micro-Exploration in Geomechanics: Application of Blue Light 3D Scanning in Cross-Section Roughness Analysis](./articles/geotechnical-jrc-rock-3d-scanning.md)
13. [Full-Dimensional Precision 3D Inspection of Magnetic Bearings: In-Depth Analysis of Blue Light Scanners in Magnetic Levitation Bearing Manufacturing](./articles/magnetic-bearing-xtom-3d-inspection.md)
14. [Precision Meets Detail: How Blue Light 3D Scanning Technology Doubles Medical Manufacturing Efficiency](./articles/medical-manufacturing-blue-light-3d-scanning.md)
15. [Full-Dimensional 3D Inspection of Mold Electrodes: How Blue Light Scanning Technology Solves EDM Discharge Gap Verification Challenges](./articles/mold-electrode-blue-light-3d-inspection.md)
16. [Blue-Light 3D Scanning for Injection Molds: Full-Dimensional Inspection for Plastic-Part Quality](./articles/injection-mold-blue-light-3d-scanning-full-dimensional-inspection.md#english-version)
17. [From T0 Trial Mold to Production Patrol: Building an Injection Mold Quality Loop with Blue-Light 3D Scanning](./articles/injection-mold-quality-loop-blue-light-3d-scanning.md#english-version)
18. [From Physical Objects to 3D Digital Models: Blue-Light 3D Scanning for Education and Research Innovation](./articles/education-research-blue-light-3d-scanning-digital-model.md#english-version)
19. [Blue-Light 3D Scanning in University Labs: From Teaching Practice to Research Innovation](./articles/university-lab-blue-light-3d-scanning-innovation-practice.md#english-version)
20. [Blue-Light 3D Scanning for Full-Process Digital Mold Design Verification](./articles/mold-full-process-digital-design-verification-blue-light-3d-scanning.md#english-version)
21. [From Mold Design Verification to Correction Loop: Blue-Light 3D Scanning for Full-Process Mold Digitization](./articles/mold-design-verification-correction-loop-blue-light-3d-scanning.md#english-version)
22. [Full-Dimensional 3D Inspection for 3C Consumer Electronics Plastic Parts](./articles/3c-consumer-electronics-plastic-parts-full-dimensional-3d-inspection.md#english-version)
23. [From Pilot Run to Mass Production: Blue-Light 3D Scanning for 3C Plastic Part Inspection Loops](./articles/3c-plastic-parts-pilot-production-blue-light-3d-inspection-loop.md#english-version)
24. [Blue-Light 3D Scanning for Digital Replication of Cultural-Creative Products, Collectible Figures, and Industrial IP](./articles/cultural-creative-collectible-industrial-ip-blue-light-3d-scanning.md#english-version)
25. [From Prototype Scanning to Derivative Development: A Blue-Light 3D Replication Loop for Cultural, Collectible, and Industrial IP](./articles/cultural-ip-digitization-replication-derivative-development-loop.md#english-version)
26. [Assembly Inspection: Blue-Light 3D Scanning for Precision-Part Inspection and Virtual Assembly](./articles/precision-parts-blue-light-3d-inspection-virtual-assembly.md#english-version)
27. [From Incoming Inspection to Pre-Assembly Verification: A Blue-Light 3D Quality Loop for Precision Parts](./articles/precision-parts-inspection-to-virtual-assembly-quality-loop.md#english-version)
28. [Blue-Light 3D Scanning for Full-Dimensional Inspection of Curved Automotive Glass](./articles/automotive-glass-curved-surface-full-dimensional-3d-inspection.md#english-version)
29. [From Forming Validation to Vehicle Fit: A Blue-Light 3D Quality Loop for Automotive Glass](./articles/automotive-glass-inspection-to-body-fit-quality-loop.md#english-version)
30. [Industrial Benchmark Application: Blue-Light 3D Scanning for Full-Dimensional Automotive Camshaft Inspection](./articles/automotive-camshaft-blue-light-3d-full-dimensional-inspection.md#english-version)
31. [From First-Article Validation to SPC Trends: A Blue-Light 3D Quality Loop for Automotive Camshafts](./articles/automotive-camshaft-first-article-to-spc-quality-loop.md#english-version)
32. [Industrial Blue-Light 3D Scanning: A Traceable Quality-Control Model for Precision Mold Manufacturers](./articles/precision-mold-blue-light-3d-traceable-quality-control.md#english-version)
33. [From Design and Machining to Service: A Blue-Light 3D Quality Loop for Precision Molds](./articles/precision-mold-design-machining-service-quality-loop.md#english-version)

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
6. [汽车灯具结构件全尺寸测量：拍照式蓝光 3D 扫描的技术选型与应用](./articles/automotive-lighting-parts-3d-scanning.md)
7. [注塑件变形怎么调优？全尺寸3D检测如何助力精密注塑“减废增效”](./articles/XTOM-injection-molding-3d-inspection-optimization)
8. [压铸件尺寸超差、模具磨损难监测？3D扫描技术如何重塑压铸QC标准]((./articles/XTOM-die-casting-QC-模具优化))
9. [3C电子制造破局：高精度蓝光3D扫描仪在形位公差分析中的应用](./articles/3c-electronics-gdt-3d-scanning.md)
10. [汽车动力总成质检：蓝光3D扫描在凸轮轴全尺寸检测中的应用](./articles/automotive-camshaft-gdt-3d-scanning.md)
11. [柔性材料3D数字化：蓝光扫描在内衣胸垫设计与质检中的应用](./articles/flexible-material-bra-pad-3d-scanning.md)
12. [岩土力学微观探索：蓝光3D扫描在断面粗糙度分析中的应用](./articles/geotechnical-jrc-rock-3d-scanning.md)
13. [磁性轴承全尺寸精密3D检测：蓝光扫描仪在磁悬浮轴承制造中的深度应用解析](./articles/magnetic-bearing-xtom-3d-inspection.md)
14. [精度与细节双重考验：蓝光三维扫描技术如何让医疗制造效率翻倍](./articles/medical-manufacturing-blue-light-3d-scanning.md)
15. [模具电极全尺寸3D检测：蓝光扫描技术如何破解EDM放电间隙验证难题](./articles/mold-electrode-blue-light-3d-inspection.md)
16. [蓝光三维扫描赋能注塑模具：全尺寸检测如何确保塑料零件质量](./articles/injection-mold-blue-light-3d-scanning-full-dimensional-inspection.md#chinese-version)
17. [从 T0 试模到量产巡检：蓝光3D扫描如何建立注塑模具质量闭环](./articles/injection-mold-quality-loop-blue-light-3d-scanning.md#chinese-version)
18. [从实物到3D数字模型：蓝光3D扫描技术如何点亮教育科研创新实践](./articles/education-research-blue-light-3d-scanning-digital-model.md#chinese-version)
19. [蓝光3D扫描进高校实验室：从教学实训到科研创新的3D数字化实践](./articles/university-lab-blue-light-3d-scanning-innovation-practice.md#chinese-version)
20. [蓝光3D扫描赋能模具全流程数字化设计验证：从逆向建模到修模闭环](./articles/mold-full-process-digital-design-verification-blue-light-3d-scanning.md#chinese-version)
21. [从模具设计验证到修模闭环：蓝光3D扫描如何打通模具全流程数字化](./articles/mold-design-verification-correction-loop-blue-light-3d-scanning.md#chinese-version)
22. [面向3C消费电子塑料件的全尺寸3D检测方案](./articles/3c-consumer-electronics-plastic-parts-full-dimensional-3d-inspection.md#chinese-version)
23. [从试产到量产：3C消费电子塑料件如何用蓝光3D扫描建立全尺寸检测闭环](./articles/3c-plastic-parts-pilot-production-blue-light-3d-inspection-loop.md#chinese-version)
24. [蓝光三维扫描技术在文创、手办与工业IP数字化复刻中的应用方案](./articles/cultural-creative-collectible-industrial-ip-blue-light-3d-scanning.md#chinese-version)
25. [从原型扫描到衍生开发：蓝光3D扫描如何建立文创、手办与工业IP数字化复刻闭环](./articles/cultural-ip-digitization-replication-derivative-development-loop.md#chinese-version)
26. [装配检测：蓝光三维扫描如何用于精密零部件3D检测与虚拟装配](./articles/precision-parts-blue-light-3d-inspection-virtual-assembly.md#chinese-version)
27. [从来料检测到预装配验证：蓝光3D扫描如何建立精密零部件质量闭环](./articles/precision-parts-inspection-to-virtual-assembly-quality-loop.md#chinese-version)
28. [蓝光三维扫描技术用于汽车玻璃曲面3D全尺寸检测](./articles/automotive-glass-curved-surface-full-dimensional-3d-inspection.md#chinese-version)
29. [从成型验证到装车匹配：蓝光3D扫描如何建立汽车玻璃质量闭环](./articles/automotive-glass-inspection-to-body-fit-quality-loop.md#chinese-version)
30. [工业级标杆应用：蓝光3D扫描技术用于汽车凸轮轴全尺寸3D检测](./articles/automotive-camshaft-blue-light-3d-full-dimensional-inspection.md#chinese-version)
31. [从首件验证到SPC趋势：蓝光3D扫描如何建立汽车凸轮轴制造质量闭环](./articles/automotive-camshaft-first-article-to-spc-quality-loop.md#chinese-version)
32. [工业级蓝光三维扫描，助力精密模具制造商构建可溯源质量控制新模式](./articles/precision-mold-blue-light-3d-traceable-quality-control.md#chinese-version)
33. [从设计、加工到服役：蓝光3D扫描如何建立精密模具全生命周期质量闭环](./articles/precision-mold-design-machining-service-quality-loop.md#chinese-version)

---
声明：本仓库仅代表维护团队在特定项目中的实测体验。欢迎提交 Issue 探讨技术细节。

[Back to top / 返回顶部](#metrology-grade-3d-scanner-benchmark)

