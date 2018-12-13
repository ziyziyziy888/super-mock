## super-easy-mock

> 作者：张子元

> super-easy-mock 旨在快速的，无侵略性，无耦合的切入到项目中使用mock数据，并为大家提供简单易用的前端假数据的解决方案。

#### 安装
```bash
 # 使用 npm 安装方式安装：
 npm i super-easy-mock -g
 
 # 使用 yarn 安装方式安装：
 yarn global add super-easy-mock
 
 # 使用美菜npm源 mnpm
 mnpm i super-easy-mock -g
```

#### 使用
```bash
# Show help
smock --help

# Initailization and start
smock --init

# Start proxy server
smock --start

# Add new url
smock --add	

# Add mock floder to .gitignore
smock --ignore    
```

#### 快速开始
##### 1.项目根目录下执行

```bash
	smock --init
```

##### 2.根据提示，先输入将要代理的服务的域名，然后输入将要代理的服务的端口

> 例如我想代理 www.baidu.com，那么就依次输入 www.baidu.com, 端口默认为80，所以可以直接回车

> 例如我想代理 local.yunshanmeicai.com:7777，那么就依次输入 local.yunshanmeicai.com, 端口输入 7777 回车即可

##### 3.第二个步骤会在你的项目目录中生成了一个mock文件夹，请把这个文件夹加入到 .gitignore 中不要随项目提交到远程仓库
```bash
# 或也可以直接执行以下命令，自动将mock文件夹加入git忽视
smock --ignore
```

##### 4.现在就可以开始享受 smock 带给你的便利了

#### 实际使用场景
##### 1. 启动服务后，访问 localhost:3000， 就相当于访问代理的目标网站
> 比如此时有一个接口 /a/b/c， 需要使用本地的假数据， 
> 
> 可以先执行 smock --add 然后输入‘/a/b/c’，smock会自动在mock文件夹中的 a=>b的目录内，生成一个 c.json
> 
> 此时只要将后端的数据结构复制进来，访问 localhost:3000的时候，/a/b/c接口访问的就是本地的json数据了

##### 2.当你不想使用这个接口时，只需将生产的json文件重命名即可，例如 a.json变成 _a.json，接口访问获得的数据就不再是本地的假数据了



























