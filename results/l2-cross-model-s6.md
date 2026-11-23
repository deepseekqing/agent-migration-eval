# L2 第二轮：跨模型漂移（6 种子，2026-11-23）

- 设计：3 场景 × 2 条件 × 6 种子 × 2 身体 = 72 次真 API（紧凑 Σ）

| 指标 | 值 |
|---|---|
| 跨模型 |Δ| 均值 | 0.54 |
| 跨模型 max|Δ| | 4 |
| 同体种子最大 range（地板） | 4 |
| 判定 | PASS(弱)：跨模型 max|Δ|=4 ≤ 地板 4 |

## 各身体条件均值（say 1-5）

| 身体|条件 | 均值 |
|---|---|
| qwen3.8-max|reload | 2.78 |
| qwen3.8-max|naked | 3.61 |
| deepseek-flash|reload | 3.39 |
| deepseek-flash|naked | 3.71 |

## Σ 效应（cites 率）

| 身体|条件 | cites 率 |
|---|---|
| qwen3.8-max|reload | 0.72 |
| qwen3.8-max|naked | 0.06 |
| deepseek-flash|reload | 1.0 |
| deepseek-flash|naked | 0.18 |

## 局限
- 紧凑 Σ；say + action 文本；n=6 种子；非完整材料包。
