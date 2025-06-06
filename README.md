# 反反截图DLL注入工具

## 项目介绍

这是一个用于对抗软件反截图机制的DLL注入工具。通过将特制的DLL注入到目标进程中，可以绕过其反截图保护，使用户能够正常进行截图操作，获取屏幕内容。

## 功能特点

- 支持32位和64位Windows系统
- 能够绕过多种反截图保护机制
- 针对常见的反截图API进行Hook和模拟
- 低资源占用，对系统性能影响小
- 无需修改目标程序，通过注入方式实现功能

## 项目结构

```
├── InjectHookDll32.dll    # 32位注入DLL
├── InjectHookDll64.dll    # 64位注入DLL
├── x64                    # 64位项目文件
│   ├── Version           # 64位源代码
│   └── Version.sln       # 64位解决方案文件
└── x86                    # 32位项目文件
    ├── Version32         # 32位源代码
    └── Version32.sln     # 32位解决方案文件
```

## 使用方法

### 前提条件

- Windows操作系统 (支持Windows 7/8/10/11)
- 根据目标进程选择对应的32位或64位DLL

### 注入步骤

1. 确定目标反截图软件进程的位数（32位或64位）
2. 选择对应的DLL（InjectHookDll32.dll或InjectHookDll64.dll）
3. 使用DLL注入工具将DLL注入到目标进程
4. 注入成功后，DLL会自动开始对抗反截图机制
5. 此时可以使用常规截图工具（如系统自带的截图、Snipping Tool等）正常截取屏幕内容

## 开发环境

- Visual Studio 2019或更高版本
- Windows SDK
- C/C++开发环境

## 编译方法

1. 使用Visual Studio打开对应的解决方案文件（x64/Version.sln或x86/Version32.sln）
2. 选择Release配置
3. 编译解决方案
4. 编译成功后，可在输出目录找到生成的DLL文件

## 注意事项

- 本工具仅供学习和研究使用，请勿用于非法用途
- 某些软件可能有多层反截图保护，可能需要多次尝试或组合使用其他技术
- 部分软件可能会检测DLL注入行为，导致工具失效或程序崩溃
- 软件更新可能会改变其反截图机制，需要相应更新本工具
- 使用前请备份重要数据，避免意外损失

## 免责声明

本项目仅供学习和研究Windows API Hook技术和反反截图机制使用，开发者不对使用本工具导致的任何问题负责。使用者需自行承担使用本工具的风险和法律责任。使用本工具时请遵守相关法律法规，尊重软件开发者的知识产权。

## 感谢

[对网课软件反反截屏（破解反截屏）的小研究 - 吾爱破解 - 52pojie.cn](https://www.52pojie.cn/thread-2002346-1-1.html)
