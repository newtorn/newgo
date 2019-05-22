<p align="right">中文 | <a href="../README.md">En</a>
<div align="center">
<h1>NewGO</h1>

轻松地通过newgo在你不同的项目中使用golang

[![GitHub release](https://img.shields.io/github/release/newtorn/newgo.svg)](https://github.com/newtorn/newgo/releases)
[![Github repository](https://img.shields.io/appveyor/ci/gruntjs/grunt.svg)](https://github.com/newtorn/newgo.git)
[![Github license](https://img.shields.io/github/license/newtorn/newgo.svg)](LICENSE)
===
</div>

## 关于

[newgo](https://github.com/newtorn/newgo.git)是一个GOPATH解决工具。在官方的情况下，为了构建和运行golang的包，你必须有一个全局或者临时的GOPATH环境变量，配置这些工作很麻烦而且不够灵活。现在newgo这个工具解决了它，所以你能够轻松地通过newgo在你不同的项目中使用golang。在你不同的项目中，它会在shell中自动为你创建临时的GOPATH和GOBIN环境变量，以供命令行编译golang使用。


## 快速上手

![quickstart](../assets/quickstart.gif)


## 安装

它很容易被安装，你可以直接将脚本clone到本地或者在mac上使用homebrew包管理工具安装。

#### MacOS
你可以使用brew命令安装它。
```
brew tap newtorn/tap && brew install newgo
```

#### Linux
你可以下载或者拷贝 [newgo](https://github.com/newtorn/newgo.git) 脚本到本地。
```
# 方法一：copy脚本到本地文件newgo

# 方法二：clone仓库到本地
git clone https://github.com/newtorn/newgo.git
cd newgo

# 移动脚本到/usr/local/bin
mv newgo /usr/local/bin/newgo

# 测试
newgo help
```


## 用法

```
# 首先创建你的工程
mkdir go-demo
cd go-demo

# 使用newgo初始化
# 它会在项目中创建src，pkg和bin文件夹
newgo init

# 编写程序
mkdir src/hello-app
cd src/hello-app
vim hello.go

# 使用newgo代替默认的go命令行工具
# 使用newgo执行go run例子
newgo run hello.go

# 使用newgo执行go build例子
newgo build hello.go

# 使用newgo执行go install例子
newgo install hello.go

# 获取帮助
newgo help
```


## 注意

一旦你离开当前项目并且在另一个项目中使用newgo init命令，那么newgo将使用另一个项目作为GOPATH，所以当你回到该项目的时候，你应该重新使用newgo init以使用newgo。


## 贡献

我很热爱你为newgo贡献，请阅读我的[贡献指南](../CONTRIBUTING.md)


## 声明

代码使用 [MIT](../LICENSE) 声明
