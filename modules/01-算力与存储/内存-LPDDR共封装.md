# 内存 · LPDDR 共封装（PoP）

---

## 1. 模块概述

眼镜端内存需在 **亚毫米厚度、数百 mW 功耗预算** 内为 ISP 缓冲、系统唤醒与短时推理提供带宽。传闻 N401 采用 **定制低功耗 LPDDR（多为 LPDDR5X）**，以 **Package-on-Package（PoP）** 叠封于 SoC 之上，缩短走线、降低 I/O 翻转功耗——与 Apple Watch SiP 及旗舰手机 PoP 方案同族。

---

## 2. N50 传闻规格（含置信度）

| 项目 | 传闻/推演 | 置信度 |
|------|-----------|--------|
| 类型 | LPDDR5X（或苹果定制 LPDDR5） | 中 |
| 封装 | PoP 与 N401 共封装 | 中 |
| 容量 | 2–4 GB 级（推定，低于 Watch 1GB 或高于？） | 低 |
| 速率 | 6400–8533 MT/s 区间 | 低 |
| 供应商 | **三星、SK海力士** 二供 | 中 |
| 待机策略 | 深度自刷新 + 与 eMMC 协同休眠 | 中 |

*Watch S10 公开为 1GB RAM + 64GB 存储；眼镜双摄管线或需更大 DRAM 池。*

---

## 3. 核心供应商与竞争格局

| 公司 | DRAM 总份额（4Q25） | LPDDR5X 出货份额（估） |
|------|---------------------|------------------------|
| **Samsung** | **36.0–36.6%** | **35–40%** |
| **SK hynix** | **32.1–33.1%** | **35–38%** |
| **Micron** | **~22.9%** | **22–27%** |
| 其他 | CXMT 等 <5% | 难进入苹果 PoP |

*DRAM 份额：TrendForce / Omdia 4Q25；LPDDR5X：DataVagyanik。*

---

## 4. 供应链逻辑

```
硅晶圆（三星/SK/Micron 厂）→ DRAM die 测试 → 苹果/封测厂 PoP 叠封（与 SoC）
    → SiP 模块 → EMS 回流焊 → 整机
```

苹果惯用 **双供应商策略**：三星与 SK 海力士在 iPhone LPDDR 长期轮换；眼镜量级小于手机，但 **定制时序/电压** 仍可能单一主导厂先期独占。

---

## 5. 厂商优势分析

| 主体 | 优势 |
|------|------|
| **Samsung** | 4Q25 重夺 DRAM 第一；LPDDR5X 10.7Gbps 旗舰方案 |
| **SK hynix** | 曾首发 iPhone 16 LPDDR5X；HBM 与 LPDDR 并行研发 |
| **Micron** | 美国 fab，地缘备选；苹果份额通常第三 |
| **Apple** | PoP 布局控制信号完整性；固件级休眠调度 |

---

## 6. 前沿未解问题

1. 眼镜是否采用 **ePOP（DRAM+eMMC 一体）** 进一步省 PCB？
2. 双摄 4K 预录时 **DRAM 带宽瓶颈** 会否迫使降分辨率？
3. **PASR 部分阵列自刷新** 能否将待机压至 <5 mW 级？
4. 2025–2026 **存储涨价周期** 对 N50 BOM 的弹性？
5. 极端低温（冬季户外）对 LPDDR 自刷新的可靠性？

---

## 7. 关键参考数据

| 指标 | 数值 | 来源 |
|------|------|------|
| LPDDR5X 自刷新 | **5–8 mW/GB** | Lexar Enterprise 技术文 |
| LPDDR5X 深睡眠 | **2–4 mW/GB**（4GB≈12–16mW） | 同上 |
| PoP 可穿戴总内存功耗 | **200–500 mW**（活跃子系统） | Lexar 智能眼镜文 |
| LPDDR5X vs LPDDR5 能效 | 约 **20–25%** 改善 | Lexar 功耗指南 |
| 全球 DRAM 4Q25 规模 | **$51.97–53.58B** | MemoryMarket / TrendForce |
| LPDDR 三巨头收入占比 | **93–95%** | DataIntelo LPDDR 报告 |
| BIWIN LPDDR5X 封装 | **12.4×8.2 mm** FBGA | BIWIN 产品页 |

---

## 8. 延伸阅读

- [Lexar：LPDDR5X 功耗指南](https://lexarenterprise.com/lpddr5x-power-consumption-guide/)
- [Lexar：智能眼镜 ePOP 架构](https://lexarenterprise.com/smart-glasses-and-ar-device-memory-requirements-epop5x-for-next-generation-wearable-computing/)
- [TrendForce 4Q25 DRAM 市占](https://www.dramexchange.com/WeeklyResearch/Post/2/12624.html)

---

*基于公开传闻整理，非苹果官方*
