TaskbarIconHider 示例工程说明（UE5.3.2 版）
📦 项目概述
本示例演示如何通过 TaskbarIconHider 插件 在 Windows 平台动态隐藏指定进程的任务栏图标。基于 Unreal Engine 5.3.2 构建，适用于需要精确控制任务栏显示状态的应用场景。

🔧 前置要求
插件获取
✅ 需从 官方商城 购买正版插件
❌ 本示例工程 不包含 插件二进制文件

运行环境
Unreal Engine 5.3.2
Windows 10/11 64-bit
Visual Studio 2022 17.5+

📂 工程配置指南
插件安装流程
解压购买的插件包至工程目录：
YourProject/
└── Plugins/
    └── TaskbarIconHider/
        ├── Resources/
        ├── Source/ 
        └── TaskbarIconHider.uplugin
        
启用插件：
启动引擎后进入 Edit > Plugins
搜索并启用 "TaskbarIconHider" 插件
重启编辑器生效

🎮 核心功能演示
C++ 调用接口
// 获取当前进程ID（示例）
int32 CurrentPID = FPlatformProcess::GetCurrentProcessId();

// 通过进程ID隐藏图标
UTaskbarIconHiderBPLibrary::HideIconByProcessID(CurrentPID);

蓝图节点说明
[右键图表] > Add Action > TaskbarIcon Hider
└── Hide Icon By Process ID (int32)

⚙️ 打包说明
直接通过标准打包流程构建即可，无特殊配置要求。

📜 许可证协议
本插件采用 BSD-3-Clause License：
Copyright (c) 2025 Steven Collins <steven_collins@mail.com>
允许在保留版权声明的前提下自由使用/修改/分发，详见 LICENSE 文件

🛠 技术支持
联系开发者：
📧 steven_collins@mail.com
⚠️ 注意：本功能通过修改窗口样式实现（WS_EX_TOOLWINDOW），部分安全软件可能误判为可疑行为。
