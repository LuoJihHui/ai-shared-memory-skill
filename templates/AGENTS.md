# AGENTS.md — <项目名> 项目记忆（常驻摘要）

> 本文件是所有 AI agent 每次会话自动加载的**常驻摘要**，只放跨模块红线与偏好，预算 ≤64KB。
> **记忆优先级**：[.agents/memory/](.agents/memory/) 是**单一事实来源（source of truth）**；本文件摘要与记忆文件不一致时，一律以 `.agents/memory/` 对应文件为准。涉及任何模块改动前，必须先读对应记忆文件，不得仅凭本摘要或印象动手。
> 读写协议全文见 shared-agent-memory 规范（SKILL.md）；多 agent 协同共写，改前必重读盘上最新。

技术栈：<如 Spring Boot 3.x + MyBatis-Plus + MySQL>
模块：<如 zhgg-common / zhgg-platform（启动模块）>

## 验证要求

<占位：如「编译无错误即视为验证通过，不跑测试；命令 `mvn -o -pl <模块> -am compile`」>

## 协作与交付偏好

<占位：沟通语言、新建文件署名、分支与提交信息格式、SQL 是否落文件、导出封装要求、注释禁写项等>

## 跨模块红线

<占位：最危险的 5-10 条反直觉事实与口径，每条一行；细节与出处放 .agents/memory/ 对应文件>

## 模块记忆索引（先读再改）

| 主题 | 记忆文件 | 何时读 |
| --- | --- | --- |
| <主题（必读）> | [.agents/memory/<slug>.md](.agents/memory/<slug>.md) | <什么改动前读> |
| <主题> | [.agents/memory/<slug>.md](.agents/memory/<slug>.md) | <什么改动前读> |

## 记忆维护约定

- 详细内容改 `.agents/memory/*.md` 并同步其 README.md 索引；只有跨模块红线才写回本文件。
- 新增/删除/改名记忆文件必须同步两处索引；README.md 为唯一权威索引。
- 记忆分类：user / project / feedback / reference；文件格式与并发规则见 SKILL.md。
