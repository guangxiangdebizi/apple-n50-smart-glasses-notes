# 主摄 CMOS · 索尼（Sony）

> **非官方说明**：N50 主摄传感器型号、像素数均为产业链推演，**无苹果或索尼公开确认**。

---

## 1. 模块概述

主摄是 N50 视觉链的**画质与合规核心**：承担拍照、录像（含空间视频相关说法）、Visual Intelligence 主画面输入。传闻采用 **5–8MP** 量级——显著低于 Ray-Ban Meta 的 **12MP（IMX681）**，体现苹果「**眼镜轻采集、iPhone 重成像**」的产品哲学。

---

## 2. N50 传闻规格

| 参数 | 传闻值 | 置信度 |
|------|--------|--------|
| 有效像素 | **5–8MP** | 中 |
| 画幅比例 | 竖向 **9:16**（适配社交/人像视角） | 中 |
| 动态范围 | **HDR** 多帧合成或片上 HDR | 中 |
| 视频 | 市场有 **4K 录制** 说法（可能经 iPhone 协同或端侧降规格） | 低–中 |
| 供应商 | **索尼** 定制微型 CMOS | 中 |
| 具体型号 | 无公开型号（非 IMX681 级别命名） | 低 |

---

## 3. 供应商与竞争格局

| 厂商 | 地位 / 公开数据 | 与可穿戴关系 |
|------|-----------------|--------------|
| **Sony Semiconductor** | 全球 CIS 龙头；2024–2026 传感器 Capex 约 **9300 亿日元**，约半数投先进制程 | iPhone 主摄长期核心供应商 |
| **Samsung ISOCELL** | 手机端份额高，可穿戴定制较少公开 | 备选，果链历史上少于索尼 |
| **OmniVision** | OV2740/OV5640 等低功耗小型号用于 IoT/可穿戴 | Meta 副摄可见 **OV5675**（5MP） |
| **onsemi** | AR0144 等工业级小型号 | 工业/车载为主 |

**竞品对标（已量产）**：

- Ray-Ban Meta：**IMX681**，12MP，照片 3024×4032，视频 1440×1920@30fps（[官方 Brochure](https://visionsourceshowcase.luxottica.com/wp-content/uploads/Ray-Ban-Meta-Brochure.pdf)）
- 小米 AI 眼镜：亦采用 **IMX681** 12MP（[Camemake](https://www.camemake.com/ar-vr-smartglasses-imx681-xiaomi/)）

---

## 4. 供应链逻辑

```
索尼晶圆/封测（日本/泰国等）
    → 苹果定制规格（滤光片、MIPI lane、功耗帽）
    → 高伟/模组厂 COB/FC 贴装
    → 立讯/歌尔 整机组装
```

索尼在「**小光学尺寸 + 高量子效率 + 低功耗**」上的堆叠工艺（双层/三层堆叠、22nm 逻辑层）是苹果维持 Watch/iPhone 影像领先的关键；N50 传闻定制件可能复用 **手机 ISP 算法链** 的缩小版，而非公开货架 IMX900（工业 3.2MP Global Shutter，封装 **12.0×9.3mm**）。

---

## 5. 厂商优势（为何索尼）

1. **果链历史深度**：iPhone 主摄 CIS 主力，定制协同与 NDA 成熟。
2. **微型化工艺**：2.25µm 级像素、小对角线传感器（如 IMX900 对角 **5.81mm / 1/3.1"**）证明索尼在「小尺寸高性能」上的工程能力（[Sony IMX900](https://www.sony-semicon.com/en/products/is/industry/gs/imx900.html)）。
3. **堆叠与片上 ISP**：三层堆叠、低功耗逻辑层利于 **<2W** 整机功耗预算（传闻）。
4. **隐私与品牌**：高端可穿戴延续「Sony inside」供应链叙事，利于差异化。

---

## 6. 前沿未解问题

1. **5–8MP 是否够用**：Apple Intelligence 识物是否依赖更高像素原图，还是特征图即可？
2. **竖向 9:16 传感器**：需定制光学黑电平/读出顺序，还是标准 4:3 裁切？
3. **4K 传闻真实性**：眼镜端编码功耗 vs 仅传 RAW/HEIF 至 iPhone 合成。
4. **全球快门 vs 卷帘快门**：快速转头/行走时果冻效应与 EIS 分工。
5. **定制 vs 货架 IMX681**：降像素能否把模组厚度压到 **<3mm** 并仍满足苹果画质 bar。

---

## 7. 关键参考数据

| 项目 | 数据 | 来源 |
|------|------|------|
| IMX900 有效像素 | 2064×1552 ≈ **3.2MP** | [Sony Semiconductor IMX900](https://www.sony-semicon.com/en/products/is/industry/gs/imx900.html) |
| IMX900 封装尺寸 | **12.0×9.3mm**（LGA） | 同上 |
| Ray-Ban Meta 主摄 | **12MP**，IMX681 | [Ray-Ban Meta Brochure](https://visionsourceshowcase.luxottica.com/wp-content/uploads/Ray-Ban-Meta-Brochure.pdf) |
| 索尼传感器投资 | 2024–2026 **~9300 亿日元** Capex | [Boardor](https://boardor.com/blog/reconstructing-the-future-of-imaging-sonys-three-layer-stacked-sensor) |
| N50 主摄传闻 | **5–8MP**，9:16，HDR | 工作区主文档 §2.2 |

---

## 8. 延伸阅读

- Sony Semiconductor — 工业/车载 Global Shutter 产品线（微型化参考）
- [Ray-Ban Meta 技术手册 PDF](https://visionsourceshowcase.luxottica.com/wp-content/uploads/Ray-Ban-Meta-Brochure.pdf)
- 主文档：[苹果N50智能眼镜-硬件与供应链详解.md](../../苹果N50智能眼镜-硬件与供应链详解.md)

---

*模块版本：v1.0 | 2026-05-29*
