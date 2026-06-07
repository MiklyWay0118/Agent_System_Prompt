[**中文版**](./README.md) | **English**

> This English version is translated by AI for reference only. The original Chinese version ([README.md](./README.md)) shall prevail.

---

## Open Source License

All content in this repository is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

# Introduction

The goal of this project is to build a large-scale, high-quality AI System Prompt library.

### Project Links

[GitHub Repository](https://github.com/MiklyWay0118/Agent_System_Prompt.git),
[Gitee Mirror Repository](https://gitee.com/YingHe01/agent-system-prompt.git)

### Current Status

- `Coder` section: under construction
- `Roll-and-Play`, `Writer`, `Translator`, `Researcher`, `Tutor` sections: planned

# Project Structure

### Top Level

```
agent-system-prompt/
├── Coder/                  Programming
├── Roll-and-Play/          *Role Playing
├── Writer/                 *Writing
├── Translator/             *Translation
├── Researcher/             *Research Assistant
├── Tutor/                  *Learning
├── .../
│
└── README.md
```
_Note: `*` indicates not yet available_

### Second Level

```
[Type]/
├── [Name-1]/
│   ├── [Name-1].agent.md   Agent content
│   ├── [Name-1].env.md     *Environment requirements
│   └── [Name-1].info.md    *Introduction
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
_Note: `*` indicates optional_

# Section Description

## Coder - Programming Assistant

#### `.agent.md` - Agent Content
- **`Frontmatter` Section** _for VS Code_: YAML format, including `name, description, argument-hint, tools, disable-model-invocation, user-invocable, agents`. See VS Code official documentation for details.
- **`Agent Operating Manual` Section**: Markdown format, containing precise, executable commands and workflows.

#### `.env.md` - Environment Requirements
- Visual Studio Code or other IDEs that support YAML `Frontmatter` sections
  - Version
  - Extensions
- Compilation and runtime environment
- Additional user-provided content _(optional)_

#### `.info.md` - Introduction
- Usage instructions
- Creation date
- Change log

#### `Agent_list.md`
- Overview of agents in this section
- Special notes
- Abbreviations used in naming

# Other Information

### Pull Requests

If you believe your Agent System Prompt is excellent enough, contributions via Pull Requests are welcome!

Pull Requests must follow the structural requirements of the corresponding section (see the `Section Description` chapter).

The maintainer `MiklyWay` usually reviews PRs on Wednesdays and Sundays.

### Issues

If you encounter unexpected AI behavior or find areas for improvement while using the Agent System Prompts from this repository, please submit an issue on the GitHub repository.

Issues submitted on Gitee may not be addressed.

### Gitee Mirror

For the convenience of users in China, an official Gitee mirror has been set up.

The Gitee mirror uses `Gitee Auto Sync` to stay synchronized with the GitHub repository.

### About the Maintainer

The maintainer of this project, `MiklyWay`, is a high school student who may need to pause maintenance for exams or OI (Olympiad in Informatics) competitions from time to time. Your understanding is appreciated.

# Support My Work

You can sponsor me on [aifadian](https://www.ifdian.net/a/miklyway),
or give a free like on [Zhihu](https://www.zhihu.com/people/miklyway)
or [bilibili](https://space.bilibili.com/1022519074) for the update notes.
