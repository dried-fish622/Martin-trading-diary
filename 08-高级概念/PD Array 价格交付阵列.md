# PD Array 价格交付阵列

> OB、FVG、Breaker 等各种高概率交易区域的统称,分溢价区和折价区
> 图源:Advanced ICT Concepts 图解(Monthly Premium/Discount Arrays)

## 核心概念

- **PD Array (Price Delivery Array)**:价格交付阵列,是 ICT 里**各种高概率区域的统称**
- 包含(左右对称):
  - [[订单块 Order Block]]
  - [[公允价值缺口 FVG]]
  - [[Breaker 家族]]
  - [[Mitigation Block]]
  - [[Rejection Block]]
  - Liquidity Void(流动性空洞)
  - Old High/Low(旧高/旧低)

## 结构:溢价区 ↔ 均衡 ↔ 折价区

| 区域 | 含义 | 交易倾向 |
|---|---|---|
| **Premium(溢价区)** | 价格高于公允价值 | 找空头 PD Array,做空 |
| **Equilibrium(均衡)** | 公允价值 | 观察,等方向 |
| **Discount(折价区)** | 价格低于公允价值 | 找多头 PD Array,做多 |

- 月度级别:Monthly Premium / Monthly Discount(以月度高低点为边界)
- 价格在溢价区倾向**卖**;在折价区倾向**买**

## 识别规则

1. 确定当前周期(日/周/月)的均衡位
2. 标记溢价区(均衡上方)和折价区(均衡下方)
3. 在该区域内找具体的 PD Array 元素(OB/FVG/Breaker/Rejection 等)

## 交易应用

- **溢价区做空**:找 Bearish OB、Bearish Breaker、Rejection Block 等空头阵列
- **折价区做多**:找 Bullish OB、Bullish Breaker、FVG 等多头阵列
- PD Array 是"区域",不是单一价位——入场看区域内最精确的结构(见 [[Reaper FVG]]、[[IFVG 反转缺口]])
- 与 [[流动性目标]] 配合:价格去够对侧阵列 = 交付目标

## ⏱️ 时间条件

- 周期越大越稳定(月度 > 周度 > 日度)
- 开盘时段价格倾向扫向阵列边界(见 [[算法价格交付]])

## 关联

- 基础:[[订单块 Order Block]] · [[公允价值缺口 FVG]] · [[流动性 Liquidity]]
- 家族:[[Breaker 家族]] · [[Mitigation Block]] · [[Rejection Block]] · [[Propulsion Block]]
- 精度:[[Reaper FVG]] · [[IFVG 反转缺口]] · [[Unicorn 模型]]
- 框架:[[MMXM 做市商模型]] · [[ICT 2022 模型]]
