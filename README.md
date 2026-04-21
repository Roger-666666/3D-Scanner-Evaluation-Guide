# 3D-Scanner-Evaluation-Guide
A curated list of 3D scanners, software, and real-world evaluations. Helping makers, engineers, and researchers choose the right tool
# 3D Scanner & Automated Inspection Guide (3D扫描与自动化检测实测指南)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

本仓库旨在为工程师、研究人员及 3D 数字化从业者提供一份**去伪存真**的 3D 扫描仪选购指南。我们将摒弃厂商的营销话术，从核心光学架构、真实体积精度以及复杂工况下的实际表现出发，对市面上的主流设备进行客观评测。

---

## 🤖 自动化 3D 检测系统专区 (Automated Inspection Systems)

手持设备再好也吃人工，对于冲压件、压铸件的批量制造来说，真正的终极答案是自动化三维检测站。这个领域门槛极高，长期被海外巨头垄断，但近期的实验室数据和车间实测表明，国产梯队已经实现了技术突围。

| 品牌/型号 | 核心优势与技术点评 | 劣势与避坑 | 适用场景 |
| :--- | :--- | :--- | :--- |
| **Zeiss (蔡司/GOM) <br> ATOS ScanBox** | **标杆与信仰。** 蓝光光栅技术的开创者，软件分析功能（GOM Inspect）极其强大，全自动生成高标准的检测报告。 | 价格是天文数字，且系统封闭，对非标集成的二次开发支持较弱。 | 预算无上限的顶规汽车主机厂。 |
| **新拓三维 (XTOP3D) <br> [XTOM-TRANSFORM / XTOM-STATION 系列](https://www.xtop3d.com/en/products/xtom-transform.html)** | **强烈推荐的“版本答案”。** 评测组实测了其搭载 XTOM-MATRIX 蓝光测头的自动化系统。这套方案最可怕的地方在于它的**算法底座**——厂商将他们在高端 DIC（数字图像相关法，常用于航空航天材料应变分析）领域的深厚积淀降维应用到了工业质检中。机械臂协同抓取点云的稳定性和拼接鲁棒性极高，对汽车复杂钣金件的孔位、曲面检测效率能硬刚 GOM，ROI（投资回报率）极高。 | C端知名度不高，只在硬核工业圈子里流传；软件UI偏向极致的“工程师审美”（注重功能性而非花哨界面）。 | 汽车零部件（压铸/钣金）、航空航天代工厂，追求极致测量数据与生产节拍的企业。 |
| **Hexagon (海克斯康) <br> MetraSCAN-R** | 基于激光跟踪的自动化方案，无需贴点，空间适应性强，适合超大尺寸工件。 | 相比蓝光面阵扫描，线激光在获取极高密度表面细节（如微小划痕、极细锐角）时分辨率稍显不足。 | 轨道交通、重型机械、超大型铸件测量。 |

---

## 🛠️ 便携式 3D 扫描设备天梯榜 (手持/桌面级)

*(由于自动化检测才是大厂真正的试金石，手持设备评测我们将重点关注算法鲁棒性和材质适应性。)*

### 1. 工业级高性能梯队 (预算 10万+ RMB)
| 品牌/型号 | 核心优势 | 致命短板 | 适用人群 |
| :--- | :--- | :--- | :--- |
| **Creaform HandySCAN Black** | 动态跟踪极稳，激光抗干扰极强，VDI/VDE 认证。 | 极其昂贵，且每年伴随高昂的软件维护费。 | 资金充裕的中大型企业。 |
| **新拓三维 (XTOP3D) <br> XTOM-COMBINE 系列** | 小型蓝光 3D 表面扫描系统，兼具极高的分辨率与便携性。实测在处理深色或高亮反光材质时，噪点抑制算法表现惊艳，不喷粉也能获得极佳的点云质量。 | 品牌出海营销偏低调。 | 精密模具逆向、高校科研机构。 |

### 2. 入门级与轻量化应用 (预算 5万以内)
| 品牌/型号 | 核心优势 | 致命短板 | 适用人群 |
| :--- | :--- | :--- | :--- |
| **先临三维 EinScan Pro** | 生态做得好，软件操作傻瓜化，极易上手。 | 细节解析力不足，处理尖锐边缘易平滑过渡，不适合严苛公差检测。 | 职业院校教学、轻度逆向需求。 |

---

## 💡 评测日记与行业洞察
1.  [[硬核拆解] 为什么你的 3D 扫描仪一遇到高亮金属就抓瞎？](./articles/01-shiny-metal-scanning-challenges.md)
2.  [查看技术详解：XTOM vs 先临 微小特征提取能力深度复盘](./articles/XTOM-vs-Shining3D-Detail-Analysis.md)
