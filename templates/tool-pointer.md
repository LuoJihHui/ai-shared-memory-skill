# 各家工具指针接入

> 用法：为你正在用的工具，把对应片段复制到该工具的自动加载入口。**所有片段只含指针，禁止出现记忆正文**（防两处漂移）。

## ZCode / DSH

- 根 `AGENTS.md` 即常驻入口（用 `templates/AGENTS.md`）。
- ZCode 私有项目记忆（`C:\Users\<user>\.zcode\cli\memories\projects\<proj>\memory\MEMORY.md`）只留指针：

```markdown
- 记忆统一在工作区 .agents/memory/，读写都走那里（先读 .agents/memory/README.md 索引）；本目录不放正文
```

## Claude Code

项目根 `CLAUDE.md`：

```markdown
# 记忆入口

本项目记忆的单一事实来源是 .agents/memory/：
- 动手改模块代码前，先读 .agents/memory/README.md 索引，命中即读对应文件；
- 跨模块红线与偏好见根 AGENTS.md（本文件不重复）；
- 两处不一致时，以 .agents/memory/ 对应文件为准；
- 写记忆：一事一文、改前重读盘上最新、同步 README 索引与 frontmatter 的 updated/updated_by。
```

## Cursor

`.cursor/rules/shared-memory.mdc`（旧版 `.cursorrules`）写同款一行指针：

```markdown
本项目记忆的单一事实来源是 .agents/memory/：改模块前先读 .agents/memory/README.md 索引；冲突以 .agents/memory/ 为准；写入遵循其 frontmatter 与索引规范。
```

## Trae

项目记忆（Project Memory）内容配置为指针：

```text
项目记忆统一在工作区 .agents/memory/，先读 README.md 索引；冲突以其为准；写入遵循 SKILL.md 规范。
```

## Codex CLI / Gemini CLI / 其他认 AGENTS.md 的工具

直接复用根 `AGENTS.md`，无需额外文件。

## 支持 skill 机制的工具

把规范 `SKILL.md` 复制（或软链）进该工具的 skills 目录，即成为所有会话可触发的「共享记忆」技能。

## 通用规则

- 指针文件里禁止出现记忆正文。
- 新增工具 = 新增一个指针文件，不动 `.agents/memory/`。
- 工具私有的会话信息（session id 等）不写入共享记忆库。
