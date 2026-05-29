# 无线-蓝牙与UWB · 最小 BOM 单元拆解

## 1. 拆解树

```
N50 无线子系统
├── 蓝牙（必选）
│   ├── BT 基带（部分在 N401 die）
│   ├── BT RF 前端 / PA / LNA
│   └── 2.4GHz 天线（镜腿）
├── UWB（传闻）
│   ├── U1/U2 类 die 或模块
│   ├── Qorvo 前端（历史 iPhone）
│   └── UWB 天线
└── 滤波/开关（RF FEM）
```

## 2. 单元清单

| 最小单元 | 规格 | 供应商 | 可再拆? |
|----------|------|--------|---------|
| BT RF 增量 | BLE 5.x | Apple/Broadcom | 部分在 SoC |
| UWB die | ~10 mm² @16nm 级 | Apple | 是 |
| UWB 模组 | 含天线 | Murata/USI | 否 |
| Meta 无线 | WiFi+BT 含 AR1 | Qualcomm | — |

## 3. N50 传闻用量

| 单元 | 用量 |
|------|------|
| BT 链路 | 1 套 |
| UWB（若搭载） | 1 模组 |

## 4. 成本锚点

| 锚点 | 参考 | 来源 |
|------|------|------|
| Apple U1 die | 9.71 mm², 16nm | TechInsights |
| NXP SR150 UWB IC | ~$3.96 @1K | Nextwaves |
| Qorvo DWM3000 模组 | $17–24 | Nextwaves |
| AirTag 整机 BOM | ~$10 | Boardor |

---

*非官方推演 | 2026-05-29*
