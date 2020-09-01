# frida_strategy
frida学习资料汇总
https://github.com/frida

## Installation

- 前期准备

  - 在 https://github.com/frida/frida/releases 上下载Android frida server

    x.x.x版本文件名格式： frida-server-x.x.x-android-arm64.xz

  - 将下载的文件解压，并重命名为frida-server（可以不重命名，只是为了后续方便）

  - Android手机需要root

  - PC和Android的frida版本需要保持一致

- PC安装frida客户端

```powershell
pip install frida
pip install frida-tools

#查看frida版本
frida --version
```

- Android手机安装frida server

```powershell
#将下载的frida server文件放到Android手机/data/local/tmp目录
adb pull frida-server /data/local/tmp

#设置端口转发
adb forward tcp:27042 tcp:27042
adb forward tcp:27043 tcp:27043

adb shell
...:$ su
...:# cd /data/local/tmp
...:/data/local/tmp# chmod 777 frida-server

#运行frida-server
...:/data/local/tmp# ./frida-server
```

- 测试

```powershell
#运行frida-server，在PC端运行frida-ps命令
frida-ps -U
```

## Demo

（TODO）

Hook Java层函数

Hook Native层函数

## Case Study
如何分析一个智能摄像头？
（TODO）

### 前期准备

### burpsuite流量分析

frida ssl-pinning-bypass

### Android app逆向

frida hook

### 固件分析


## Related Links
（侵删）
- [Frida如何打印参数具体内容](https://bbs.pediy.com/thread-253994.htm)
- [Frida脚本示例1 - ilovechocolate/FridaHook](https://github.com/ilovechocolate/FridaHook)
- [Frida脚本示例2 - m0bilesecurity/Frida-Mobile-Scripts](https://github.com/m0bilesecurity/Frida-Mobile-Scripts)
