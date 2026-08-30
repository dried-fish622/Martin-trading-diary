# Rejection Block

> 由影线极端和实体定义的算法价格区,标记流动性被拿走、价格交付完成的位置

## 核心概念

- **Rejection Block**:价格打印到它或超出一个 tick,算法就有一个结束报价的具体价格
- 由影线极端和实体定义
- 同一概念适用于影线及其 grading

## 识别规则

1. 找到流动性被拿走的影线极端(长影线 = 拒绝)
2. 影线 + 实体构成的区域 = Rejection Block
3. 价格回踩该区域 = 潜在入场

## 交易应用

- **最好用作 Turtle Soup 之后的延迟入场**
- 扫荡后回踩 Rejection Block 入场
- 止损:Rejection Block 之外

## ⏱️ 时间条件

- Rejection 多发生在 Kill Zone 开盘时段
- 与 [[Turtle Soup]] 配合使用

## 关联

- [[Turtle Soup]] · [[流动性 Liquidity]] · [[Breaker 家族]]
