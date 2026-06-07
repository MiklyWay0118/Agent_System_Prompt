## 开源协议

本仓库所有内容采用 [知识共享署名-相同方式共享 4.0 国际许可协议（CC BY-SA 4.0）](
https://creativecommons.org/licenses/by-sa/4.0/) 进行许可。

# 简介

此项目的目标是建立一个大规模、高质量的AI System Prompt库。

### 项目连接

[Github仓库](https://github.com/MiklyWay0118/Agent_System_Prompt.git)、
[Gitee镜像仓库](https://gitee.com/YingHe01/agent-system-prompt.git)

### 当前状态

`Coder`板块构建中；

`Roll-and-Play`、`Writer`、`Translator`、`Researcher`、`Tutor`板块规划中。

# 项目结构

### 最外层

```
agent-system-prompt/
├── Coder/                  编程
├── Roll-and-Play/          *角色扮演
├── Writer/                 *写作
├── Translator/             *翻译
├── Researcher/              *研究助手
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

## Coder - 编程助理

#### `.agent.md` - 助理内容
- **` Frontmatter ` 段** _适用于VS Code_ **：** YAML 格式，包括 ` name, description, argument-hint, tools, disable-model-invocation, user-invocable，agents `，各部分内容见VS Code官方文档。
- **`Agent Operating Manual`段：** Markdown 格式，内容为精确的、可执行的命令和流程。

#### `.env.md` - 环境需求
- Visual Studio Code 或其他支持YAML格式`Frontmatter`段的IDE
- - 版本
- - 插件 
- 编译与运行环境
- 额外的自备内容 _非必须_

#### `.info.md` - 介绍
- 使用方法
- 构造时间
- 更改记录

#### `Agent_list.md`
- 此版块的Agent概览
- 特殊说明
- 在命名中使用的缩写

# 其他说明

### Pull Requests

如果您认为您的Agent System Prompt足够优秀，欢迎以Pull Requests的形式作出贡献！

Pull Requests必须遵循对应板块的结构要求（参见`板块说明`章节）。

维护者 `MiklyWay` 通常将在每周三和周日集中审批。

### issue

如果您在使用此仓库中的Agent System Prompt时，发现AI做出了意料之外的操作，或是有可以优化的地方，请前往GitHub仓库提交issue。

在Gitee中提交的issue可能不会被解决。

### Gitee镜像

为方便国内用户访问，本仓库设立了官方Gitee镜像。

Gitee镜像使用`Gitee Auto Sync`与Github仓库保持同步。

### 关于维护者

此项目的维护者 `MiklyWay` 是一名高中生，随时可能因为 考试/OI竞赛 暂停维护此项目一段时间，还请谅解。

# 支持我的工作

你可以在 [爱发电](https://www.ifdian.net/a/miklyway) 中赞助我，
也可以在 [知乎](https://www.zhihu.com/people/miklyway)
或 [bilibili](https://space.bilibili.com/1022519074) 中给更新说明点一个免费的赞。
