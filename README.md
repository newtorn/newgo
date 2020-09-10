<p align="right">En | <a href="./doc/README-zh_cn.md">中文</a>
<div align="center">
<h1>NewGO</h1>

Easily use golang in your different projects with newgo

[![GitHub release](https://img.shields.io/github/release/newtorn/newgo.svg)](https://github.com/newtorn/newgo/releases)
[![Github repository](https://img.shields.io/appveyor/ci/gruntjs/grunt.svg)](https://github.com/newtorn/newgo.git)
[![Github license](https://img.shields.io/github/license/newtorn/newgo.svg)](LICENSE)
===
</div>

## About

[newgo](https://github.com/newtorn/newgo.git) is a GOPATH solution tool. 
Officially to build and run go packages, your must have global or temporary GOPATH and GOBIN enviroment variables, it's a annoying and not enough freedom.
Now newgo solved it, so you can easily use golang in your different projects with newgo. And in different projects, it will automatically create temporary GOPATH and GOBIN to system shell enviroment variable.


## QuickStart

![quickstart](assets/quickstart.gif)


## Installation

It's easy to be installed.

#### MacOS
You can use homebrew to install it.
```
brew tap newtorn/tap && brew install newgo
```

#### Linux
You should download or copy [newgo](https://github.com/newtorn/newgo.git) shell script.
```
# First by method 1
# copy newgo shell script to newgo file

# First by method 2
# or git clone newgo repo
git clone https://github.com/newtorn/newgo.git
cd newgo/src

# Second
mv newgo /usr/local/bin/newgo

# Test
newgo help
```


## Usage

```
# first go to your projects
mkdir go-demo
cd go-demo

# initialize newgo
# it will create three floders src, pkg and bin
newgo init

# edit program
mkdir src/hello-app
cd src/hello-app
vim hello.go

# then you can use newgo instead of default go
# exmaple for command go run
newgo run hello.go

# exmaple for command go build
newgo build hello.go

# exmaple for command go install
newgo install hello.go

# Get help
newgo help
```


## Notice

Once you leave current project and initialize newgo in another project, when you enter this project you must reinitialize again to use newgo.

## Contributing

I'd love you to contribute to newgo, please read my [Contribution Guide](CONTRIBUTING.md)


## License

Code license with [MIT](LICENSE)
