# 制程 · 台积电 3nm / N4P（N3E）

---

## 1. 模块概述

N401 传闻采用 **台积电 3nm 家族（N3E）或 N4P（增强 4nm）**，将 Watch 世代从 **4nm（S9/S10）** 推升至先进节点，以换取更低漏电与更强 Neural Engine 能效。制程选择直接决定 **晶圆成本、产能排队与亚利桑那 Fab 分工**。

---

## 2. N50 传闻规格（含置信度）

| 项目 | 传闻/推演 | 置信度 |
|------|-----------|--------|
| 节点 | N3E（3nm）优先；N4P 为备选 | 中 |
| 对比 Watch S10 | 从 4nm → 3nm 换代 | 中 |
| 封装 | 延续 Fan-out / SiP（非 CoWoS） | 中 |
| 美国制造比例 | 部分 Watch SiP 已在 AZ Fab 21 | 低–中 |
| 晶圆成本 | N3 单片约 $20k+ 量级 | 中（行业估算） |

---

## 3. 核心供应商与竞争格局

| 公司 | 先进制程地位 | 2025–2026 数据要点 |
|------|--------------|-------------------|
| **TSMC** | 全球代工约 **70.4%**（4Q25） | N3 产能约 16–17.5 万片/月 |
| **Samsung** | 3nm GAA 外供有限 | 代工份额约 11.5% |
| **Intel** | 18A 追赶中 | 外部客户仍少 |
| **SMIC** | 成熟/部分 7nm 以下 | 份额约 5.7%，难进苹果供应链 |

*N3 节点 <7nm 市占：TSMC >90%（Counterpoint  cited by CapitalFlows）。*

---

## 4. 供应链逻辑

```
原材料/设备（ASML EUV、东京电子）→ TSMC Fab 18（台南）/ Fab 15B
    → 苹果测试芯片 → 量产晶圆 → 苹果封测（台湾/越南/美国）
    → N401 SiP → EMS
```

**苹果在 N3 队列优先级极高**（与 NVIDIA、高通争产能）；眼镜芯片出货量远低于 iPhone，但 **tape-out 窗口仍受 52–104 周交期约束**（Silicon Analysts 2026）。

---

## 5. 厂商优势分析

| 主体 | 优势 |
|------|------|
| **TSMC** | N3E HVM 成熟；Fab 18 八期扩产至 20 万片/月（2026） |
| **Apple** | 长期产能协议 + 多产品分摊折旧 |
| **Samsung（对比）** | 价格可能更低，但苹果历史未采用三星先进代工 |

---

## 6. 前沿未解问题

1. N401 使用 **N3B 还是 N3E**（能效/成本差异显著）？
2. 亚利桑那 **Fab 2（3nm）2027 HVM** 是否分担 N401？
3. 3nm **涨价 15%（2026H2）** 对眼镜 BOM 敏感度？
4. 2nm（N2）已预订至 2028，眼镜 Gen2 是否直接跳过 N3？
5. 地缘政治下 **美国制造比例** 对出口合规的影响？

---

## 7. 关键参考数据

| 指标 | 数值 | 来源 |
|------|------|------|
| 4Q25 全球代工份额 | TSMC **70.4%** | TrendForce 2026-05 |
| 3nm 月产能（2026Q2） | **16–17.5 万片** | 工商时报 / TrendForce |
| 2026 年底 3nm 产能目标 | **18–20 万片/月** | GlobalSemiResearch |
| 2027 年 3nm 产能 | **25 万片/月**（+5万 Fab15B） | GlobalSemiResearch |
| N3 交期 | **52–104+ 周**，新案暂停 | Silicon Analysts 2026Q1 |
| N3 晶圆定价趋势 | 2026H2 或涨 **≤15%** | TrendForce 2026-05 |
| AZ Fab 21 现状 | N4P，~1 万片/月，S9 SiP | TrendForce / AppleInsider |

---

## 8. 延伸阅读

- [TrendForce：3nm 涨价与产能](https://www.trendforce.com/news/2026/05/27/news-tsmc-reportedly-eyes-up-to-15-3nm-price-hike-in-2h26-further-5-10-seen-in-2027-amid-ai-asic-demand/)
- [Silicon Analysts：N3 产能分配](https://siliconanalysts.com/analysis/foundry-allocation-status-q1-2026)
- [GlobalSemiResearch：3nm 路线图](https://globalsemiresearch.substack.com/p/decoding-tsmcs-advanced-process-roadmap)

---

*基于公开传闻整理，非苹果官方*
