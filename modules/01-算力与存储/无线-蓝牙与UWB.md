# 无线 · 蓝牙与 UWB

---

## 1. 模块概述

N50 与 iPhone 构成 **分层算力系统**，无线链路承担 **音频、通知、压缩视频/特征流、空间锚定**。**蓝牙（BR/EDR + BLE）** 为确定能力；**UWB（Ultra-Wideband）** 为产业链推演，可能延续 **U1 芯片** 生态，实现 **厘米级指向、解锁、Find My 与低延迟伴生体验**。

---

## 2. N50 传闻规格（含置信度）

| 项目 | 传闻/推演 | 置信度 |
|------|-----------|--------|
| 蓝牙 | 标配，与 iPhone 深度配对 | 高 |
| 蓝牙版本 | BLE 5.x / 与 iOS 27 协同（推定） | 中 |
| UWB | 传闻集成，类似 U1 | 中 |
| Wi-Fi 独立上网 | 不主打（依赖 iPhone） | 中高 |
| 音频 | 镜腿开放式扬声器 + 定向麦 | 中 |
| 竞品参考 | Meta 眼镜以蓝牙 + 手机为主 | 高 |

---

## 3. 核心供应商与竞争格局

| 技术 | 主导厂商 | 市场/地位 |
|------|----------|-----------|
| 蓝牙协议栈 | **Apple** 自研 + **Broadcom** 等射频（手机历史） | 眼镜或集成于 SiP |
| UWB 芯片 | **Apple U1/U2**；外供 **Qorvo**、**NXP**、**STMicro** | ST 推 IEEE 802.15.4ab |
| UWB 模组 | **Murata**、**Johanson** 等 | 封装天线一体化 |
| 竞品 | Meta × **Qualcomm** 无线套件 | AR1 集成连接 |

| 全球 UWB 市场 | 2025 **$33.7亿** → 2032 **$101.2亿** | CAGR **16.97%** |

*市场规模：GII Research / 多家机构 2025 估算。*

---

## 4. 供应链逻辑

```
射频 IP（Apple / 授权）→ 晶圆与封测 → SiP 与 N401 合封
    → iPhone（UWB 对端 + A 系列）→ 云端（可选）
```

UWB 若落地，需 **iPhone 15 及以后 U1 设备** 形成网络效应；苹果 **10 亿+活跃设备** 为生态护城河（TNW 2026）。

---

## 5. 厂商优势分析

| 主体 | 优势 |
|------|------|
| **Apple** | AirDrop 指向、Car Key、Find My 已验证 UWB 场景 |
| **Qorvo/NXP** | 汽车数字钥匙带动出货量；IEEE 802.15.4z/ab 兼容 |
| **STMicro** | ST64UWB 支持 802.15.4ab，数百米测距宣传 |
| **Qualcomm（对比）** | 眼镜侧单芯片连接方案成熟，但无苹果级 UWB 生态 |

---

## 6. 前沿未解问题

1. 眼镜 UWB 主要用于 **指向 iPhone** 还是 **镜腿触控手势**？
2. 双摄视频流走 **蓝牙 带宽** 是否足够，抑或 **UWB 仅传控制面**？
3. **功耗**：UWB 常开对 <50g 电池的全日续航影响？
4. 与 **Wi-Fi 7 直连** 传闻是否冲突？
5. 跨境 **射频认证**（中国、欧盟）对 UWB 信道限制？

---

## 7. 关键参考数据

| 指标 | 数值 | 来源 |
|------|------|------|
| 全球 UWB 市场 2025 | **$33.7B** | GII Research |
| 2032 预测 | **$101.2B**，CAGR **16.97%** | 同上 |
| ABI：802.15.4ab | 2030 多数 UWB 车端迁移新标准 | ST 新闻稿引 ABI |
| 可穿戴 UWB | 智能手表→**眼镜/听穿戴** BA 网络 | DataIntelo UWB 模块报告 |
| Qualcomm：AR 功耗时序 | 眼镜 **<1W** vs 手机个位数 W | Indian Express 采访 |
| Gurman：连接方式 | 主要蓝牙，深度 iPhone 同步 | Apfelpatient / Bloomberg |

---

## 8. 延伸阅读

- [GII：UWB 市场预测](https://www.giiresearch.com/report/ires2011825-ultra-wideband-market-by-components-technology.html)
- [STMicro ST64UWB 发布](https://circuitcellar.com/newsletter/stmicroelectronics-propels-new-era-of-uwb-technology/)
- [DataIntelo：UWB 模组与可穿戴](https://dataintelo.com/report/uwb-module-market)
- 主文档 §1.2 三层算力架构

---

*基于公开传闻整理，非苹果官方*
