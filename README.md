# 使用方法（补充运行说明）
1. 安装 Qt 6.10.1（含 MinGW 64-bit 工具链）。确保 PATH 包含：
   - Qt Tools 下的 `mingw*_64\bin`
   - 对应 Qt 版本的 `Qt\6.10.1\mingw_64\bin`
   （路径随你安装位置而定，确保同一套 Qt/MinGW 且为 64 位。）
2. 在 PowerShell 执行：
   ```
   cd <项目目录>\src
   qmake tictactoe.pro     # 或 qmake6
   mingw32-make            # 生成 release\tictactoe.exe
   ```
3. 部署 Qt 依赖（在 release 目录）：
   ```
   cd <项目目录>\src\release
   windeployqt tictactoe.exe
   ```
   这一步会拷贝 Qt6*.dll 和 plugins，避免运行时报找不到入口点。
4. 运行：
   ```
   .\tictactoe.exe
   ```
   运行时保持当前 PATH 指向同一套 Qt/MinGW，不要混用旧版或其他版本的 DLL。

# 井字棋（tic-tac-toe）

使用α-β剪枝（Alpha-beta-pruning）的极小极大算法（Minimax-algorithm）实现的井字棋（一字棋、tic-tac-toe）游戏。

## 下载

[tic-tac-toe/releases](https://github.com/huihut/tic-tac-toe/releases)

## 演示

![demo](images/demo.gif)

## 更换主题

使用`tic-tac-toe\theme\theme*\`下三个图片替换`tic-tac-toe\src`中的三个图片即可更换主题。

* 主题一

  ![theme1](images/theme1.png)

* 主题二

  ![theme2](images/theme2.png)

* 主题三

  ![theme3](images/theme3.png)
