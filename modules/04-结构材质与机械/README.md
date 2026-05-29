# 04 · 结构材质与机械 — 模块索引

> **免责声明**：基于 Bloomberg、郭明錤、产业链推演整理，**非苹果官方规格**。

---

## 1. 模块概述

结构材质与机械子系统决定 N50 的**佩戴感、耐用性与品牌辨识度**。传闻苹果放弃与 EssilorLuxottica 联名路线，自研 **4 款醋酸纤维（Cellulose Acetate）镜框**，目标重量 **<50 g**，接近普通 Ray-Ban（~45 g）而非「电子头箍」。

该子系统横跨：
- **材料**：意大利 Mazzucchelli 板材
- **加工**：五轴 CNC + 手工抛光（领益智造 / 捷普 Jabil）
- **机械**：钛合金微型铰链 + 穿铰链 FPC（兆威机电 / 长盈精密）
- **人机工程**：鼻托、镜腿弧度、重量分布

---

## 2. N50 传闻规格（汇总）

| 子模块 | 传闻规格 | 可能供应商 | 置信度 |
|--------|----------|------------|--------|
| 镜框材质 | 醋酸纤维 Acetate；4 款造型 | Mazzucchelli 板材 | 中 |
| 加工 | 五轴 CNC + 抛光 | 领益智造、捷普 Jabil | 低–中 |
| 铰链 | 钛合金微型铰链 | 兆威机电、长盈精密 | 低–中 |
| 重量 | **<50 g**（含电子件） | — | 中高 |
| 表面 | 高端质感；多色 | 苹果自研 ID | 中 |

---

## 3. 子模块文档

| 文件 | 内容 |
|------|------|
| [镜框-醋酸纤维Mazzucchelli.md](./镜框-醋酸纤维Mazzucchelli.md) | 板材来源、奢侈品供应链 |
| [CNC加工-领益与捷普.md](./CNC加工-领益与捷普.md) | 五轴加工、EMS 角色 |
| [铰链-钛合金微型铰链.md](./铰链-钛合金微型铰链.md) | MIM/CNC 铰链、FPC 过铰链 |
| [重量与佩戴工程学.md](./重量与佩戴工程学.md) | <50g 约束、竞品对比 |

---

## 4. 供应链逻辑（总览）

```
Mazzucchelli 板材（意大利/中国产）
      ↓
CNC 粗铣 → 滚光 → 手工抛光（领益/捷普/东莞/丹阳集群）
      ↓
钛合金铰链 + FPC 穿铰链（兆威/长盈/专精 MIM 厂）
      ↓
苹果：ID、公差、佩戴模型、Drop Test
      ↓
整机组装（立讯/歌尔 EMS — 见 05 模块）
```

**与 Meta 差异**：Meta 依赖 Ray-Ban 成熟镜框 + EssilorLuxottica 渠道；苹果走**自研 ID + 奢侈品级板材**路线，供应链更分散、品控更难。

---

## 5. 竞争格局速览

| 环节 | 全球/中国地位 | N50 相关 |
|------|---------------|----------|
| 醋酸纤维板材 | Mazzucchelli 为奢侈品级龙头 | 传闻首选 |
| 眼镜 CNC | 中国丹阳/深圳集群占全球大量产能 | 领益等果链跨界 |
| 钛铰链 MIM | 日本 Taisei、中国 Zhongwei 等 | 微型化 ~0.006 g 级 |
| 精密结构件 | 长盈精密：折叠屏铰链 ~14% 全球份额 | 可复用微型铰链能力 |

---

## 6. 前沿未解问题

- **电子件增重 vs <50 g**：双摄像头 + 电池 + 扬声器后的配重设计
- **醋酸纤维热变形**：镜腿内发热对板材尺寸稳定性的影响
- **铰链疲劳**：含 FPC 的铰链开合寿命标准（通常 >1 万次）
- **处方镜片**：是否支持光学镜片定制及渠道

---

## 7. 关键参考数据

| 指标 | 数据 | 来源 |
|------|------|------|
| N50 目标重量 | <50 g | [Road to VR / Gurman](https://www.roadtovr.com/apple-accelerates-smart-glasses-report/) |
| Meta Ray-Ban Gen2 | 48–51 g | [Medium 评测](https://medium.com/antaeus-ar/meta-ray-bans-gen-1-vs-gen-2-full-review-and-comparison-7facac116080) |
| 丹阳眼镜产量 | 年产镜片 >8 亿片，占全国 >50% | [Vocal Media](https://vocal.media/journal/how-china-s-eyewear-supply-chain-fuels-lucrative-d2-c-brands-5x1k3l0faa) |
| 长盈折叠屏铰链份额 | ~14% 全球高端液金铰链 | [BCG Matrix 分析](https://dcfmodeling.com/products/300115sz-bcg-matrix) |

---

## 8. 延伸阅读

- [Mazzucchelli 1849 官网](https://www.mazzucchelli1849.it/pages/frontpage)
- [领益智造 — AI 眼镜/XR 场景](https://www.lingyiitech.com/en/ApplicationScenarios/info_itemid_3416_lcid_29.html)
- 主文档：[苹果N50智能眼镜-硬件与供应链详解.md](../../苹果N50智能眼镜-硬件与供应链详解.md)

---

*模块版本：v1.0 | 2026-05-29*
