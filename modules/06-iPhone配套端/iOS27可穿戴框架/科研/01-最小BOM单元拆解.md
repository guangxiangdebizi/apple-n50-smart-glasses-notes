# iOS 27 · 最小 BOM 单元拆解

> 软件 R&D — 无物理 BOM

## 1. 工程交付单元

```
iOS 27 可穿戴栈
├── Wearables Framework（配对/权限/生命周期）
├── 视觉数据管道（特征 ingress → NE）
├── Siri 2.0 多模态路由
├── 隐私与指示器策略（隐私灯联动）
└── 开发者 API（若开放）
```

## 2. 依赖已有模块

- CoreBluetooth / NearbyInteraction
- Core ML / Apple Intelligence
- AccessorySetupKit

---

*非官方 | 2026-05-29*
