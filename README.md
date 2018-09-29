# 基于串口的多蓝牙设备通信
## 目的
&nbsp;&nbsp;&nbsp;&nbsp;盼望着，盼望着，夏天即将过去。使用游戏本来编写程序，好处是显而易见的，弊端是也是显而易见的。</br>
`钢铁侠`里面有句话，让我印象深刻——`一切都可以由科技达成`。作为懂得一点点硬件知识的菜鸟程序员来说，我非常认同前面那句话。</br>
想法早已有之，缺的是买材料的银子和场地呀。然而，只要`贼心不死`，就没有办不到的事。</br>

这一整套控制系统由`Arduino开发板`、`mini Arduino`、`USB转TTL`、`蓝牙`、`BMP180`、`服务器级开关电源`和`涡轮风扇`组成。</br>
由本本上开的console输入命令，通过USB转串口连接到蓝牙`（master角色）`设备，它可以连接若干个蓝牙从机，由该蓝牙设备把指令发送给蓝牙从机</br>
1#从机用于测量当前环境的物理量，如温度，气压等。2#从机，连接涡轮风扇，根据指令控制涡轮风扇的转速，强制送风，实现降温效果。</br>
好久都没有和人说话了，可能表达的意思不完整 :-)，快递的一些电子产品还没有到，但是控制涡轮风扇的功能已经调试好了，先看看吧</br>
![image](https://github.com/Iflier/fanAndBLT/blob/master/images/1.jpg)</br>
涡轮风扇，很强大</br>
![image](https://github.com/Iflier/fanAndBLT/blob/master/images/2.jpg)</br>

## Update `2018.09.16`

缺的小东西买回来了，然后发现`master`设备并不能连接两个`slaver`设备，尽管已经修改了`master`设备的`INQM`选项。

## Update `2018.09.29`

当涡轮风扇的转速与计算机`CPU`平均利用率呈线性关系的时候，风扇的噪声比较大</br>
