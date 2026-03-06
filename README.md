# code-moment-codex-switch

[中文](#中文) | [English](#english)

---

## 中文

`code-moment-codex-switch` 是一个 OpenClaw skill，用来在“代码时刻”自动把任务升级到 Codex 工作台。

### 作用

当任务已经不再是普通聊天，而是进入明显的工程实现阶段时，这个 skill 会把任务切到更适合编码工作的模型与流程。

### 典型触发场景

- 多文件代码修改
- 需要 `build` / `test` / `lint` / 重启前验证
- 前端/后端状态机、路由、组件、接口、配置联动修改
- 需要“改代码 → 构建/测试 → 看结果 → 再修补”的迭代任务
- Dockerfile、docker-compose、nginx、caddy、systemd、CI、构建失败排查

### 主要行为

- 日常普通对话仍留在默认模型
- 编码型重任务自动切到 Codex 工作台
- 遇到 deploy / restart / delete / 鉴权 / 路由改动时，仍保留确认闸门

### 文件

- `SKILL.md`：skill 主定义文件

### 适用目标

适合希望把“普通聊天”和“工程编码”分流处理的 OpenClaw 使用场景。

---

## English

`code-moment-codex-switch` is an OpenClaw skill that upgrades coding-heavy tasks into a Codex workbench flow.

### What it does

When a task moves beyond normal chat and becomes a real engineering task, this skill switches execution to a more coding-focused model and workflow.

### Typical trigger cases

- multi-file code changes
- tasks that require `build` / `test` / `lint` / pre-restart verification
- linked frontend/backend changes across state machines, routing, components, APIs, or configs
- iterative loops such as: modify code → build/test → inspect result → patch again
- Dockerfile, docker-compose, nginx, caddy, systemd, CI, build-failure debugging

### Main behavior

- normal chat remains on the default model
- coding-heavy tasks are upgraded to the Codex workbench
- deploy / restart / delete / auth / routing changes still keep confirmation gates

### Files

- `SKILL.md`: the main skill definition

### Intended use

Best for OpenClaw setups that want to separate general chat work from heavier engineering execution.
