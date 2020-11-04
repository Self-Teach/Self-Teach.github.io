# Win10系统（64位）安装Visual Studio Code的方法

### 1. Visual Studio Code
1. Visual Studio Code 是微软开发并开源的程序源代码编辑器（以下简称 VSCode），VSCode 集成了对各种编程语言和工具的支持，我们写程序代码和文档都可以用它。

### 2. 下载与安装
1. 访问 [Visual Studio Code](https://code.visualstudio.com/) 主页并点击下载按钮，下载时注意看清楚是和自己的操作系统一致（Windows）的版本；
2. 运行下载好的 VSCode 安装程序（通常叫 VSCodeUserSetup-xxx-1.xx.x.exe）；
3. 安装好后即可从 Windows 开始菜单运行 VSCode，也可以从命令行运行。

### 3. ConEmu运行VSCode
1. 进入 ConEmu 在命令行操作界面；
2. 通过 ```cd A:\python``` 进入相应的目录；
3. 输入 ```mkdir Code ↩︎``` 在目录下创建一个叫 ```Code``` 的子目录，写的代码都可以放在这里；
4. 输入 ```cd Code ↩︎``` 进入 Code 子目录；
5. 输入 ```code . ↩︎``` 这里 ```code``` 是运行 VSCode 的命令行命令，后面跟的参数是命令 VSCode 打开的文件或者文件夹，这里我们用一个点 ```.``` 代表 “当前目录”，所以此命令会运行 VSCode 并打开 ```Code``` 这个目录；
6. 在打开的 VSCode 中按 Ctrl+N 打开一个新文件，输入 ```print('Hello world!')```，然后按 Ctrl+S 保存，文件名为 ```hello.py```；
7. 然后回到 ConEmu 窗口，输入 ```ls ↩︎```，可以看到刚才新建的文件 ```hello.py```；输入 ```python hello.py ↩︎``` 应该可以看到运行 ```hello.py``` 程序的结果。

    ```
    ↩︎ 代表回车键 Enter
    ```

## Visual Studio Code 安装完毕