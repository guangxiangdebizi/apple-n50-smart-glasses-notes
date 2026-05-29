# 06 · iPhone 配套端

> **免责声明**：基于公开传闻与 iOS/芯片公开规格推演，**非苹果官方文档**。

---

## 模块概述

N50 的「主大脑」在 iPhone：A 系列 Neural Engine 运行 Apple Intelligence，蓝牙/UWB 负责与眼镜低延迟通信，iOS 27 可穿戴框架统一管理配对、权限与多设备路由。无 iPhone 配对，眼镜功能将大幅受限。

---

## N50 传闻规格

| 维度 | 传闻要点 | 置信度 |
|------|---------|--------|
| 最低 iPhone | A17 Pro 及以上（Apple Intelligence 门槛） | 高 |
| 主芯片 | A18/A19 系列 + 16 核 Neural Engine | 中 |
| NE 算力 | ~35 TOPS（A18 Pro 级） | 高 |
| 通信 | 蓝牙 LE + 传闻 UWB（U1/U2 芯片） | 中 |
| 系统 | **iOS 27** 可穿戴框架、Siri 2.0 | 中 |
| 云 | Private Cloud Compute，按需 | 中 |
| 独立蜂窝 | 眼镜端不主打；依赖 iPhone 蜂窝/Wi-Fi | 高 |

---

## 供应商 / 生态格局

| 层级 | 主体 | 说明 |
|------|------|------|
| 芯片 | 苹果 + TSMC 3nm | A 系列自研，NE 16 核 |
| 通信 | 苹果 U1/U2 + Broadcom BT | UWB 精确定位与低延迟 |
| 系统 | 苹果 iOS 27 | 可穿戴 API、隐私框架 |
| AI | Apple Intelligence + Foundation Models | 端侧 3B 级 + 云扩展 |
| 竞品 | Meta AI / Gemini | 云端为主，跨平台 |

---

## 供应链或系统逻辑

```
N50 眼镜 ──BT/UWB──→ iPhone（NE 推理 + iOS 27 框架）
                          ↓
                    Apple Intelligence
                          ↓
              本地响应 / Private Cloud Compute
                          ↓
              音频回传眼镜 OWS / 通知 Watch
```

**系统绑定逻辑**：
1. 眼镜作为 iPhone「传感器延伸」，非 MFi 简单配件
2. Apple ID 统一身份；视觉数据受 App Tracking / 隐私指示灯约束
3. 代际升级：换 iPhone 即可提升 AI 能力，无需换眼镜

---

## 优势分析

- **算力随 phone 升级**：NE 35 TOPS 远超镜端 AR1 公开能力
- **生态复用**：Visual Look Up、翻译、导航、Siri 无需从零构建
- **隐私架构**：PCC + 本地优先，差异化 Meta 云端 Llama 路线
- **开发门槛**：iOS 27 可穿戴 API 可吸引第三方视觉 AI 应用

---

## 前沿未解问题

- iOS 27 可穿戴框架 API 开放程度（是否仅第一方？）
- 非 Pro iPhone 能否获得完整 Visual AI 体验？
- 长时间 NE 满载对 iPhone 续航与发热的用户感知
- 与 Apple Watch 健康/通知的数据仲裁
- Android 用户完全被排除的商业影响

---

## 关键参考数据（附来源）

| 指标 | 数值 | 来源 |
|------|------|------|
| A18 Pro NE | 35 TOPS | [Wikipedia A18](https://en.wikipedia.org/wiki/Apple_A18) |
| M4 NE | 38 TOPS | [Apple Newsroom](https://www.apple.com/newsroom/2024/05/apple-introduces-m4-chip/) |
| Apple Intelligence 门槛 | A17 Pro+ / 8GB RAM | Apple 官方 |
| 端到端 AI 延迟（推演） | <150ms | World Today News |
| N50 2027 出货 | 300–500 万 | 郭明錤 |
| iOS 27 传闻同步 | 2027 与 N50 同期 | Gurman / Logicity |

---

## 延伸阅读

- [Neural Engine 与 Apple Intelligence](./Neural-Engine与Apple-Intelligence.md)
- [蓝牙 UWB 通信链路](./蓝牙UWB通信链路.md)
- [iOS 27 可穿戴框架](./iOS27可穿戴框架.md)
- [00 · 三层算力](../00-产品架构与三层算力/)

---

*模块版本：v1.0 | 2026-05-29*
