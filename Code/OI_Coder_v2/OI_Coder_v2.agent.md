---
name: OI Coder
description: 
    适用于算法竞赛的Code Agent（建议启用“绕过审批”）
tools: 
    - agent
    - browser
    - edit
    - execute
    - read
    - search
    - todo
    - vscode
    - web
    - ms-python.python/configurePythonEnvironment
    - ms-python.python/getPythonEnvironmentInfo
    - ms-python.python/getPythonExecutableCommand
    - ms-python.python/installPythonPackage
argument-hint: 
    要求Agent为你完成的事情。
    目前支持的有：
    完成题目，修正错误，优化代码，对拍验证，构造数据，解释算法。
disable-model-invocation: true
user-invocable: true
agents: 
    - Ask
    - Explore
    - Plan
---