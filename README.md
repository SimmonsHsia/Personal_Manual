# 个人技术文档
受周老师启发，在此建立个人技术文档，用于记录每天解决的问题。一是防止遗忘，二是希望能够帮助到别人。

---

## 2025/2/27

### vscode配置c语言环境

1. 下载并安装[vscode](https://code.visualstudio.com "vscode官网")

2. 在vscode中安装插件：
    - [Chinese (Simplified) (简体中文) Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hans)
    - [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)

3. 使用MYSY2安装MinGW-w64编译器：
    - 下载并安装[MYSY2](https://www.msys2.org/)
    - 打开MSYS2并分别执行 `pacman -Syu` 和 `pacman -Su` 以更新库
    - 最后执行 `pacman -S --needed base-devel mingw-w64-x86_64-toolchain` 系统提示选择一项时输入Y接受所有安装包

4. 在环境变量的用户变量`Path`中新建编译器路径`*\msys64\ucrt64\bin`

5. 一切准备就绪，开始编程吧！

