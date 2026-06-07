# 运行环境要求

## Visual Studio Code

### 版本要求

- **最低版本**：1.110
- **推荐版本**：1.117 及以上
  - ⚠️ 已知 1.119 版本存在可能影响 Agent 调用的 bug，请避免使用该版本。

### 插件要求

| 插件                                                                                                        | 说明                                                | 必要性   |
| ----------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | -------- |
| [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)                        | AI 聊天与代码补全核心插件，提供 `@` 召唤 Agent 能力 | **必需** |
| [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)                              | Python 语言支持（数据生成、对拍脚本运行）           | **必需** |
| [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)                     | Python 语言服务（代码分析、类型检查、符号导航）     | **必需** |
| [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)                             | C++ 语言支持（语法高亮、智能提示、调试）            | **必需** |
| [C/C++ DevTools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpp-devtools)                | C++ 符号导航、调用关系分析等高级功能                | 推荐     |
| [Terminal Tools](https://marketplace.visualstudio.com/items?itemName=mijur.copilot-terminal-tools) （可选） | Copilot 终端命令执行能力（若无则 Agent 自行处理）   | 可选     |

### 配置说明

1. **注册 Agent 文件**：确保 `.agent.md` 文件位于 VS Code 可识别的路径下（如项目根目录 `.github/prompts/` 或用户 prompts 目录）。
2. **建议启用「绕过审批」**：在 VS Code 设置中搜索 `github.copilot.chat.autoEditMode` 或相关审批设置，启用后 Agent 可直接修改文件，减少交互确认步骤，提升竞赛调试效率。
3. **Python 环境配置**：Agent 依赖 Python 环境运行数据生成与对拍脚本，需确保已配置有效的 Python 解释器。

## 编译与运行环境

### GCC / G++
- **最低版本**：8.0.0
- **推荐版本**：9.3.0 及以上
- **编译命令**：`g++ -std=c++14 -O2 -Wall sol.cpp -o sol`
- **注意**：Agent 默认使用 C++14 标准；若题目要求 C++17/20，请在提示中说明。

### Python
- **最低版本**：3.5
- **推荐版本**：3.9 及以上
- **主要用途**：编写随机数据生成器（`gen.py`）、暴力验证脚本（`bruteforce.py`）、数据校验器（`validate.py`）以及对拍驱动脚本
- **依赖库**：`cyaron`（推荐，用于便捷构造竞赛测试数据）、`random`（内置，备选方案）

### 操作系统兼容性

本 Agent 已在以下系统中测试通过：
- **Linux**（✅ 当前环境）— 完整支持
- **Windows**（✅ 支持，需安装 MinGW/WSL 获取 GCC）
- **macOS**（✅ 支持，需安装 Xcode Command Line Tools 获取 GCC/Clang）

## 额外自备

### AI API Key

请自行准备并配置有效的 AI 服务密钥。推荐方案：

- **DeepSeek API Key**：前往 [DeepSeek 官网](https://platform.deepseek.com/) 申请
- 其他兼容 OpenAI API 格式的密钥亦可
- 配置方式：在 VS Code 设置中配置 `github.copilot.chat.*` 相关项，或通过对应扩展的 API Key 设置界面录入

### 可选工具

- **代码格式化**：`clang-format`（保持代码风格一致）
- **静态分析**：`cppcheck`（辅助 Agent 发现潜在问题）
- **性能分析**：`perf`（Linux）/ `gprof`（用于排查运行时性能瓶颈）
- **CYaRon 文档**：参见 https://github.com/luogu-dev/cyaron/wiki
