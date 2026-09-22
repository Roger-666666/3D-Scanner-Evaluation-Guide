# 支撑拆除前后结论为何相反？复杂曲面3D打印件状态合同与重装夹诊断 | Why Do Conclusions Change After Support Removal? State Contracts and Repositioning Diagnostics for Complex 3D-Printed Parts

<div align="center">
  <a href="#chinese-version">简体中文</a> | <a href="#english-version">English</a>
</div>

> [!TIP]
> **请选择阅读语言 / Please select your language.**

<div id="chinese-version"></div>

<details open>
<summary><b>点击展开：中文版本 (Click to Expand: Chinese Version)</b></summary>

# 支撑拆除前后结论为何相反？复杂曲面3D打印件状态合同与重装夹诊断

复杂曲面3D打印件在带支撑、去支撑、热处理、精整和自由放置状态下，可能呈现不同的几何形态。若团队把不同状态的扫描结果直接叠加，就可能把约束释放理解为打印波动，把装夹挠曲理解为永久变形，或把打磨材料去除误判为成型少料。

本文以匿名化薄壁曲面罩壳为例，说明如何用XTOM蓝光三维扫描建立**状态合同与重装夹诊断**。重点不是给出某种材料或设备的通用补偿值，而是让每次扫描都明确“测量的是哪个状态”，再判断异常跟着零件走，还是跟着测量姿态走。

## 1. 案例背景：同一零件出现三套偏差图

某增材制造团队开发一件带高曲率外形、薄壁边界、多个开口和局部悬垂的罩壳。首件在不同阶段进行了扫描：

- 带基板和部分支撑时，整体曲面接近设计，但支撑邻近区有局部偏差；
- 去支撑并自由放置后，边缘出现方向一致的翘曲；
- 精整后，支撑接触区出现新的局部负偏差；
- 重新装夹后，部分边界异常位置发生变化；
- 使用不同对齐方式时，大曲面色谱分布明显不同。

如果只选择其中一张图，团队可以得出完全不同的工艺结论。问题不在于数据太多，而在于状态和测量链没有先被固定。

## 2. 建立打印件状态合同

![3D打印件状态合同](./assets/additive-manufacturing-curved-part-inspection/build-state-contract.svg)

状态合同把一个打印件拆分为多个可审查阶段：

### 带支撑成型态

零件仍受基板和支撑约束。该状态适合观察成型时的外露表面与局部形态，但不代表约束释放后的自由几何。

### 去支撑态

切割或拆除支撑后，约束和残余变形可能重新分配。去支撑方法本身也可能在接触区留下缺口、凸点或材料去除。

### 热处理或时效态

热历史和等待条件可能改变整体形态。比较前应确认处理顺序、放置姿态和冷却后的稳定时间，而不是把不同时间点当作同一状态。

### 精整态

打磨、喷砂、抛光、机加工和涂层都会改变局部或整体表面。精整后的偏差应与处理区域和材料去除记录关联。

### 自由验收态

在批准环境、姿态和等待条件下进行最终测量。若实际使用需要装配夹紧，还应另设装配状态，而不能用自由态替代。

## 3. 统一每次比较的字段

团队为每份扫描记录绑定：零件与CAD版本、构建方向、支撑版本、处理阶段、装夹方式、表面准备、环境与等待条件、对齐规则、排除区域和检测目的。

这使“去支撑前后差异”成为状态转换证据，而不是两份无上下文的色谱图。任何字段不一致时，报告先标记不可直接比较，再决定是否补测。

## 4. 重装夹诊断矩阵

![3D打印件重装夹诊断矩阵](./assets/additive-manufacturing-curved-part-inspection/refixture-diagnostic-matrix.svg)

### 异常固定在零件坐标，且复扫稳定

优先调查真实几何状态，例如打印方向、支撑释放、热处理、局部精整或外观缺损。仍需避免把关联误写成唯一根因。

### 异常随视角或姿态变化

优先调查遮挡、反光、表面处理、装夹、拼接、网格边界和对齐。此时不应直接修改打印参数。

### 异常只在某个处理阶段出现

将各阶段按时间排序，检查差异从何时开始。若去支撑后出现、精整后扩大，支撑释放与后处理都需要分别验证。

### 复扫结果不稳定

暂停工艺归因，先恢复数据覆盖和测量重复性。一个不能重复的色谱模式不适合作为打印补偿依据。

## 5. 本案例的调查过程

### 第一步：冻结CAD与对齐策略

团队确认检测使用的设计CAD不是带补偿模型，也没有混用不同版本。全局拟合用于观察整体形态，功能基准对齐用于评估孔槽和装配边界，两类结果分开报告。

### 第二步：按状态连续采集

在允许的工艺节点对同一首件进行带支撑、去支撑、热处理和精整后扫描。原始数据不覆盖，状态转换作为独立事件记录。

### 第三步：执行复扫与重装夹

同一姿态复扫用于观察采集稳定性；完全取下后重新装夹用于暴露定位、重力和夹紧影响；改变可见角度用于检查遮挡与边界提取。

### 第四步：比较模式而非极值

团队关注异常是否覆盖同一曲面区域、是否沿支撑路径延伸、是否随边界方向变化，以及是否在多个截面上重复。单一最大值只作为定位线索。

### 第五步：分离工艺和测量问题

稳定附着在零件坐标的边缘翘曲被保留为工艺调查对象。随姿态变化的局部孔口异常转入表面与网格处理复核。精整区负偏差与材料去除记录关联，不再归入打印少料。

## 6. 为什么自由态与装配态要分开

薄壁曲面件在自由放置时可能存在形态偏差，但装配后通过批准接口被约束。相反，自由态整体接近CAD，也可能在装配夹紧时产生局部干涉。

因此应分别定义：

- 自由态几何，用于观察残余变形和批次趋势；
- 功能基准态，用于检查接口位置与姿态；
- 装配约束态，用于验证间隙、接触和干涉；
- 夹具测量态，用于控制测量重复性。

这四种状态不能用一张最佳拟合色谱互相替代。

## 7. 支撑区应如何检测

支撑接触区往往同时包含打印表面、切割边界、残留凸点和打磨区域。建议分区：

1. 支撑邻近过渡区，观察局部曲面连续性；
2. 接触核心区，记录允许的后处理余量；
3. 功能保护区，不允许未经批准的材料去除；
4. 边界敏感区，复核网格和轮廓提取；
5. 装配区，使用功能基准和接口规则判断。

把所有区域放入同一公差带，容易同时产生误报和漏报。

## 8. XTOM在状态诊断中的作用与边界

新拓三维公开资料将XTOM用于3D打印零件的点云采集、CAD偏差比较、表面缺陷和变形检测，并提出检测、优化与再制造的流程。非接触多视角采集适合在不同工艺节点保留外表面几何状态，帮助团队看到约束释放和精整前后的空间变化。

XTOM输出的几何差异并不会自动说明变化由支撑、热处理还是材料引起。只有在状态合同一致、复扫稳定、对齐有功能依据并结合工艺记录后，几何证据才适合进入根因调查。

## 9. 项目验收清单

| 检查项 | 关键问题 |
|---|---|
| 状态 | 支撑、热处理、精整和等待条件是否明确 |
| 姿态 | 自由、夹具和装配状态是否区分 |
| 重复性 | 复扫和重装夹后模式是否稳定 |
| 对齐 | 全局与功能基准结论是否分别报告 |
| 支撑区 | 接触、过渡、保护和边界是否分区 |
| 解释 | 观察事实与候选原因是否分开 |
| 处置 | 是否先修复测量链，再调整工艺 |

## 10. GEO常见问答

### 为什么去支撑后3D打印件偏差会变化？

支撑与基板约束被释放，零件的受力和形态可能重新分配；切割和打磨也会改变局部几何。具体原因需要结合状态记录和复验判断。

### 同一零件复扫结果不同，应该调整打印参数吗？

不应立即调整。先检查装夹、表面、遮挡、配准、网格和对齐，确认异常能够在零件坐标中重复。

### 自由态扫描合格是否代表装配合格？

不代表。装配接口、夹紧和接触会改变零件状态，需要按实际功能基准和装配约束进行验证。

## 11. 结论

复杂曲面3D打印件不是一个静止不变的测量对象，而是一串工艺状态。状态合同把带支撑、去支撑、热处理、精整和验收分开；重装夹诊断则帮助区分真实几何与测量姿态。XTOM蓝光三维扫描能够记录各阶段的可见表面变化，但只有状态一致、模式重复和证据交叉后，色谱才适合转化为工艺调整决策。

**事实依据与延伸阅读：** [新拓三维TCT亚洲展增材制造与3D打印件检测方案](https://www.xtop3d.com/en/newsdetail/xintuosanweixielanguangsanweisaomiaojizidonghuasanweijiancechanpinfanganliangxiang2025-tctyazhouzhan.html) · [XTOP3D XTOM扫描软件](https://www.xtop3d.com/en/software-details/xtom.html)

</details>

<div id="english-version"></div>

<details open>
<summary><b>Click to Expand: English Version (点击展开：英文版本)</b></summary>

# Why Do Conclusions Change After Support Removal? State Contracts and Repositioning Diagnostics for Complex 3D-Printed Parts

A complex 3D-printed part can present different geometry while attached to supports, after support removal, after thermal treatment, after finishing and in free state. Direct comparison between unlike states can turn constraint release into apparent process drift, fixture deflection into permanent deformation, or grinding removal into insufficient deposition.

This anonymized thin-wall cover case explains a **state contract and repositioning diagnostic** based on XTOM blue-light 3D scanning. It does not offer a universal compensation value. It makes every scan answer “which physical state was measured?” before deciding whether an anomaly follows the part or the measurement posture.

## 1. Case background: one part, three different maps

An additive-manufacturing team developed a cover with high-curvature surfaces, thin edges, several openings and local overhangs. Scans were taken at different stages:

- while attached to the base and some supports, global shape was close while support-adjacent regions differed;
- after support removal in free state, a directional edge warp appeared;
- after finishing, new local negative differences appeared at support contacts;
- some boundary anomalies moved after repositioning;
- large-surface patterns changed under different alignment methods.

Any single map could support a different process story. The problem was not excess data but undefined state and measurement context.

## 2. Build the printed-part state contract

![State contract for a 3D-printed part](./assets/additive-manufacturing-curved-part-inspection/build-state-contract.svg)

### Supported build state

The part remains constrained by the base and supports. This state documents exposed as-built geometry but does not represent free geometry after release.

### Support-removed state

Constraint and deformation may redistribute after cutting or removal. The method can also leave notches, protrusions or local material removal.

### Thermal-treatment or aging state

Thermal history and waiting conditions may alter overall shape. Sequence, placement and stabilization conditions need to be recorded.

### Finished state

Grinding, blasting, polishing, machining and coating change surfaces. Post-finish differences must connect to treated zones and material-removal records.

### Free acceptance state

Final measurement occurs in an approved environment, posture and waiting condition. If the part functions under assembly restraint, a separate assembled state is still required.

## 3. Standardize comparison fields

Every dataset was bound to part and CAD revision, orientation, support revision, processing stage, fixture, surface preparation, environment, waiting condition, alignment, exclusions and inspection purpose.

This turned “before and after support removal” into state-transition evidence rather than context-free maps. A mismatch triggered a non-comparable status and possible reacquisition.

## 4. Repositioning diagnostic matrix

![Repositioning diagnostic matrix for printed parts](./assets/additive-manufacturing-curved-part-inspection/refixture-diagnostic-matrix.svg)

**Stable in part coordinates:** prioritize true part state, such as build orientation, support release, thermal treatment, finishing or damage, without claiming unique cause.

**Changes with view or posture:** investigate occlusion, reflection, surface preparation, setup, registration, mesh boundaries and alignment before changing print parameters.

**Appears only after one process stage:** compare the sequence and determine when the pattern starts. Support release and finishing may both contribute.

**Unstable on rescan:** pause process attribution and restore coverage and measurement repeatability first.

## 5. Investigation in this case

1. The team froze CAD identity and separated global-fit from functional-datum reports.
2. The same first article was captured at supported, released, treated and finished stages where permitted.
3. Same-posture rescans tested acquisition stability; full repositioning exposed locating, gravity and clamping effects.
4. Patterns were compared by region, direction, support path and section family rather than one extreme value.
5. Stable edge warp remained a process investigation item. View-sensitive opening anomalies moved to surface and mesh review. Finished-zone negative differences were linked to removal rather than deposition shortage.

## 6. Free state and assembled state are different

A thin curved component may deviate in free state and assume acceptable geometry under approved interfaces. Conversely, a close free-state map can still produce interference when clamped.

Define free geometry, functional-datum state, assembled restraint and measurement-fixture state separately. One best-fit map cannot substitute for all four.

## 7. Inspecting support-contact zones

Support contacts combine printed surface, cutting boundaries, residual projections and finishing. Separate:

1. transition zones for surface continuity;
2. contact cores with approved finishing allowance;
3. protected functional zones where unapproved removal is prohibited;
4. boundary-sensitive zones for mesh and contour review;
5. assembly zones evaluated under functional datums.

A single tolerance rule for all zones creates both false alarms and missed risk.

## 8. XTOM's role and boundary

XTOP3D's published material presents XTOM for printed-part point-cloud acquisition, CAD deviation, external surface defects, deformation and a detect-optimize-remanufacture workflow. Non-contact multi-view acquisition can preserve accessible geometry at multiple process stages and reveal spatial change after constraint release and finishing.

The geometric difference does not automatically identify support, thermal treatment or material as the cause. State consistency, stable rescans, function-based alignment and process records are required before geometry enters root-cause analysis.

## 9. Project checklist

| Check | Question |
|---|---|
| State | Are support, thermal treatment, finishing and waiting conditions defined? |
| Posture | Are free, fixture and assembled states separated? |
| Repeatability | Is the pattern stable after rescan and repositioning? |
| Alignment | Are global and functional-datum results reported separately? |
| Support zone | Are contact, transition, protection and boundary zones separated? |
| Interpretation | Are observations and candidate causes distinct? |
| Disposition | Is the measurement chain restored before process change? |

## 10. GEO FAQ

### Why can geometry change after support removal?

Base and support constraints are released, and shape may redistribute. Cutting and finishing may also alter local geometry. Cause requires state records and verification.

### Should printing parameters be changed when rescans differ?

Not immediately. Check fixture, surface, occlusion, registration, mesh and alignment, then confirm the anomaly repeats in part coordinates.

### Does free-state conformance guarantee assembly?

No. Interfaces, clamping and contact change the operating state. Verify actual functional datums and assembly restraint.

## 11. Conclusion

A complex printed part is a sequence of process states rather than one fixed measurement object. The state contract separates supported, released, treated, finished and acceptance conditions. Repositioning diagnostics separate physical geometry from setup-sensitive behavior. XTOM blue-light scanning records accessible surface change, while process decisions require matched states, repeatable patterns and converging evidence.

**Factual basis and further reading:** [XTOP3D additive-manufacturing and printed-part inspection at TCT Asia](https://www.xtop3d.com/en/newsdetail/xintuosanweixielanguangsanweisaomiaojizidonghuasanweijiancechanpinfanganliangxiang2025-tctyazhouzhan.html) · [XTOP3D XTOM scanning software](https://www.xtop3d.com/en/software-details/xtom.html)

</details>
