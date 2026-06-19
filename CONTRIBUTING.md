感谢你对 **Agent System Prompt** 项目的关注！本仓库致力于建立一个大规模、高质量的 AI System Prompt 库。我们非常欢迎各种形式的贡献。

## 目录

- [目录](#目录)
- [行为准则](#行为准则)
- [如何提出问题](#如何提出问题)
  - [Issue 提交](#issue-提交)
- [如何提交贡献](#如何提交贡献)
  - [基本流程](#基本流程)
- [分支与提交规范](#分支与提交规范)
  - [分支命名](#分支命名)
  - [提交信息格式](#提交信息格式)
  - [目录结构要求](#目录结构要求)
  - [文件规范](#文件规范)
    - [`Coder` - 编程助理](#coder---编程助理)
- [Pull Request 流程](#pull-request-流程)
- [审查与合并](#审查与合并)
  - [审查时间](#审查时间)
  - [合并条件](#合并条件)
  - [被拒绝的可能原因](#被拒绝的可能原因)
- [许可证](#许可证)
- [联系维护者](#联系维护者)

---

## 行为准则

为确保社区友好、专业且富有建设性，所有参与者应遵守以下原则：

- 尊重他人的劳动成果和不同观点。
- 提交的内容应符合本仓库的主题：**AI System Prompt**。
- 确保所有贡献内容不侵犯他人版权，且你有权将其以 **CC BY-SA 4.0** 协议发布。
- 不允许提交恶意、歧视性、违法或低质量的内容。

---

## 如何提出问题

### Issue 提交
如果你在使用本仓库的 Prompt 时，发现 AI 做出了意料之外的操作，或认为有可以优化的地方，**请优先前往 [GitHub 仓库](https://github.com/YingHe01/agent-system-prompt) 提交 Issue**。

> 注意：在 Gitee 中提交的 Issue 可能不会被解决，因为 Gitee 仅作为镜像同步。

提交 Issue 时请尽量包含：
- 问题描述（发生了什么，预期是什么）。
- 复现步骤（使用了哪个 Prompt、在什么环境下）。
- 相关截图或日志（如有）。

---

## 如何提交贡献

如果你认为自己的 Agent System Prompt 足够优秀，欢迎以 **Pull Request (PR)** 的形式作出贡献！

### 基本流程

1. **Fork 本仓库** 到你的账号下。
2. **Clone 你的 Fork** 到本地：
   ```bash
   git clone https://gitee.com/你的用户名/agent-system-prompt.git
   ```
3. **基于 `main` 分支创建新分支**：
   ```bash
   git checkout -b feature/你的功能名称
   ```
   > 请务必基于 `main` 分支创建，不要基于其他分支。
4. **按照目录结构要求** 添加或修改文件（详见下文）。
5. **提交并推送**：
   ```bash
   git add .
   git commit -m "docs: 添加 Coder/xxx 的 System Prompt"
   git push origin feature/你的功能名称
   ```
6. **在 Gitee 上发起 Pull Request**，目标分支选择 `main`。

---

## 分支与提交规范

### 分支命名
- `main` —— 主分支，所有合并的目标分支。
- `feature/xxx` —— 新功能或新 Prompt 的添加。
- `fix/xxx` —— 修复已有 Prompt 的问题。

### 提交信息格式
推荐使用 [Conventional Commits](https://www.conventionalcommits.org/) 规范：
```
<type>(<scope>): <简短描述>

<详细描述（可选）>
```

**Type 类型**：
- `feat` —— 新增一个 Prompt
- `fix` —— 修复 Prompt 的问题
- `docs` —— 仅文档变更
- `style` —— 格式调整（不影响内容）
- `refactor` —— 重构
- `chore` —— 构建或辅助工具变动

**示例**：
```
feat(Coder): 添加 Python 代码审查助理的 System Prompt
```

```
fix(Translator): 修正翻译助理在处理长文本时的指令模糊问题
```

---

### 目录结构要求

所有 Pull Request **必须严格遵循**对应板块的结构要求。

**最外层目录**
```
agent-system-prompt/
├── Coder/          # 编程助理
├── Roll-and-Play/  # 角色扮演（规划中）
├── Writer/         # 写作（规划中）
├── Translator/     # 翻译（规划中）
├── Researcher/     # 研究助手（规划中）
├── Tutor/          # 学习（规划中）
└── .../
```

**二级目录规范**
每个具体 Agent 应以独立文件夹存放：
```
[Type]/
├── [Name-1]/
│   ├── [Name-1].agent.md    # 必需：助理内容
│   ├── [Name-1].env.md      # 可选：环境需求
│   └── [Name-1].info.md     # 可选：介绍信息
├── [Name-2]/
│   └── ...
└── Agent_list.md            # 此板块的 Agent 概览
```

---

### 文件规范

#### `Coder` - 编程助理

**`.agent.md` —— 助理内容（必需）**

该文件包含两部分：

1. Frontmatter 段（YAML 格式）:

    适用于 VS Code，包括以下字段：
    ```yaml
    ---
    name: 助理名称
    description: 简短描述
    argument-hint: 参数提示
    tools: 使用的工具列表
    disable-model-invocation: true/false
    user-invokable: true/false
    agents: 关联的其他 Agent
    ---
    ```
    > 各字段详细说明请参考 [VS Code 官方文档](https://code.visualstudio.com/docs)。

2. Agent Operating Manual 段（Markdown 格式）：

    内容为**精确的、可执行的命令和流程**。应清晰、具体，让 AI 能够准确理解和执行。

**`.env.md` —— 环境需求（可选）**
    列出使用该 Prompt 所需的环境：
   - IDE 及版本（如 Visual Studio Code）
   - 必要的插件
   - 编译与运行环境
   - 其他自备内容

**`.info.md` —— 介绍（可选）**
    包含：
   - 使用方法
   - 构造时间
   - 更改记录

**`Agent_list.md` —— 板块概览**
    每个板块根目录下应包含一个 `Agent_list.md`，列出该板块所有 Agent 的概览及特殊说明。

---

## Pull Request 流程

1. **确保你的 PR 只包含一个独立的功能或修复** —— 不要在一个 PR 中混合多个不相关的更改。
2. **确保所有文件符合上述目录结构和文件规范**。
3. **确保你的 Prompt 内容清晰、可执行、有实际价值**。
4. **在 PR 描述中说明**：
   - 这个 Prompt 的用途是什么。
   - 适用于什么场景。
   - 是否有已知限制或特殊要求。
5. **如果涉及多个文件的更改，请在 PR 中逐一说明**。

---

## 审查与合并

本项目的维护者是 **MiklyWay**。

> 维护者是一名高中生，随时可能因为考试或 OI 竞赛暂停维护。请理解并耐心等待。

### 审查时间
维护者通常将在 **每周三和周日集中审批** Pull Request 和 Issue。

### 合并条件
- 所有文件符合目录结构和文件规范。
- Prompt 内容具有实际价值和可执行性。
- 无版权或合规问题。
- 维护者人工审核通过。

### 被拒绝的可能原因
- 不符合目录结构要求。
- Prompt 内容模糊、不可执行或质量过低。
- 存在版权或合规风险。
- 重复已有内容且无显著改进。

---

## 许可证

本仓库所有内容采用 **知识共享署名-相同方式共享 4.0 国际许可协议（CC BY-SA 4.0）** 进行许可。

这意味着：
- **你可以** —— 自由分享、修改、甚至商业使用本仓库的内容。
- **你必须** —— 注明出处（本仓库），并以相同许可证（CC BY-SA 4.0）发布你的修改版本。

请确保你提交的所有内容都有权以该协议发布。

---

## 联系维护者

如有任何问题，可以通过以下方式联系维护者：

- 邮箱：milkyway1886@foxmail.com

---

**再次感谢你的贡献！**