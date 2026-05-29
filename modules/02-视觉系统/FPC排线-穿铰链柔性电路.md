# FPC 排线 · 穿铰链柔性电路

> **非官方说明**：鹏鼎/欣兴为果链 FPC **推测**；N50 铰链穿线方案无专利或供应链实锤公开。

---

## 1. 模块概述

智能眼镜的 **镜框（相机/传感器）** 与 **镜腿（电池、SoC、扬声器）** 必须通过 **柔性印刷电路（FPC）** 在 **铰链** 处互联。N50 传闻采用 **穿铰链 FPC**，是整机 **<50g** 与可靠性的隐形瓶颈：需承受 **数万次动态弯折** 且保证 **MIPI CSI-2** 信号完整性。

---

## 2. N50 传闻规格

| 参数 | 传闻值 | 置信度 |
|------|--------|--------|
| 类型 | 多层 **FPC** / FPCB | 低–中 |
| 路径 | 镜框 ↔ 镜腿，**穿过钛合金微型铰链** | 低 |
| 协议 | 相机 **MIPI**、电源、GPIO（LED） | 中（推演） |
| 供应商 | **鹏鼎**、**欣兴** 等苹果 FPC 供应链 | 低 |
| 层数 | 推测 **6–8 层** 阻抗控制（参考研究原型） | 低 |

---

## 3. 供应商与竞争格局

| 厂商 | 果链地位 | 可穿戴相关 |
|------|----------|------------|
| **鹏鼎控股（Avary）** | 全球 FPC 龙头，iPhone 主力 | 折叠屏、Apple Watch FPC |
| **欣兴电子** | 苹果 HDI/FPC 重要供应商 | 通讯+消费电子 |
| **台郡科技** | FPC 二线 | 价格竞争 |
| **Fumax 等 EMS** | 方案文章：AI 眼镜 FPC **25μm/12.5μm PI**、**LCP** 高频 | [Fumax Tech](https://fumaxtech.com/fpc-solutions-for-ai-glasses-enabling-ultra-slim-design-reliable-electrical-interconnection/) |

**专利参考（非苹果）**：欧洲专利 **EP4187284B1** 描述 **flex-type 铰链 + 中空腔体**，FPC 在腔内 **折叠成环状缓冲**，避免折弯时拉伸/扭转（[TREA 专利摘要](https://trea.com/information/hinge-of-the-flex-type-for-eyeglasses/patentgrant/4e30845d-6575-4af3-a869-78b70225892a)）——与智能眼镜穿线设计高度相关。

---

## 4. 供应链逻辑

```
鹏鼎/欣兴 设计制造 FPC → 与铰链（兆威/长盈等，见 04 结构模块）联合验证
    → 模组厂/EMS 镜框-镜腿总成 → 苹果可靠性测试（动态弯折 + 温湿度）
```

Ray-Ban Meta 拆解显示：**定制异形 FPC** 沿镜腿轮廓走线，拆卸镜腿需加热并避免拉断排线（[Wokoo Teardown](https://wokoodesign.com/Insights/electronics-teardown/ray-ban-meta-teardown/)）。

N50 若采用 **钛合金铰链 + 更窄镜腿**，FPC 弯折半径更苛刻。

---

## 5. 厂商优势（鹏鼎 / 欣兴）

### 鹏鼎

- iPhone 折叠区、主板互连经验可直接迁移。
- 大规模 **阻抗控制、微孔** 能力支撑 MIPI 高速线。

### 欣兴

- 苹果多年合作，与台积电、EMS 协同成熟。
- 高密度互连（HDI）与 FPC 组合供应灵活。

**共同优势**：果链认证、数据保密、与立讯/歌尔 EMS 配套历史。

---

## 6. 前沿未解问题

1. **动态弯折寿命**：AI 眼镜 FPC 可能需 **>10,000–200,000** 次循环（折叠手机上限作参考）。
2. **最小弯折半径**：动态弯折建议 **≥10× 板厚**（0.1mm 板约 **1mm** 半径）（[AllPCB 指南](https://www.allpcb.com/allelectrohub/the-ultimate-guide-to-flexible-pcbs-in-smart-eyewear-materials-design-and-manufacturing)）。
3. **铜箔类型**：**RA 铜** 优于 ED 铜抗疲劳。
4. **铰链内容积**：钛合金铰链内腔能否容纳 **环状缓冲 + 多 lane MIPI**。
5. **维修性**：FPC 断裂即整机返修，用户可维修性几乎为零。

---

## 7. 关键参考数据

| 项目 | 数据 | 来源 |
|------|------|------|
| 动态弯折半径建议 | **≥10× PCB 厚度**（动态） | [AllPCB Smart Eyewear Guide](https://www.allpcb.com/allelectrohub/the-ultimate-guide-to-flexible-pcbs-in-smart-eyewear-materials-design-and-manufacturing) |
| AI 眼镜 FPC 弯折寿命 | 可能 **数万次** 动态弯折 | [Fumax Tech](https://fumaxtech.com/fpc-solutions-for-ai-glasses-enabling-ultra-slim-design-reliable-electrical-interconnection/) |
| 镜腿电子区（研究原型） | **14×56×3mm** | [arXiv 2311.01057](https://arxiv.org/html/2311.01057v3) |
| 折叠手机 FPC 测试 | 最高 **~200,000** 次弯折（行业宣传） | [AllPCB Flex PCB Blog](https://www.allpcb.com/blog/pcb-knowledge/flex-pcbs-unfolded-shape-bending-and-dynamic-applications.html) |
| AI 眼镜增重 | 传感器/显示等常增 **50–100g**（相对普通眼镜） | [Fumax Tech](https://fumaxtech.com/fpc-solutions-for-ai-glasses-enabling-ultra-slim-design-reliable-electrical-interconnection/) |
| N50 重量目标 | **<50g**（整机） | 工作区主文档 §2.4 |

---

## 8. 延伸阅读

- [FPC Solutions for AI Glasses — Fumax](https://fumaxtech.com/fpc-solutions-for-ai-glasses-enabling-ultra-slim-design-reliable-electrical-interconnection/)
- [Flex-type hinge for eyeglasses — EP4187284B1](https://trea.com/information/hinge-of-the-flex-type-for-eyeglasses/patentgrant/4e30845d-6575-4af3-a869-78b70225892a)
- [Ray-Ban Meta Teardown](https://wokoodesign.com/Insights/electronics-teardown/ray-ban-meta-teardown/)

---

*模块版本：v1.0 | 2026-05-29*
