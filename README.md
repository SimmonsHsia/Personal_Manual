# 个人技术文档
受周老师启发，在此建立个人技术文档，用于记录每天解决的问题。一是防止遗忘，二是希望能够帮助到别人。

---

## 2025/2/27

### vscode配置c语言环境

1. 下载并安装[vscode](https://code.visualstudio.com "vscode官网")

2. 在vscode中安装插件：
    - [Chinese (Simplified) (简体中文) Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-zh-hans)
    - [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)

3. 使用MSYS2安装MinGW-w64编译器：
    - 下载并安装[MSYS2](https://www.msys2.org/)
    - 打开UCRT64并重复执行 `pacman -Suy` 直到提示所有软件包都是最新
    - 最后执行 `pacman -S mingw-w64-ucrt-x86_64-toolchain` 系统提示选择一项时按`Enter`接受所有安装包

4. 在环境变量的用户变量`Path`中新建路径：`*\msys64\ucrt64\bin`

5. 一切准备就绪，开始编程吧！

## 2025/3/6

### Github提交签名验证

- 参考[Github官方文档](https://docs.github.com/zh/authentication/managing-commit-signature-verification/about-commit-signature-verification)即可

## 2025/3/25

### 解决 git push/pull 网络问题

1. 打开 `git bash` 终端，输入以下命令取消原来的代理恢复默认：

    ```
    git config --global --unset http.proxy

    git config --global --unset https.proxy
    ```

2. 第二步设置代理：
    ```
    git config --global https.proxy https://127.0.0.1:7897

    git config --global http.proxy http://127.0.0.1:7897
    ```

    ![git bash终端命令](/set%20proxy.png)

    设置完成后可通过 `git config --global https.proxy` 查看代理设置
    
    其中，`https://127.0.0.1` 和 `http://127.0.0.1` 是代理IP地址，冒号后面的 `7897` 是端口。这两项根据自己的电脑设置确定，可以在 `设置-网络和Internet-代理` 的手动设置代理中找到。

    ![win11代理设置](/win11%20proxy.png)
