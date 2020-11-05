# Win10系统（64位）配置ConEmu命令行界面的方法

### 1. 确认系统架构
1. 单击桌面左下角的搜索按钮，输入 ```cmd``` ，运行命令行界面 (Command Prompt)；
2. 在命令行界面输入：```wmic CPU get DataWidth```，按```Enter```键后返回的是 ```CPU``` 架构(64 或 32 位)；
3. 在命令行界面输入：```wmic OS get OSArchitecture```，按```Enter```键后返回的是 ```Windows``` 操作系统架构(64或32位)

### 2. 确认 PowerShell 版本
1. PowerShell 是 Windows 下的增强命令行环境，也是我们以后要用的主要命令行界面。
2. 以下操作继续在上面打开的命令行界面进行：
    ```
    1. 在命令行界面输入：powershell 后按 Enter 键，命令行界面的行首提示信息出现了 PS 字样；
    2. 在命令行界面输入：$PSVersionTable.PSVersion.Major 后按 Enter 键。
    ```
&emsp;&emsp;上面的命令返回为 5 或者以上就没问题。


**否则**需要下载并安装：


&emsp;&emsp;1. [.NET Framework 4.5 or later](https://dotnet.microsoft.com/download)


&emsp;&emsp;2. [Windows Management Framework 5.x](https://www.microsoft.com/en-us/download/details.aspx?id=54616)


&emsp;&emsp;以上确认完毕可以在命令行界面输入：```exit``` 按 ```Enter``` 键退出。

### 3. 安装ConEmu
1. ConEmu简介：是一款免费的DOS系统仿真器，体积小巧，界面清爽，支持多标签操作，兼容dos原有的指令。
2. ConEmu下载：


    &emsp;&emsp;1. 进入 [ConEmu](https://conemu.github.io/) 首页，点击 Download 按钮，选择下载页面中最新的“Inster (32-bit, 64-bit)” 安装器版本（一般是 Alpha 版本，有时候没有新的 Alpha 版本那就是 Preview 版本）；


    &emsp;&emsp;2. 运行下载好的 ConEmu 安装程序（通常叫 ConEmuSetup.xxxxx.exe），如果前面检查的 Windows 版本为 64 位就选择安装 x64（64位）版本，否则选择 x86（32位）版本；安装时有的防病毒软件可能会报出病毒警告，请放心继续安装，这是误报。

3. ConEmu设置：
    1. 运行 ConEmu，可以看到下面这样的界面；


    <img src="./Pictures/ConEmu.png">

    2. 单击 ConEmu 左上角的图形按钮（如上图红框），从弹出菜单中选择 Settings，在打开的设置窗口将下图所示的选项改为 {Shells::PowerShell}，点击 Save settings 来保存修改；


    <img src="./Pictures/ConEmu-Setting.png">

    3. 退出 ConEmu 然后重新运行它，可以进入一个 PowerShell 环境，注意每行开始的提示符变成了 PS；


    <img src="./Pictures/ConEmu-PS.png">

    4. 当需要“打开命令行界面运行 ````xxxx```` 命令”的时候，就是指在上图这个 PowerShell 界面下输入 ```xxxx ↩︎```；


    <img src="./Pictures/ConEmu-Admin.png">
    
    5. 需要以管理员的权限执行一些命令行命令，那么就需要启动 ConEmu 然后打开一个管理员权限的 PowerShell 界面，方法是选右上角的绿色加号然后按下图选择。

    ```
    ↩︎ 代表回车键 Enter
    ```

## ConEmu 安装设置完毕
