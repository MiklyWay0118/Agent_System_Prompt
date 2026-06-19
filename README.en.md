[**中文版**](./README.md) | **English**

---

## Open Source License

All content in this repository is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

# Introduction

The goal of this project is to build a large-scale, high-quality library of AI System Prompts.

### Project Links

[GitHub Repository](https://GitHub.com/MiklyWay0118/Agent_System_Prompt.git),
[Gitee Mirror Repository](https://gitee.com/YingHe01/agent-system-prompt.git)

### Current Status

`Coder` section is under construction;

`Roll-and-Play`, `Writer`, `Translator`, `Researcher`, `Tutor` sections are planned.

# Project Structure

### Top-Level Directory

```
agent-system-prompt/
├── Coder/                  Programming
├── Roll-and-Play/          *Role-playing
├── Writer/                 *Writing
├── Translator/             *Translation
├── Researcher/             *Research Assistant
├── Tutor/                  *Tutoring
├── .../
│
└── README.md
```
_Note: `*` indicates not yet available_

### Second-Level Directory

```
[Type]/
├── [Name-1]/
│   ├── [Name-1].agent.md   Agent Content
│   ├── [Name-1].env.md     *Environment Requirements
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
- **`Frontmatter` Section** _for VS Code_ **:** YAML format,
  including `name, description, argument-hint, tools, disable-model-invocation, user-invocable, agents`.
  See VS Code official documentation for details.
- **`Agent Operating Manual` Section:** Markdown format, containing precise and executable commands and workflows.

#### `.env.md` - Environment Requirements
- Visual Studio Code or other IDEs that support YAML format `Frontmatter` section
- - Version
- - Extensions
- Compilation and runtime environment
- Additional self-provided content _optional_

#### `.info.md` - Introduction
- Usage instructions
- Creation date
- Changelog

#### `Agent_list.md`
- Overview of Agents in this section
- Special notes
- Abbreviations used in naming

# Other Information

### Contributing

If you think your Agent System Prompt is outstanding enough, you are welcome to contribute via Pull Requests!

If you encounter unexpected AI behavior while using any Agent System Prompt from this repository, or see areas for improvement, please submit an issue on the GitHub repository.

For details, see the [Contributing Guide](./CONTRIBUTING.md).

### Gitee Mirror

To facilitate access for users in China, this repository has a Gitee mirror.

The Gitee mirror uses `Gitee Auto Sync` to stay synchronized with the GitHub repository.

### About the Maintainer

The maintainer of this project, `MiklyWay`, is a high school student. Maintenance may be paused from time to time due to exams or OI (Olympiad in Informatics) competitions. Thank you for your understanding.

You can contact me via email at `milkyway1886@foxmail.com`.

# Support My Work

You can sponsor me on [Afdian](https://www.ifdian.net/a/miklyway) (in Chinese),
or follow me on [Zhihu](https://www.zhihu.com/people/miklyway),
or leave a free like on update notes at [Bilibili](https://space.bilibili.com/1022519074).
