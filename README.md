# 简介

此项目的目标是建立一个大规模、高质量的AI Syetem Prompt库。

### 项目连接

https://github.com/MiklyWay0118/Agent_System_Prompt.git 

https://gitee.com/YingHe01/agent-system-prompt.git

### 当前状态

`Code`板块构建中；

`Roll-and-Play`、`Writer`、`Translator`、`Reseacher`、`Tutor`板块规划中。

# 项目结构

### 最外层

```
agent-system-prompt/
├── Code/                   编程
├── Roll-and-Play/          *扮演
├── Writer/                 *写作
├── Translator/             *翻译
├── Reseacher/              *研究
├── Tutor/                  *学习
├── .../
│
└── README.md
```
_注：`*`表示暂无_

### 二级目录

```
[Type]/
├── [Name-1]/
│   ├── [Name-1].agent.md   助理内容
│   ├── [Name-1].env.md     *环境需求
│   └── [Name-1].info.md    *介绍
│
├── [Name-2]/
│   ├── [Name-2].agent.md
│   ├── [Name-2].env.md
│   └── [Name-2].info.md
│
├── .../
│
└── Agent_list.md
```
_注：`*`表示非必须_

# 板块说明

## Code - 编程助理

**适用于 VS Code**

#### `.agent.md` - 助理内容
- **` Frontmatter ` 段：** YAML 格式，包括 ` name, description, argument-hint, tools, disable-model-invocation, user-invocable，agents `。
- **`Agent Operating Manual`段：** Markdown 格式，内容为精确的、可执行的命令和流程。

#### `env.md` - 环境需求
- Visual Studio Code
- - 版本
- - 插件 
- 编译与运行环境
- 额外的自备内容 _非必须_