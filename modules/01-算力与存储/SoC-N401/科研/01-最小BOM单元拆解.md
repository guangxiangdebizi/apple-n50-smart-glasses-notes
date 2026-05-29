# SoC-N401 · 最小 BOM 单元拆解

## 1. 拆解树

```
N401 SiP 模块
├── Logic die（CPU+NE+ISP 逻辑）
│   ├── CPU 双核
│   ├── Neural Engine 4 核
│   ├── ISP 管线（部分逻辑）
│   └── 互联/PMU 数字
├── 模拟/RF（BT 基带等）
├── LPDDR PoP（叠封，见内存模块）
├── eMMC/NAND（若集成，Watch 级 32–64GB）
└── 封测
    ├── Fan-out / SiP 基板
    └── 测试+良率损耗
```

## 2. 单元清单

| 最小单元 | 规格 | 供应商 | 可再拆? |
|----------|------|--------|---------|
| N3E logic die | ~80–120 mm² 估 | TSMC | 是→制程模块 |
| SiP 封测 | Watch 级 16×9 mm 级 | ASE/苹果 | 否 |
| 对标 AR1 | 6nm，~$55 主板价 | Qualcomm | — |
| 对标 S10 AP | Watch 11 ~$23.90 | Apple | — |

## 3. N50 传闻用量

| 单元 | 单副用量 |
|------|---------|
| N401 SiP | 1 |

## 4. 成本锚点

| 锚点 | 参考价 | 来源 |
|------|--------|------|
| AR1 主板 SoC | ~$55 | Wellsenn XR |
| AR1 外售单价 | $50–80 | 产业链访谈 |
| Watch S11 AP | $23.90 @1M | TechInsights |
| Meta 整机 BOM | ~$135 | Counterpoint |

---

*非官方推演 | 2026-05-29*
