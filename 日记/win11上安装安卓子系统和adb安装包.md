####  1. 先打开 Hyper-v  和 虚拟机平台
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124194116506-1883292289.png)
###### 然后输入 启用或关闭 Windows 功能
###### 将 Hyper-v  和 虚拟机平台 两个勾选
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124194257659-865755833.png)
######  注意： 完成后一定要重新启动

<br />

####  2. 准备工作
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124194634029-706192399.png)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124194640251-1267180720.png)

<br />

####  3. 下载 [安卓子系统](https://www.freedidi.com/2361.html)  或则在我的 阿里云盘里面 下载 win11安装安卓子系统和adb 文件夹

<br />

####  4. 安装 安卓子系统 首先将 子系统放在 win11的C盘根目录下
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124201437056-760142968.png)
```js
在 C盘的根目录下 运行 Windows PowerShell

在 Windows PowerShell 命令行里面输入 以下内容

方法一：  add-Appxpackage "MicrosoftCorporationII.WindowsSubsystemForAndroid_1.7.32815.0_neutral___8wekyb3d8bbwe.Msixbundle"

方法二：  Add-AppxPackage -Path "C:\MicrosoftCorporationII.WindowsSubsystemForAndroid_1.7.32815.0_neutral_8wekyb3d8bbwe.Msixbundle"  // 后面跟的是 安卓子系统的文件路径（绝对路径）

最后点击 enter 就会安装安卓子系统了
```
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124201907874-918643054.png)

<br />

####  5. 设置 安卓子系统
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124202130763-1325622031.png)

<br />

####  6. 安装 [adb 的命令包](https://www.freedidi.com/2350.html) 或则 我的 阿里云盘里面 下载 win11安装安卓子系统和adb 文件夹
```js
1. 下载完成后 解压 platform-tools_r31.0.3-windows

2. 解压后 将 platform-tools 里面的所有文件全部都 复制到 win11 C盘中 Windows 中

3.  测试 adb 是否安装成功 在桌面出打开 Windows PowerShell 窗口 输入
adb version
adb connect 127.0.0.1:58526  // 注意： 不一定都是 58526  查看自己的开发者模式查看端口号（一定要和自己电脑上的端口号一致）
adb devices
adb install .\tiktok.apk  // .\tiktok.apk  表示的是 自己下载的 apk 文件的 路径
```
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124203729213-236912261.png)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124203734630-1936211229.png)
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124203740604-854176753.png)

<br />

#### 7.  先要连接后才能下载，如下图 先要执行命令一才能安装成功
![](https://img2020.cnblogs.com/blog/2113686/202111/2113686-20211124204955999-244847968.png)