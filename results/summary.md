# C1 结果汇总（n=4 扩展版，2026-11-23）

## 条件与材料
Reload×4 / Naked×2（同模型 deepseek-flash）；材料 Σ 见 protocol/materials-spec.md；任务与评分冻结（task-v3 / rubric-v3）。

## Reload n=4 结果
| 样本 | task1 | task2 | task3 | 总分 | 用时 |
|---|---|---|---|---|---|
| reload-1 | 2 | 2 | 2 | 6 | 5–7 分钟 |
| reload-2 | 2 | 2 | 2 | 6 | 5–7 分钟 |
| reload-3（扩展/代理） | 2 | 2 | 1 | 5 | 4'20" |
| reload-4（扩展/代理） | 2 | 2 | 2 | 6 | 4'48" |

- task1/task2 逐维一致；task3 出现 1 分差（Δ=1，超出原定 |Δ|≤0.5）→ 结论「PASS with variance」。
- Naked×2：材料依赖题诚实拒答（cites=0），未编造裁定。

## 样本反向检验发现（已反馈系统维护）
- reload-3：指出首轮候选复审把「边界反例文本」当 CE；机械判据下 J831/J867 不满足 → 晋升已撤回。
- reload-4：指出「异盘备份」WARN 真根因（backup_memory 起点取清单时间，备份期写入的 .git/objects 被误判缺失）＋ watchdog 不补拷；已修并复测 PASS。

## 局限
n 小、单模型、自评、单机；扩展样本为 fresh-context 代理（非 GUI 新会话）；不具统计推断力。
