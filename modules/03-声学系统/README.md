# 03 · 声学系统 — 模块索引

> **免责声明**：基于 Bloomberg（Mark Gurman）、产业链推演与公开研报整理，**非苹果官方规格**。N50 声学方案以正式发布为准。

---

## 1. 模块概述

声学系统是 N50「无屏 AI 眼镜」的**人机语音接口**：镜腿内扬声器负责私密听音与 Siri 反馈，3–4 颗 MEMS 麦克风阵列负责远场拾音与波束成形。与 Meta Ray-Ban 类似，N50 不依赖骨传导或入耳式单元，而是采用**开放式定向发声（OWS 类）**，在保持环境感知的同时尽量控制漏音。

在三层算力架构中，声学模块承担：
- **端侧**：唤醒词检测、基础降噪、波束成形预处理
- **iPhone 端**：Apple Intelligence 语音识别与对话推理
- **用户感知**：通话隐私、户外风噪、音乐/导航体验

---

## 2. N50 传闻规格（汇总）

| 子模块 | 传闻规格 | 可能供应商 | 置信度 |
|--------|----------|------------|--------|
| 扬声器 | 镜腿内开放式定向发声；近场听音、低漏音 | 歌尔、瑞声 AAC | 中 |
| 麦克风 | 3–4 颗 MEMS；波束成形；多麦降噪 | 歌尔、瑞声 AAC | 中 |
| 算法 | 端侧 + iPhone 协同；Siri 2.0 / Visual Intelligence | 苹果自研 | 中高 |

---

## 3. 子模块文档

| 文件 | 内容 |
|------|------|
| [扬声器-开放式定向发声.md](./扬声器-开放式定向发声.md) | OWS 原理、LBS/SBS 平台、漏音与隐私 |
| [MEMS麦克风阵列.md](./MEMS麦克风阵列.md) | 多麦布局、SNR、全球 MEMS 格局 |

---

## 4. 供应链逻辑（总览）

```
上游：MEMS 晶圆 / 振膜材料 / 声学仿真 IP
  ↓
中游：歌尔、瑞声（扬声器 + MEMS 模组 + 算法参考设计）
  ↓
苹果：声学腔体 ID、DSP 调音、隐私策略
  ↓
下游：通话 / Siri / 音乐 / 导航 / 第三方 App 音频 API
```

**关键约束**：镜腿内腔体体积极小（需容纳电池、FPC、天线），扬声器与麦克风必须**共用有限空间**且互不干扰；苹果对漏音与风噪的验收标准通常高于消费级 OWS 耳机。

---

## 5. 竞争格局速览

| 厂商 | 角色 | 备注 |
|------|------|------|
| **歌尔 Goertek** | 全球 XR/声学龙头；Meta、Pico 等眼镜声学主力 | CES 2026 发布 SPK 三代、LBS 漏音抑制 |
| **瑞声 AAC** | 高端 MEMS + 智能眼镜扬声器 | 2024 年报明确 AI 眼镜声学量产 |
| **Knowles → Syntiant** | 原高端 MEMS 龙头，2024 年底已剥离消费业务 | 苹果未来或更依赖亚洲供应链 |
| **STM / TDK / Infineon** | 备选 MEMS 供应商 | 汽车/工业线为主 |

---

## 6. 前沿未解问题

- **漏音 vs 响度**：开放式架构在 50 dB 环境噪声下能否稳定唤醒 Siri
- **风噪与骑行场景**：镜腿麦克风位置对风切声的敏感性
- **多设备协同**：眼镜 + AirPods 同时在线时的音频路由策略
- **隐私合规**：欧盟/美国各州对「始终在线麦克风」的法规差异

---

## 7. 关键参考数据

| 指标 | 数值 | 来源 |
|------|------|------|
| 全球 MEMS 麦克风市场（2024） | Knowles ~39%、歌尔 ~34%、AAC ~30%（消费细分，各报告口径不一） | [ReportPrime](https://www.reportprime.com/consumer-mems-microphones-r2981/company) |
| 歌尔 MEMS 年出货 | >70 亿颗（含多下游） | [ReportPrime MEMS](https://www.reportprime.com/mems-microphone-r18097/company) |
| Meta Ray-Ban 重量 | 48–51 g | [Medium 评测](https://medium.com/antaeus-ar/meta-ray-bans-gen-1-vs-gen-2-full-review-and-comparison-7facac116080) |
| AAC AI 眼镜扬声器 | 2024 起多品牌量产 | [AAC 2024 年报 PDF](https://www1.hkexnews.hk/listedco/listconews/sehk/2025/0428/2025042802876.pdf) |

---

## 8. 延伸阅读

- [歌尔 CES 2026 声学发布](https://www.goertek.com/en/content/details15_240100.html)
- [Bloomberg — N50 加速开发](https://www.roadtovr.com/apple-accelerates-smart-glasses-report/)
- 主文档：[苹果N50智能眼镜-硬件与供应链详解.md](../../苹果N50智能眼镜-硬件与供应链详解.md)

---

*模块版本：v1.0 | 2026-05-29*
