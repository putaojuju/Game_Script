# 游戏脚本自动化项目规则

## 项目概述
多游戏脚本自动化系统，支持虚拟屏幕运行和独立鼠标控制，确保脚本稳定、高效、安全运行。

## 项目目录
```
项目根目录/
├─ Girls_Creation_script/       # 女生创作脚本
├─ twinkle_starknightsX/         # 闪耀骑士团脚本
├─ parsec-vdd-cli/               # 虚拟屏幕驱动CLI
├─ venv/                         # Python虚拟环境
├─ .trae/                        # TRAE IDE配置
├─ background_windows.py         # 窗口后台运行模块
├─ control_panel.py              # 控制面板
├─ game_window_manager.py        # 游戏窗口管理
├─ independent_mouse.py          # 独立鼠标控制
├─ virtual_display.py            # 虚拟屏幕管理
├─ script_manager.py             # 脚本管理器
├─ run_game_script.py            # 脚本运行器
├─ requirements.txt              # 依赖列表
└─ virtual_screen_documentation.md # 虚拟屏幕文档
```

## 技术栈
- **框架**：Airtest≥1.2.10
- **Python**：3.8-3.9
- **核心依赖**：airtest、pywin32、numpy、opencv-python
- **虚拟屏幕**：Parsec VDD Driver v0.41.0.0

## 代码规范
- **命名**：文件夹/文件名/变量/函数名用小写+下划线，类名用驼峰命名，截图用元素名.png
- **风格**：4空格缩进，每行≤100字符，函数/类前后空2行
- **注释**：函数用docstring，关键逻辑加单行注释
- **脚本稳定性**：touch()前加wait(≥10秒)，后加0.5-1.2秒随机延迟
- **防检测**：仅UI层操作，操作间隔随机延迟

## 分支管理
- **main**：稳定版本发布
- **develop**：开发整合分支
- **feature-xxx**：新功能开发
- **bugfix-xxx**：bug修复
- **hotfix-xxx**：紧急修复

## Git提交规范
<类型>: <简短描述>

<详细描述>

<可选标签>

**提交类型**：feat(新功能)、fix(修复)、docs(文档)、style(风格)、refactor(重构)、test(测试)、chore(构建)

## 虚拟屏幕要求
- 分辨率建议1920×1080@60Hz，最多8个
- 使用virtual_display.py管理，independent_mouse.py实现独立鼠标
- 所有脚本必须在虚拟屏幕测试通过

## 附则
本规则定期更新，违反可能导致代码驳回或任务延期。

**版本**：v1.0.0