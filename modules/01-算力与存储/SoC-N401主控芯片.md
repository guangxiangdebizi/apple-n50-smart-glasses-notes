# SoC · N401 主控芯片

---

## 1. 模块概述

**N401** 为苹果智能眼镜内部主控代号，传闻基于 **Apple Watch S 系列 SiP** 裁剪魔改：保留双核 CPU + 4 核 Neural Engine 的能效基因，砍掉手表专用模块（如复杂健康传感前端），强化 **双摄像头 ISP 接入、蓝牙/UWB 与始终在线唤醒**。Bloomberg（Mark Gurman）将其定位为「全天佩戴、被动散热」的专用低功耗处理器，而非 iPhone A 系列的缩小版。

---

## 2. N50 传闻规格（含置信度）

| 项目 | 传闻规格 | 置信度 | 依据类型 |
|------|----------|--------|----------|
| 内部代号 | N401 | 高 | Gurman / 供应链汇总 |
| 架构基底 | S10/S9 类 SiP（T8310 系） | 高 | 与 Watch 共用可扩展架构 |
| CPU | 64 位双核 | 中 | Watch S10 公开规格外推 |
| Neural Engine | 4 核（与 S9/S10 同级） | 中 | 端侧唤醒/轻推理 |
| GPU | 单核或极简图形管线 | 低 | Watch 裁剪惯例 |
| SoC 功耗上限 | <2 W | 中高 | 主文档 + 眼镜热设计 |
| 存储 | 与 Watch 类似 eMMC/NAND 集成 | 低 | 无公开容量 |
| 量产窗口 | 2026 末–2027 | 中高 | Gurman 2026-04 报道 |

---

## 3. 核心供应商与竞争格局

| 角色 | 公司 | 份额/地位 | 与 N401 关系 |
|------|------|-----------|--------------|
| 芯片设计 | **Apple** | 100% 自研 | N401 定义方 |
| 晶圆代工 | **TSMC** | 全球先进制程 >90%（<7nm） | 唯一量产代工方（传闻） |
| 竞品平台 | **Qualcomm** AR1/AR1+ Gen 1 | Meta Ray-Ban 主力 | 眼镜专用外售 SoC |
| 竞品平台 | **恒玄 BES2800** 等 | 国产轻量眼镜 | 蓝牙 + 低功耗 ISP |
| 封测/SiP | **日月光 ASE**、苹果自有产线 | 高端 SiP 主导 | Watch SiP 同类工艺 |

*TSMC <7nm 份额：Counterpoint / TrendForce 2025；AR1：Qualcomm 产品简报。*

---

## 4. 供应链逻辑

```
IP/EDA（Synopsys、Cadence）→ TSMC 晶圆 → 苹果后端（封测/SiP）
    → 歌尔/立讯 EMS（SMT+组装）→ 苹果质检 → 零售 + 配对 iPhone
```

苹果对 N401 的控制力极强：**架构复用 Watch 可降低 NRE**，但眼镜双摄与空间链路仍可能触发 **独立 tape-out**（非简单屏蔽层裁剪）。

---

## 5. 厂商优势分析

| 主体 | 优势 |
|------|------|
| **Apple** | Watch 十年低功耗经验；与 iOS/Apple Intelligence 深度绑定；无授权费 |
| **TSMC** | N3E 量产成熟；苹果长期产能合约 |
| **Qualcomm（对比）** | 眼镜参考设计完整、Meta 已验证；但 <1W 平台仍弱于苹果垂直整合 |

---

## 6. 前沿未解问题

1. N401 是否为 **全新 die** 还是 S10 **金属层屏蔽 + 基板重布**？
2. 眼镜端是否集成 **独立 Secure Enclave / U1 协处理器**？
3. 与 iPhone 协同推理时，**Neural Engine 任务划分协议**是否开放给第三方 App？
4. 无屏形态下 **GPU 是否完全移除** 对 SiP 面积与成本的边际收益？
5. 2027 量产是否与 **Vision 产品线争抢 3nm 产能**？

---

## 7. 关键参考数据

| 指标 | 数值 | 来源 |
|------|------|------|
| Watch S10 SiP | 4nm，双核，4 核 NE，64GB 存储 | PhoneDB / Apple Support |
| Watch S9 SiP | 4nm，基于 A16 裁剪架构 | Wccftech 分析 |
| 眼镜 SoC 峰值功耗 | 通常 1–2 W（行业） | Lisleapex 智能眼镜芯片报告 |
| AR1 平台系统功耗 | <1 W | Qualcomm AR1 产品简报 |
| Gurman：N401 基于 Watch | 2026 量产窗口 | Bloomberg 转引 KnowTechie / TNW |
| 智能眼镜市场增速 | 2025 年约 +211%（IDC 转引） | Winbuzzer 2026-04 |

---

## 8. 延伸阅读

- Bloomberg — Mark Gurman《Power On》智能眼镜专题
- [Apple Watch S10 技术规格](https://support.apple.com/en-gb/121202)
- [Qualcomm Snapdragon AR1 Gen 1 产品简报](https://docs.qualcomm.com/doc/87-86507-1/87-86507-1_REV_B_Snapdragon_AR1_Gen_1_Platform_Product_Brief.pdf)
- [Lisleapex 智能眼镜芯片深度报告](https://www.lisleapex.com/solution-ai-smart-glasses-chip-solutions)

---

*基于公开传闻整理，非苹果官方*
