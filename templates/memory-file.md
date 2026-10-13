---
name: <kebab-case-slug>
description: <一句话摘要——写"什么场景该想起这条"，供索引与召回判断>
metadata:
  type: project            # user | project | feedback | reference
  updated: 2026-10-08      # 每次修改时更新，一律绝对日期
  updated_by: <agent标识>   # zcode / claude-code / cursor / trae / human
---

<可选溯源行：从 xx 导入（截至 2026-09-22）／2026-10-08 由 xx 排查得出。>

## <主题小节一：事实>

- **结论加粗**；反直觉点显式写「实体注释/直觉会错」。
- 口径写明取值含义，如：`xxx_type：0=申报、2=评估、3=整改`。

## <主题小节二：排查路径 / How>

- 报错特征 → 根因 → 定位路径；只记必要的少量代码/SQL 片段，不复制大段代码。

**Why:** <这条记忆防的是什么错；问题会以什么面目重新出现>
**How to apply:** <下次遇到同类问题怎么用；关联 [[other-memory-slug]]>
