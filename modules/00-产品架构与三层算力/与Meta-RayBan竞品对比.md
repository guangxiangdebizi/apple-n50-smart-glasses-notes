# 与 Meta Ray-Ban 竞品对比

> **免责声明**：基于公开报道与产业链信息对比，**非官方评测或规格确认**。

---

## 模块概述

Meta Ray-Ban（Gen 2, 2025）是当前 AI 智能眼镜品类的**销量与心智标杆**。N50 与其同属「无屏/轻 AR」路线，但在芯片选型、算力分布、生态绑定上走截然不同的路径。本文件聚焦 Gen 2 音频眼镜线（非 Ray-Ban Display）。

---

## N50 传闻规格 vs Meta Ray-Ban Gen 2

| 维度 | 苹果 N50（传闻） | Meta Ray-Ban Gen 2 |
|------|-----------------|-------------------|
| 主控 | 自研 N401（Watch 系） | 高通 **Snapdragon AR1 Gen 2** |
| 算力分布 | 轻算力在镜端，主 AI 在 iPhone | 镜端 AR1 承担更多端侧 AI |
| 摄像头 | 双摄（主 5–8MP + 副广角） | 3K 升级（Gen 2），12MP 级（AR1 上限） |
| 显示 | 无 | 无（Display 版另计，$799 起） |
| 重量 | 目标 <50g | ~50g 级（Samsung Jinju 参考） |
| 电池 | 镜腿异形软包（ATL/德赛） | Gen 2 宣称**双倍**续航 |
| 连接 | BT + 传闻 UWB | Wi-Fi + BT |
| 平台 | iOS 27，**仅 iPhone** | Meta AI，iOS + Android |
| 镜框 | 自研醋酸纤维 | EssilorLuxottica / Ray-Ban |
| 起价 | $799–$1,299（传闻） | **$379** 起（Gen 2） |
| 上市 | 2027 Q2 量产 | 2025 年 9 月发售 |

---

## 供应商 / 生态格局

| 阵营 | 芯片 | 光学/镜框 | AI | 渠道 |
|------|------|----------|-----|------|
| **苹果 N50** | 自研 N401 | Mazzucchelli 板材 + 果链 | Apple Intelligence | Apple Store + 光学合作（待定） |
| **Meta** | 高通 AR1 | EssilorLuxottica | Meta AI（Llama） | Ray-Ban/Oakley 零售网络 |
| **Android XR** | 高通 AR1 | Warby Parker / Gentle Monster | Gemini | 2026 秋起 |

Counterpoint 称 2025 H2 Meta 全球智能眼镜份额约 **82%**，AI 眼镜占出货 **88%**。

---

## 供应链或系统逻辑

**Meta 路线**：高通 AR1 平台化 → 索尼 IMX681 等标准 CMOS → EssilorLuxottica 一体化眼镜零售 → Meta AI 云端为主、端侧为辅。

**苹果路线**：自研 N401 垂直整合 → 定制索尼 CMOS + 大立光镜头 → 立讯/歌尔 EMS → iPhone NE 本地推理 + 有限上云。

```
Meta：  AR1(镜端AI) ──Wi-Fi/BT──→ Meta Cloud(Llama)
Apple： N401(采集)   ──BT/UWB──→  iPhone NE ──→ Cloud(PCC)
```

---

## 优势分析

### Meta 优势
- **先发**：2023 起量，2025 年 >700 万副，产能目标 2,000 万+/年
- **价格**：$379 起，显著低于苹果传闻定价
- **渠道**：LensCrafters、Sunglass Hut 等光学零售直达
- **跨平台**：Android + iOS 均可配对

### 苹果优势
- **算力**：iPhone NE 35 TOPS >> AR1 公开算力（高通未公布 TOPS）
- **隐私**：Private Cloud Compute + 本地优先策略
- **生态**：与 iPhone/Watch/AirPods 深度联动
- **定制芯片**：N401 可针对 Watch 级功耗极致优化

---

## 前沿未解问题

- Gen 2 已验证「无屏 + AI」市场，苹果 2027 入场是否**晚了两代**？
- Meta 2026 目标产能 2,000 万，苹果 300–500 万首年是否过于保守？
- 高通 AR1 Gen 2 规格未完全公开，与 N401 真实性能差距待验证
- 光学渠道：苹果是否找到 EssilorLuxottica 级合作伙伴？
- Counterpoint 预测 2026/27 起「Meta / Android XR / Apple 三强赛跑」

---

## 关键参考数据（附来源）

| 指标 | 数值 | 来源 |
|------|------|------|
| Meta 2025 销量 | >700 万副 | [CNBC](https://www.cnbc.com/2026/02/11/) |
| Meta 2025 H2 市场份额 | ~82% | [Counterpoint](https://news.futunn.com/en/post/70297707) |
| Ray-Ban Gen 2 起价 | $379 | [The Gadgeteer](https://the-gadgeteer.com/2026/05/25/) |
| 产能目标 2026 | 2,000 万+/年 | [UploadVR](https://www.uploadvr.com/) |
| AR1 Gen1 CPU | 4×1.9GHz | [Qualcomm PDF](https://docs.qualcomm.com/doc/87-86507-1/) |
| N50 2027 出货 | 300–500 万 | 郭明錤 |
| 2025 全球智能眼镜市场 | ~$24.6 亿 | [Grand View Research](https://www.grandviewresearch.com/) |

---

## 延伸阅读

- [三层算力架构](./三层算力架构.md)
- [01 · 算力与存储](../01-算力与存储/) — N401 vs AR1 芯片细节
- [05 · 电源与组装](../05-电源与组装/) — 续航与 EMS 对比
- Bloomberg — Mark Gurman《Power On》
- Fortune India — Counterpoint 三强赛跑分析

---

*模块版本：v1.0 | 2026-05-29*
