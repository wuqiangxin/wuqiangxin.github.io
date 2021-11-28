####  转载:   [https://blog.csdn.net/weixin_39947908/article/details/109864326](https://blog.csdn.net/weixin_39947908/article/details/109864326)
</br>
<div class="rich_media_content" id="js_content"> 
  <p>win10系统是现在我们最喜欢的装机系统，但是很多用户们使用win10系统时会觉得卡顿等，那么我们要如何的对系统进行优化，才能让系统更加流畅呢，快来看看详细教程吧~</p>
</br>
  <h3><a name="t0"></a>win10优化设置教程：</h3>
  <p>1、<strong>禁用Windows Seach功能。</strong></p>
  <p>首先需要禁用Windows的搜索功能。首先打开菜单搜索"Windows 管理工具"</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/66789d8cf13a0141aba6f68c24a8a056.png" alt="66789d8cf13a0141aba6f68c24a8a056.png"></p>
  <p>进入管理界面后，点击：服务-Windows Search禁用，但windows firewall (windows防火墙服务)千万不能停用。</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/354450a254cc250029219744ae1a1b27.png" alt="354450a254cc250029219744ae1a1b27.png"></p>
  <p>可在控制面板里面的防火墙的“高级设置”里面的“属性”把“域配置文件”、“专用配置文件”、“公用配置文件”的状态改成关闭，这样就可以在不禁用防火墙服务的情况下关闭防火墙。</p>
  <p><br>2、<strong>关闭讨厌的第三方软件服务项</strong></p>
  <p>Win+ R输入“msconfig”→确定，服务→勾选隐藏所有的Microsoft服务去掉不需要执行的服务。</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/c761557698a224e8b2e110fd6252c20d.png" alt="c761557698a224e8b2e110fd6252c20d.png"></p>
  <p>3、<strong>关闭性能特效</strong>(配置不好的机器可以关闭)</p>
  <p>右键"此电脑"》属性》高级系统设置》高级》性能》设置》关闭淡出淡入效果。运行文件夹。</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/6e727a268479e87356fb2a902dbcda9a.png" alt="6e727a268479e87356fb2a902dbcda9a.png"></p>
  <p>4、<strong>清理产生的Windows.old文件夹</strong>(针对直接升级的系统)</p>
  <p>方案1：快捷键Win+X命令提示符，输入：rd X:windows.old /s(X代表盘符，可以写成C、D、E等)&nbsp;</p>
  <p>方案2(推荐)：C盘右键》属性》磁盘清理，选中以前的Windows安装复选框，确定清理。</p>
  <p>C盘–右键–属性-磁盘清理-选中以前的Windows 安装复选框–确定清理。</p>
  <p>5、<strong>设置好Superfetch服务</strong></p>
  <p>服务Superfetch启动类型改成延迟启动或禁用，可以避免Win10对硬盘的频繁访问。</p>
  <p>控制面板–管理工具–服务– Superfetch -启动类型–自动(延迟启动)。</p>
  <p>6、<strong>WindowsDefender 全盘扫描下系统，否则运行文件夹会卡顿</strong>。</p>
  <p>控制面板 Windows Defender “设置》实施保护”去掉勾和管理员，启用WindowsDefender去掉勾。</p>
  <p>服务WindowsDefenderService禁用。</p>
  <p>控制面板–Windows Defender –设置–实施保护-去掉勾和管理员–启用 Windows Defender –去掉勾。</p>
  <p>控制面板–管理工具–服务- Windows Defender Service禁用。</p>
  <p>7、<strong>关闭ipv6</strong></p>
  <p>部分网卡驱动开启ipv6会导致开机系统未响应，假死。</p>
  <p>网络共享中心》网络连接》以太网》属性》取消ipv6。(去掉钩钩)。</p>
  <p>8、<strong>WindowsDefender 全盘扫描下系统，否则运行文件夹会卡顿</strong></p>
  <p>控制面板 Windows Defender “设置》实施保护”去掉勾和管理员，启用WindowsDefender去掉勾。</p>
  <p>服务WindowsDefenderService禁用。</p>
  <p>控制面板–Windows Defender –设置–实施保护-去掉勾和管理员–启用 Windows Defender –去掉勾。</p>
  <p>控制面板–管理工具–服务- Windows Defender Service禁用。</p>
  <p>9、<strong>关闭windows安全中心服务</strong></p>
  <p>Win+R键 输入services.msc回车——找到SecurityCenter ，设置禁用。</p>
  <p>注意事项：请不要删除系统文件，优化后速度明显加快。</p>
  <p>10、<strong>设置Win10自动登陆，省去输入密码步骤</strong></p>
  <p>Win+R输入netplwiz取消使用计算机必需输入客户名和密码的选项，然后双击需要自动登录的账户，输入你的密码。</p>
  <p>或者在管理里面将自己建的客户删除，使用系统带的administrator客户，默认是直接进系统的。</p>
  <p>11、<strong>关闭计划任务里的隐藏的自启动程序</strong></p>
  <p>控制面板→所有控制面板项→管理工具→任务计划程序→任务计划程序库→右侧任务列表→禁用不需要的任务。</p>
  <p>12、<strong>Win10加速关机速度</strong></p>
  <p>Win+R键，输入 gpedit.msc。</p>
  <p>计算机管理中选择，模块管理 – 系统 — 关机选项，关闭会阻止或取消关机的应用程序的自动终止功能。</p>
  <p>13、<strong>win10加速开机速度</strong></p>
  <p>Win+ R – 输入msconfig – 引导 – 勾上无GUI引导，确定。</p>
  <p>14、<strong>开启HybridBoot</strong>(随个人喜好开启，开启会占C盘的部分容量)</p>
  <p>Win10启动飞快：控制面板》电源选项》选择电源按钮的功能，更改当前不可用的设置》关机设置》勾上启用快速启动。</p>
  <p>请先开启休眠：Win+R输入powercfg–h on，关闭休眠：powercfg –h off(关闭后C盘会空出几G的空间)。</p>
  <p>15、<strong>关闭磁盘碎片整理计划</strong></p>
  <p>磁盘碎片整理可以提高磁盘性能，但不需要整理计划，可以关闭整理计划。</p>
  <p>选中磁盘C-属性–工具–对驱动器进行优化和碎片整理–优化–更改设置–取消选择按计划执行。</p>
  <p>16、<strong>关闭家庭组</strong></p>
  <p>右键点击“此电脑”，选择“管理”，进入“计算机管理”窗口。</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/110aa3b4768115350185108f24d0c996.png" alt="110aa3b4768115350185108f24d0c996.png"></p>
  <p>在左侧的菜单选择“服务”，并在右侧找到“HomeGroup Listener”和“HomeGroup Provider”两个服务。</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/b7818f3150f85cba624252c6f9add581.png" alt="b7818f3150f85cba624252c6f9add581.png"></p>
  <p>右键点击它，选择“属性”，并在新打开的窗口中把启动类型改为“禁用”。</p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/f0bfce2a142eb6e39097df1594593170.png" alt="f0bfce2a142eb6e39097df1594593170.png"></p>
  <p><img src="https://img-blog.csdnimg.cn/img_convert/f746c693d4e8f1edcb57e09861b1dfb0.png" alt="f746c693d4e8f1edcb57e09861b1dfb0.png"></p>
  <p>这样，就关闭了“家庭组”功能。win8时代就有的家庭组功能会不断读写硬盘，造成硬盘占用高，这个问题在win10中依然存在。</p>
  <p>关闭这个功能会使硬盘占用大幅降低，不再出现动不动就占用100%的情况。(可在任务管理器中查看)</p>
