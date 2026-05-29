# 03 · 竞品 BOM 与硬件毛利率

> 本章数字 **全部来自 Counterpoint / Wellsenn 公开拆解链路**，非本库估算。

---

## 1. Ray-Ban Meta · 基础版（$299）— Counterpoint（等级 A）

| 项目 | 数值 | 来源 |
|------|------|------|
| 零售价 ASP | **$299** | [Communications Today → Counterpoint](https://www.communicationstoday.co.in/ray-ban-meta-surpasses-1-million-shipments/) |
| 生产成本 BOM | **~$135** | 同上 |
| **硬件毛利率** | **46.5%** | 同上（EssilorLuxottica + Meta） |
| AR1 Gen1 占 BOM | **37.7%** → **~$50.9** | 同上 |
| 机械件 | **13.9%** → **~$18.8** | 同上 |
| 电池 | **5.6%** → **~$7.6** | 同上 |

**推算校验**：135 × (1 − 0.465) = 72.2 ≠ 135 − 135×0.465 = 72.2；ASP−BOM = 164，164/299 = **54.8%**（毛利润额/ASP）。Counterpoint 的 **46.5%** 为其 BoM Service 定义，可能与 ASP 口径（渠道/套装）有关 — **以 Counterpoint 原文为准**。

---

## 2. Wellsenn XR 拆解（等级 B）

### 2.1 综合成本

| 口径 | USD | 来源 |
|------|-----|------|
| BOM | **~$149** | [洞见/首创转 Wellsenn](https://data.djyanbao.com/detail/7003676.html) |
| 含税等综合硬件成本 | **~$164** | 同上 |

### 2.2 分项占比（CMB International 引 Wellsenn，等级 B）

来源：[CMBIGM PDF](https://hk-official.cmbi.info/upload/0eb79424-f9bf-4403-9ce5-024a676b9d7c.pdf)（2025-07-31）

| 成本项 | 占 BOM 比 | 备注 |
|--------|-----------|------|
| **Chips / SoC** | **40–50%** | 高通 AR 平台为主 |
| 结构件 | **~12%** | |
| OEM/组装 | **~9%** | |
| 摄像头 | **~5%** | |
| PCB | **~4%** | |
| 电池 | **~4%** | |
| 声学 | **~3%** | |
| 包装等 | 余量 | Figure 7 饼图 |

### 2.3 分项绝对值（LinkedIn 转 Wellsenn，等级 B）

来源：[LinkedIn / Wellsenn 分项](https://www.linkedin.com/pulse/whats-inside-metas-smart-glasses-closer-look-cost-structure-liu-2gzge)

| 模块 | USD | 占比 |
|------|-----|------|
| 主板+SoC | **$99.1** | 56.95% |
| 充电盒 | **$17.5** | 10.06% |
| 结构件 | **$16.9** | 9.71% |
| OEM 组装 | **$15.0** | 8.62% |
| 传感器 | **$13.0** | 7.47% |
| 声学 | **$5.5** | 3.16% |
| 电源 | **$2.0** | 1.15% |
| 包装 | **$5.0** | 2.87% |
| **合计** | **~$174** | 100% |

---

## 3. 带屏版 Ray-Ban Display（等级 B/C）

| 项目 | 数值 | 来源 |
|------|------|------|
| 零售价 | **$799** | [LinkedIn 产业分析](https://www.linkedin.com/pulse/diffractive-vs-geometric-waveguides-what-manufacturing-chunte-ho-vhlpc) |
| Wellsenn BOM | **~$554** | 同上 |
| 隐含硬件毛利（粗算） | **(799−554)/799 ≈ 30.7%** | **本库算术，非 Meta 披露** |
| 产业评论 | Meta 可能 **接近成本价/亏损** 换生态 | 同上（作者分析，非财报） |

---

## 4. Gen2 定价与毛利空间（等级 C）

| SKU | ASP（公开） | 备注 |
|-----|-------------|------|
| Ray-Ban Meta Gen2 起价 | **$379** | Meta 官网/发布报道 |
| 若 BOM 较 Gen1 +$10–20（推演） | ~$145–155 | 本库 [Meta对比模块](../modules/00-产品架构与三层算力/与Meta-RayBan竞品对比/) |

**Gen2 硬件毛利（算术，等级 D）**：

| BOM 假设 | ASP $379 | 毛利率 |
|----------|----------|--------|
| $135（Gen1 同） | | **42.2%** |
| $149（Wellsenn） | | **39.6%** |
| $155 | | **35.1%** |

---

## 5. 竞品对标结论（有出处部分）

1. **无屏 AI 眼镜** 硬件毛利 **40–55%** 区间有 Counterpoint **46.5%** 锚定。
2. **SoC 占 BOM 约 38–57%**（Counterpoint 37.7% vs Wellsenn 57%）— 计量是否含主板/存储导致差异。
3. **带屏眼镜** BOM 跃升至 **~$554**，毛利显著变薄 — N50 无屏路线避开了这一成本坑（与 Bloomberg 无 waveguide 报道一致）。

---

*2026-05-29*
