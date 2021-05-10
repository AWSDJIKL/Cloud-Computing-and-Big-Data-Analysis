# mininet学习过程

## mininet安装

此处使用事先安装好mininet的虚拟机镜像

## mininet学习part1

- 打开wireshark和mininet

`sudo HOME=~wireshark & `

`sudo mn -x`

![](https://www.hualigs.cn/image/607ff703ec163.jpg)

- 节点之间互相ping

`h1 ping -c 1 h2`

`h2 ping -c 1 h1`
![](https://www.hualigs.cn/image/6088c6c792097.jpg)

`pingall`

![](https://www.hualigs.cn/image/6088c6c790e33.jpg)

- 运行一个简单的网络服务器和客户端样例

`h1 python3 -m http.server 80 &`

这里需要指定python3

`h2 wget -O -h1`

![](https://www.hualigs.cn/image/6088c8fa329ac.jpg)

- 结束

`h1 kill %python3`

![](https://www.hualigs.cn/image/6088c8fa15779.jpg)

`exit`

![](https://www.hualigs.cn/image/6088c8fa2d087.jpg)