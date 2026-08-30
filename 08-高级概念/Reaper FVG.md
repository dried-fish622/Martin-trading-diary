# Reaper FVG

> 精度 PD Array:形成于 Breaker 内部、冲动腿内部的高精度入场区

## 核心概念

- **Reaper**:精度 PD Array,形成于:
  - Breaker 内部
  - 冲动腿内部
  - 看涨在折价区 / 看跌在溢价区
  - 情绪已切换之后
  - 最大扩张腿之前
- 不是普通 FVG,不是供需

## 识别规则

1. 市场结构确认(如 Lower High → Lower Low = 空头延续结构)
2. 结构成立就能当作 Reaper
3. Breaker 只当结构用(不需要价格回测来尊重它)

## 交易应用

- 只做结构成立的方向(多头 Reaper / 空头 Reaper)
- 入场在 Reaper FVG 内部,止损结构外
- 目标:下一个流动性池

## ⏱️ 时间条件

- 情绪切换后、最大扩张腿之前最有效
- 与 [[Kill Zone 交易时段]] 配合

## 关联

- [[Breaker 家族]] · [[公允价值缺口 FVG]] · [[MSS 进阶]]
