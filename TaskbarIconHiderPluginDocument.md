TaskbarIconHider 插件说明
=

功能概述
-
本插件提供在 Windows 平台动态隐藏指定进程任务栏图标的完整解决方案，适用于需要精确控制任务栏显示状态的应用程序开发。

插件获取
-
✅ 需从 **官方商城** 购买正版插件

运行环境
-
Unreal Engine  
Windows 10/11 64-bit  
Visual Studio 2022 17.5+

安装配置指南
-

解压插件至目标工程目录：

    YourProject/  
        └── Plugins/  
            └── TaskbarIconHider/  
                ├── Resources/  
                ├── Source/  
                └── TaskbarIconHider.uplugin

激活插件：
-
1. 启动引擎后进入 **Edit > Plugins**  
2. 搜索并启用 **"TaskbarIconHider"** 插件  
3. 重启编辑器完成加载

核心功能接口
-

**C++ 调用方式**：
// 获取当前进程ID（典型用法）
int32 CurrentPID = FPlatformProcess::GetCurrentProcessId();

// 执行图标隐藏操作
UTaskbarIconHiderBPLibrary::HideIconByProcessID(CurrentPID);

**蓝图节点路径**：
[右键图表] > Add Action > TaskbarIcon Hider
    └── Hide Icon By Process ID (int32)

打包部署
-
支持常规打包流程，无需额外配置。

技术支持
-
开发者联系方式：  
📧 **steven_collins@mail.com**  

⚠️ 技术说明：  
底层通过设置窗口样式（`WS_EX_TOOLWINDOW`）实现功能，部分安全防护软件可能触发误报。
int32 CurrentPID = FPlatformProcess::GetCurrentProcessId();

// 执行图标隐藏操作
UTaskbarIconHiderBPLibrary::HideIconByProcessID(CurrentPID);
