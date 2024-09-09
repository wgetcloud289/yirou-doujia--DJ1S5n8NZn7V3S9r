[合集 \- .NET 开源工具(12\)](https://github.com)[1\..NET 开源快捷的数据库文档查询和生成工具07\-31](https://github.com/1312mn/p/18333223)[2\..NET 结果与错误处理利器 FluentResults08\-01](https://github.com/1312mn/p/18336221)[3\..NET\+WPF 桌面快速启动工具 GeekDesk08\-19](https://github.com/1312mn/p/18361056)[4\.Gradio.NET 支持 .NET 8 简化 Web 应用开发08\-26](https://github.com/1312mn/p/18370464)[5\..NET 开源实时监控系统 \- WatchDog08\-27](https://github.com/1312mn/p/18379779)[6\.实用接地气的 .NET 微服务框架08\-28](https://github.com/1312mn/p/18381195)[7\..NET 开源报表神器 Seal\-Report08\-30](https://github.com/1312mn/p/18385442)[8\..NET 最好用的验证组件 FluentValidation09\-03](https://github.com/1312mn/p/18393208)[9\..NET 8\.0 文档管理系统网盘功能的实现09\-04](https://github.com/1312mn/p/18392313)[10\..NET 8 \+ WPF 企业级工作流系统09\-05](https://github.com/1312mn/p/18395595)[11\..NET 多版本兼容的精美 WinForm UI控件库09\-06](https://github.com/1312mn/p/18389654)12\.超轻量级、支持插件的 .NET 网络通信框架09\-09收起:[豆荚加速器](https://yirou.org)**阅读目录**

* [前言](#_label0)
* [项目介绍](#_label1)
* [项目环境](#_label2)
* [项目功能](#_label3)
* [项目特点](#_label4)
* [项目使用](#_label5)
* [项目案例](#_label6)
* [项目地址](#_label7)
* [最后](#_label8)

## 前言


给大家推荐一个轻量级的、支持插件的综合网络通信库：TouchSocket。


TouchSocket 的基础通信功能包括 TCP、UDP、SSL、RPC 和 HTTP。其中，HTTP 服务器支持 WebSocket、静态网页、XML\-RPC、WebAPI 和 JSON\-RPC 等扩展插件。


此外，TouchSocket 还支持自定义协议的 TouchRPC，具备 SSL 加密、异步调用、权限管理、错误状态返回、服务回调和分布式调用等功能。


在空载函数执行时，10 万次调用仅需 3\.8 秒；在不返回状态时，仅需 0\.9 秒。


## 项目介绍


TouchSocket（Pro）是基于 .NET 的程序集系列，可用于对应 .NET 版本的 C\#、F\# 和 VB.NET 项目。无论你的项目是控制台、WinForms、WPF 还是 ASP.NET Core，它都全面支持。


TouchSocket（Pro）长期支持 .NET 4\.5、.NET 4\.8\.1、.NET Standard 2\.0 三个平台，并将 .NET 6\.0 作为最新稳定版支持平台，同时支持.NET 7\.0 作为最新发布平台。


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907164654052-896424236.png)


## 项目环境


.NET 4\.5：保证了在.Net Framework上的最低支持版本。基本上支持全系99%的功能。


.NET 4\.8\.1：这是在net45的依赖基础之上，额外添加了一些微软官方库，以支持达到net6\.0一样的功能（例如：Span、ValueTuple、ValueTask等）。


.NET Standard 2\.0：这是保证了在一些通用平台上的最低依赖。基本上支持全系99%的功能。


.NET 6\.0：这是目前最新的稳定版发布平台，它在最低依赖的前提下，还保证了全部功能。


.NET 7\.0：这是目前最新的发布平台，我们会在该平台上开发最能尝鲜的功能（例如：AOT等）。


支持框架的框架Console、WPF、Winform、Blazor Server、Xamarin、MAUI、Avalonia、Mono、Unity 3D（除WebGL）、其他（即所有C\#系）


## 项目功能


### 1、功能导图


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907164816191-1458492251.png)


 


### 2、项目文档


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907164940184-858301155.png)


## 项目特点


### 1、传统 IOCP 与 TouchSocket 的 IOCP 模式


TouchSocket 的 IOCP 模式与传统 IOCP 不同。以微软官方示例为例，传统 IOCP 使用 MemoryBuffer 开辟一块内存，均分后给每个会话分配一个区域接收数据，收到数据后再复制并处理。而 TouchSocket 则在每次接收前从内存池中获取一个可用内存块直接用于接收，收到数据后直接处理该内存块，从而避免了复制操作。虽然这只是细节上的设计差异，但在传输 10 万次 64KB 数据时，性能提升了 10 倍。


### 2、数据处理适配器


TouchSocket 在设计时借鉴了其他产品的优秀理念，数据处理适配器就是其中之一。与其他产品不同的是，TouchSocket 的适配器功能更加强大、易用且灵活。它不仅可以提前解析数据包，还可以解析数据对象，并且可以随时替换，立即生效。例如，可以使用固定包头对数据进行预处理，从而解决数据分包和粘包问题；也可以直接解析 HTTP 数据协议和 WebSocket 数据协议等。


### 3、兼容性与适配


TouchSocket 提供多种框架模型，能够完全兼容基于 TCP 和 UDP 协议的所有协议。例如，TcpService 和 TcpClient 的基础功能与 Socket 相同，但增强了框架的坚固性和并发性，通过事件形式抛出连接和接收数据，使用户能够更加友好地使用。


## 项目使用


### 1、Nuget安装


搜索框输入TouchSocket，然后在搜索结果中选择，点击安装，具体如下图所示


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907165102115-1597021877.png)


### 2、TcpService


TcpService是Tcp系服务器基类，它不参与实际的数据交互，只是配置、激活、管理、注销、重建SocketClient类实例。


而SocketClient是当**TcpClient（客户端）** 成功连接服务器以后，由服务器新建的一个实例类，后续的所有通信，也都是通过该实例完成的。




```
var service = new TcpService();
service.Connecting = (client, e) => { return EasyTask.CompletedTask; };//有客户端正在连接
service.Connected = (client, e) => { return EasyTask.CompletedTask; };//有客户端成功连接
service.Disconnecting = (client, e) => { return EasyTask.CompletedTask; };//有客户端正在断开连接，只有当主动断开时才有效。
service.Disconnected = (client, e) => { return EasyTask.CompletedTask; };//有客户端断开连接
service.Received = (client, e) =>
{
    //从客户端收到信息
    var mes = Encoding.UTF8.GetString(e.ByteBlock.Buffer, 0, e.ByteBlock.Len);//注意：数据长度是byteBlock.Len
    client.Logger.Info($"已从{client.Id}接收到信息：{mes}");
​
    client.Send(mes);//将收到的信息直接返回给发送方
​
    //client.Send("id",mes);//将收到的信息返回给特定ID的客户端
​
    //将收到的信息返回给在线的所有客户端。
    //注意：这里只是一个建议思路，实际上群发应该使用生产者消费者模式设计
    //var ids = service.GetIds();
    //foreach (var clientId in ids)
    //{
    //    if (clientId != client.Id)//不给自己发
    //    {
    //        service.Send(clientId, mes);
    //    }
    //}
​
    return EasyTask.CompletedTask;
};
​
service.Setup(new TouchSocketConfig()//载入配置
    .SetListenIPHosts("tcp://127.0.0.1:7789", 7790)//同时监听两个地址
    .ConfigureContainer(a =>//容器的配置顺序应该在最前面
    {
        a.AddConsoleLogger();//添加一个控制台日志注入（注意：在maui中控制台日志不可用）
    })
    .ConfigurePlugins(a =>
    {
        //a.Add();//此处可以添加插件
    }));
​
service.Start();//启动
```


### 3、TcpClient



```
TcpClient是Tcp系客户端基类，他直接参与tcp的连接、发送、接收、处理、断开等，他的业务与服务器的SocketClient是一一对应的。
```



```
var tcpClient = new TcpClient();
tcpClient.Connecting = (client, e) => { return EasyTask.CompletedTask; };//即将连接到服务器，此时已经创建socket，但是还未建立tcp
tcpClient.Connected = (client, e) => {return EasyTask.CompletedTask; };//成功连接到服务器
tcpClient.Disconnecting = (client, e) => {return EasyTask.CompletedTask; };//即将从服务器断开连接。此处仅主动断开才有效。
tcpClient.Disconnected = (client, e) => {return EasyTask.CompletedTask; };//从服务器断开连接，当连接不成功时不会触发。
tcpClient.Received = (client, e) =>
{
    //从服务器收到信息。但是一般byteBlock和requestInfo会根据适配器呈现不同的值。
    var mes = Encoding.UTF8.GetString(e.ByteBlock.Buffer, 0, e.ByteBlock.Len);
    tcpClient.Logger.Info($"客户端接收到信息：{mes}");
    return EasyTask.CompletedTask;
};
​
//载入配置
tcpClient.Setup(new TouchSocketConfig()
    .SetRemoteIPHost("127.0.0.1:7789")
    .ConfigureContainer(a =>
    {
        a.AddConsoleLogger();//添加一个日志注入
    }));
​
tcpClient.Connect();//调用连接，当连接不成功时，会抛出异常。
​
//Result result = tcpClient.TryConnect();//或者可以调用TryConnect
//if (result.IsSuccess())
//{
​
//}
​
tcpClient.Logger.Info("客户端成功连接");
​
tcpClient.Send("RRQM");
```


### 4、TcpClient 断线重连


在Config的插件配置中，使用重连插件即可。




```
.ConfigurePlugins(a=> 
{
   a.UseReconnection(5, true, 1000);//如需永远尝试连接，tryCount设置为-1即可。
});
```


## 项目案例


### 1、工程师软件工具箱


使用TouchRpc开发的一个内部工程师软件工具箱 。


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907165239715-1325523770.png)


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907165803155-1859945574.png)


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907165926095-1251909002.png)


### 2、远程监控、控制项目


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907170634483-1082539913.gif)


![](https://img2024.cnblogs.com/blog/576536/202409/576536-20240907170653827-410038086.gif)


## 项目地址


**GitHub：**[https://github.com/RRQM/TouchSocket](https://github.com)


**Gitee：**[https://gitee.com/RRQM\_Home/TouchSocket](https://github.com)


**文档地址：**[https://touchsocket.net/](https://github.com)


## 最后


如果你觉得这篇文章对你有帮助，不妨点个赞支持一下！你的支持是我继续分享知识的动力。如果有任何疑问或需要进一步的帮助，欢迎随时留言。


也可以加入微信公众号**\[DotNet技术匠]** 社区，与其他热爱技术的同行一起交流心得，共同成长！**优秀是一种习惯，欢迎大家留言学习！**


![](https://img2024.cnblogs.com/blog/576536/202408/576536-20240814113403514-910171896.png)


