# GameNetworkingSockets vs2017 project build by CMake-3.19.0
Origin:[GameNetworkingSockets](https://github.com/ValveSoftware/GameNetworkingSockets)

You may read the GameNetworkingSockets origin page first. 
你应该先阅读GameNetworkingSockets源码页面上的相关说明

Here just provides VS2017 project files generated according to GameNetworkingSockets source code.
这里仅提供了一个根据GameNetworkingSockets源码生成出来的vs2017工程文件

## Dependencies
* OpenSSL 1.1.1 or later
* Google protobuf 2.6.1+  ([protobuf-3.5.x release](https://github.com/sitonmoon/protobuf-3.5.x-Release))
这里提供的链接是根据protobuf3.5.x源码编译出来的库文件，可以直接下载使用<br>
* Google [webrtc](https://opensource.google/projects/webrtc) is used for
  NAT piercing (ICE) for P2P connections.  The relevant code is linked in as a
  git submodule.  You'll need to initialize that submodule to compile.<br>
  webRTC这个子模块我这里没有添加成功，不过不需要webRTC也可以编译GameNetworkingSockets工程，就是可能会没有P2P连接功能<br>
  
## VS solution file
'/build/GameNetworkingSockets.sln'
直接打开VS2017解决方案，然后生成“ALL BUILD”项目即可生成GameNetworkingSockets网络库的相关dll文件

## Demo
解决方案中有个用于测试的Demo聊天室项目"example_chat",生成该项目后会在输出目录输出一个"example_chat.exe"可执行程序<br>
![](https://github.com/sitonmoon/GameNetworkingSockets-VS2017/blob/main/demo1.png)<br>

用法就是创建快捷方式，在后面加参数：<br>
 server 表示启动服务器<br>
 client 127.0.0.1 表示启动客户端 并使用默认端口连接本地服务器<br>
 启动两个客户端就可以互相聊天了。<br>
 ![](https://github.com/sitonmoon/GameNetworkingSockets-VS2017/blob/main/demo2.png)<br>
