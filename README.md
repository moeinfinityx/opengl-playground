# OpenGL Playground

A basic reop contains all necessary libraries and configs to build a modern OpenGL program.

## 克隆本项目/Clone this repository

Github:

```shell
git clone https://github.com/moeinfinityx/opengl-playground.git --recursive
```

Gitlab:

```shell
git clone https://git.sinomo.net/ix/opengl-playground.git --recursive
```

如果你已经克隆了本项目，但是忘记了`--recursive`选项：

```shell
cd opengl-playground
git submodule init
git submodule update --recursive
```

## 使用说明/How to use

这是一个简单的OpenGL学习环境。

OpenGL Playground使用CMake管理，支持Windows、Linux和Mac OS。

首先，你需要一个基本的C++开发环境。在Linux上，可以使用GCC。在Windows上，可以使用Visual Studio、MinGW或者MSYS2。在MacOS上，可以使用XCode。

然后，安装CMake.

CMake下载地址：https://cmake.org/download/

Linux和Mac OS可以使用包管理器来安装CMake。

```shell
apt install cmake
```

```shell
brew install cmake
```

### 编译、运行/Compile and run

Linux、MSYS2:

```shell
cd OpenGLPlayground
mkdir build
cd build
cmake ..
cmake --build .
```

Visual Studio:

打开PowerShell或CMD，执行

```shell
cd OpenGLPlayground
mkdir build
cd build
cmake -G "Visual Studio 14 2015" ..
cmake --build .
```

当然也可以打开生成的Visual Studio项目进行生成。

生成的可执行文件在`build/`下的响应目录里，如自带的`demo1`的可执行文件默认在`build/demo1`下。

### 添加更多程序

想要添加多个程序，不需要复制整个项目。只需复制`demo1`，并在项目根目录下的`CMakeLists.txt`里添加上新的文件夹即可。

如复制`demo1`并命名为`demo2`，只要在`CMakeLists.txt`中添加

```cmake
add_subdirectory(demo2)
```

## 环境信息

GLAD Options:

OpenGL: 3.2
OpenGL ES1: 1.0
OpenGL ES2: 3.2

## Contribution

如果你有任何的意见和建议，可以提交一个Issue，或者直接提交Pull Request。

现在可能需要的改进：

 - 改进CMake项目结构
 - 添加更多的常用库，并只编译使用了的库
 - 添加OpenGL版本选项
 - 一键编译、运行脚本
 - 更多示例
 - 更多说明文档、注释

## LICENSE

WTFPL

<a <a href="http://www.wtfpl.net/"><img src="http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-4.png" width="80" height="15" alt="WTFPL" /></a>

