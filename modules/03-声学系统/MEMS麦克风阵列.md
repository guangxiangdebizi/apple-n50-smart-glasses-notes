# MEMS 麦克风阵列 · 波束成形与远场拾音

> **免责声明**：基于公开 MEMS 市场数据与产业链推演，**非苹果官方规格**。

---

## 1. 模块概述

N50 传闻配备 **3–4 颗 MEMS 数字麦克风**，分布于镜框/镜腿，通过**波束成形（Beamforming）**指向佩戴者口部，抑制环境噪声与风噪。该阵列是 Siri 唤醒、通话、Visual Intelligence 语音指令的**前端传感器**，与 iPhone 主麦克风形成「眼镜近场 + 手机补充」协同。

与 TWS 耳机不同，眼镜麦克风**无法贴近嘴角**，阵列算法与物理间距设计难度更高。

---

## 2. N50 传闻规格

| 参数 | 传闻/推演 | 置信度 |
|------|-----------|--------|
| 数量 | **3–4 颗** MEMS | 中 |
| 类型 | 数字 MEMS（PDM/I²S），高 SNR | 中 |
| 算法 | 端侧预处理 + iPhone Neural Engine 协同 | 中 |
| 可能供应商 | **歌尔**、**瑞声 AAC** | 中 |
| 备选 | STMicro、TDK InvenSense（苹果历史备选池） | 低 |

**布局推演**（非官方）：
- 镜腿各 1 颗（左右对称，利于立体声降噪）
- 鼻托/眉心 1–2 颗（缩短与口部等效距离）

---

## 3. 供应商与竞争格局

| 排名 | 厂商 | 2024 消费 MEMS 营收 | 份额（ReportPrime 口径） | 智能眼镜关联 |
|------|------|---------------------|---------------------------|--------------|
| 1 | Knowles → **Syntiant** | ~4.52 亿美元 | ~39% | 2024.12 完成出售；苹果历史供应商 |
| 2 | **歌尔 Goertek** | ~3.90 亿美元 | ~34% | Rox Vision 等参考设计标配自研 MEMS |
| 3 | **瑞声 AAC** | ~3.50 亿美元 | ~30% | 高 SNR 麦；AI 眼镜/机器人/汽车拓展 |
| 4 | STMicroelectronics | ~2.60 亿美元 | ~23%* | 汽车+消费双线 |
| 5 | TDK InvenSense | ~2.25 亿美元 | ~20%* | 低功耗 SmartSound 系列 |

\* 各机构统计口径重叠，合计 >100%，仅作相对量级参考。

**行业变局**：Knowles 退出消费 MEMS 后，**歌尔 + 瑞声 + STM** 将分食高端份额；对 N50 而言，**亚洲双雄**因与扬声器共供应商协同，概率上升。

**产能参考**：歌尔、AAC 在亚太年 MEMS 出货均达**数十亿颗**级别（含手机/TWS/IoT），智能眼镜年需求百万级仅占极小比例，**产能不是瓶颈**。

---

## 4. 供应链逻辑

```
MEMS 晶圆（InvenSense/TDK 等 Fabless 或 IDM）
      ↓
封装测试（歌尔/瑞声/AAC 模组厂）
      ↓
多麦阵列 SMT + 声学测试
      ↓
苹果 DSP 校准（工厂 + 云端模型）
      ↓
iPhone：Apple Intelligence ASR / 通话降噪
```

**关键节点**：
1. **麦间距**决定最低可处理频率，影响波束宽度
2. **防风网 + 腔体阻尼**需与醋酸纤维镜腿共设计
3. **隐私指示灯**逻辑可能联动麦克风激活状态（与摄像头并列）

---

## 5. 厂商优势

### 歌尔
- Meta 智能眼镜长期 MEMS 供货；**VPU 振动拾音**（120–125 μA 低功耗）可作为辅助通道
- 越南等地扩产，分散地缘风险

### 瑞声 AAC
- **高 SNR 麦克风**在 Android 旗舰占比 >60%（2024 年报）
- 与 Qualcomm 联合 ANC/语音参考设计，算法生态成熟
- 垂直整合：同一客户可同时采购 MEMS + 扬声器 + 光波导（虽 N50 无屏）

---

## 6. 前沿未解问题

- **风噪**：骑行/跑步场景下，镜腿位置麦克风的风切声仍是行业痛点
- **远场 SNR**：无屏眼镜缺少「用户靠近设备」交互，需更强远场能力
- **多麦同步**：数字 MEMS 时钟漂移对阵列相位的影响
- **法规**：GDPR/各州法对「默认监听」的限制可能影响唤醒策略

---

## 7. 关键参考数据

| 指标 | 数据 | 来源 |
|------|------|------|
| Knowles 出售消费 MEMS | 2024.12.27 完成，买家 Syntiant | [Knowles IR](https://investor.knowles.com/news/news-details/2024/Knowles-Corporation-Completes-the-Sale-of-Its-Consumer-MEMS-Microphone-Business-to-Syntiant/default.aspx) |
| AAC 高 SNR MEMS | 中高端 Android 占比 >60% YoY | [AAC 2024 年报](https://www1.hkexnews.hk/listedco/listconews/sehk/2025/0428/2025042802876.pdf) |
| 亚太 MEMS 出货 | 占全球 ~68%；歌尔/AAC 各 >70 亿颗/年 | [ReportPrime MEMS](https://www.reportprime.com/mems-microphone-r18097/company) |
| 歌尔 VPU 传感器 | 120–125 μA，辅助语音拾音 | [Goertek CES 2026 声学](https://www.primepublishers.com/goertek-showcases-full-stack-innovations-in-acoustics-and-sensing-at-ces-2026/article_a67717ee-0966-5335-870b-7015b28ae173.html) |

---

## 8. 延伸阅读

- [PortersFiveForce — AAC MEMS 竞争格局](https://portersfiveforce.com/blogs/competitors/aactechnologies)
- [Knowles 2024 年报 — CMM 业务剥离](https://s29.q4cdn.com/538730168/files/doc_financials/2024/ar/2024-Annual-Report.pdf)
- 姊妹模块：[扬声器-开放式定向发声.md](./扬声器-开放式定向发声.md)

---

*模块版本：v1.0 | 2026-05-29*
