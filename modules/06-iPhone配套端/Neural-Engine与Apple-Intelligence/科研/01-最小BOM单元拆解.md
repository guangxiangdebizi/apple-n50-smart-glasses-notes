# Neural Engine · 最小 BOM 单元拆解

> 系统级单元 — **不在眼镜 BOM 内**，用于分摊模型

## 1. 拆解树（iPhone 侧）

```
Apple Intelligence 算力栈
├── A 系列 SoC die（含 16 核 NE）
├── 系统 LPDDR（8GB+ 门槛）
├── 端侧模型权重存储（~3B FM）
├── Core ML / ANE 调度固件
└── Private Cloud Compute（按需，不计入本地 BOM）
```

## 2. 与眼镜交互的最小单元

| 单元 | 角色 |
|------|------|
| NE 推理周期 | 每帧/每请求算力消耗 |
| BT/UWB 接收缓冲 | 特征流 ingress |
| TTS 回传 | 至眼镜 OWS |

## 3. 眼镜侧不计入项

- A18 Pro 整 die（~$50–70 采购推演）
- iPhone 其余 BOM（屏幕、电池等）

---

*非官方 | 2026-05-29*
