# 搭建 hexo 静态博客 教程
# 转载与 huanhao   https://www.cnblogs.com/huanhao/p/hexobase.html

<div id="cnblogs_post_body" class="blogpost-body cnblogs-markdown">
<span title-type="h1" class="header__span"><h1 id="基础篇搭建hexo博客一" class="header__dev"><b class="dev__fe"><i>1</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">【基础篇】搭建hexo博客（一）</span></b></h1></span><br>
<p>作者：Huanhao</p>
<p>bilibili：Mrhuanhao</p>
<span title-type="h1" class="header__span"><h1 id="前言" class="header__dev"><b class="dev__fe"><i>2</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">前言</span></b></h1></span><br>
<p>你是否想拥有属于自己的博客？你是否无奈与自己不会写网站而烦恼？</p>
<p>不要担心，本系列教程将会实现你白嫖的愿望，连服务器都不需要买，就算没有任何编程基础也可以学会的搭建博客教程</p>

<p>下面来看看这些好看的个人博客：</p>
<p><a href="http://fech.in/" target="_blank">http://fech.in/</a></p>
<p><a href="https://xaoxuu.com/" target="_blank">https://xaoxuu.com/</a></p>
<p><a href="https://nexmoe.com/" target="_blank">https://nexmoe.com/</a></p>
<p><a href="https://sakura.hojun.cn/" target="_blank">https://sakura.hojun.cn/</a></p>
<p>以上的博客你是否都心动了呢？我想说的是，它们都是由hexo搭建的，等你学完了基础和进阶篇，上面展示的博客你都可以实现，就让我们一步步来吧！</p>
<p>这是一个系列教程，有基础篇和进阶篇，让我们看看这两个教程实现的效果</p>
<ul>
<li>【基础篇】</li>
</ul>
<ol>
<li>
<p>学会安装相应需要的依赖软件</p>
</li>
<li>
<p>学会更换主题</p>
</li>
<li>
<p>学会基本的站点配置</p>
</li>
<li>
<p>知道怎么生成文章并编辑</p>
</li>
<li>
<p>上传你的博客并拥有一个可以访问的地址</p>
</li>
</ol>
<hr>
<ul>
<li>进阶篇</li>
</ul>
<ol>
<li>学会用markdown基本语法编写你的文章</li>
<li>学会如何搭建一个免费的图床并使用</li>
<li>学会进一步配置主题并了解所有主题的基本功能</li>
<li>拥有自己的域名并绑定</li>
<li>使用一些插件让自己博客更完美</li>
<li>备份</li>
</ol>
<hr>
<span title-type="h1" class="header__span"><h1 id="搭建之前的准备" class="header__dev"><b class="dev__fe"><i>3</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">搭建之前的准备</span></b></h1></span><br>
<span title-type="h2" class="header__span"><h2 id="安装nodejs" class="header__dev"><b class="dev__fe"><i>3</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>1</i></b><b class="dev__developer"><span class="dev__title">安装nodejs</span></b></h2></span><br>
<blockquote>
<p>下载地址： <a href="http://nodejs.cn/download/" target="_blank">http://nodejs.cn/download/</a></p>
</blockquote>
<p>选择windows安装包.msi安装</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-54-53.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-54-53.png" alt="" loading="lazy" class="medium-zoom-image"></a></p>
<p>运行安装包，我们默认选择c盘</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-49-21.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-49-21.png" alt="" loading="lazy" class="medium-zoom-image"></a></p>
<p>在这里选择Add to PATH然后点Next继续就行了</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-49-39.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-49-39.png" alt="" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h2" class="header__span"><h2 id="安装git" class="header__dev"><b class="dev__fe"><i>3</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>2</i></b><b class="dev__developer"><span class="dev__title">安装Git</span></b></h2></span><br>
<blockquote>
<p>下载地址：<a href="https://git-scm.com/" target="_blank">https://git-scm.com/</a></p>
</blockquote>
<p>点这里即可下载最新版本，如果你的下载速度比较慢可以选择下面的链接下载</p>
<blockquote>
<p><a href="https://www.lanzous.com/i9s7tib" target="_blank">https://www.lanzous.com/i9s7tib</a></p>
</blockquote>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-57-32.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_08-57-32.png" alt="" loading="lazy" class="medium-zoom-image"></a></p>
<p>运行安装包，选择合适的安装位置，然后点Next</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_09-01-49.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/gtd/Snipaste_2020-02-29_09-01-49.png" alt="" loading="lazy" class="medium-zoom-image"></a></p>
<p>后面的安装步骤全部只要点Next就行了，不需要我们多余配置</p>
<p><a data-fancybox="gallery" href="https://i.loli.net/2020/02/29/jqTCDk6YSbwQOVz.png"><img src="https://i.loli.net/2020/02/29/jqTCDk6YSbwQOVz.png" alt="Snipaste_2020-02-29_09-02-25.png" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h2" class="header__span"><h2 id="验证nodejs是否安装配置成功" class="header__dev"><b class="dev__fe"><i>3</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>3</i></b><b class="dev__developer"><span class="dev__title">验证nodejs是否安装配置成功</span></b></h2></span><br>
<p>我们安装完Git后，在桌面右键会有Git Bash Here，我们直接点开</p>
<p><a data-fancybox="gallery" href="https://i.loli.net/2020/02/29/s1YhxtEILOlk4Xz.png"><img src="https://i.loli.net/2020/02/29/s1YhxtEILOlk4Xz.png" alt="Snipaste_2020-02-29_09-05-54.png" loading="lazy"></a></p>
<p>会出来一个终端，我们分别执行下面的命令</p>
<code-box id="tWFAWz" style="position: relative;display: block;"><button code-id="tWFAWz" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=tWFAWz]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="tWFAWz" class="hljs crmsh mCustomScrollbar _mCS_1 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_1" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_1_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-6GWmma"><code-line class="line-numbers-rows"></code-line>$ <span class="hljs-keyword">node</span> <span class="hljs-title">-v</span>
<code-line class="line-numbers-rows"></code-line>$ npm -v
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_1_scrollbar_vertical" class="mCSB_scrollTools mCSB_1_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_1_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_1_scrollbar_horizontal" class="mCSB_scrollTools mCSB_1_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_1_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>如果输出了版本号，那么证明配置成功，如果没有版本号，请重新安装nodejs（检查是否勾选Add to Path），或者手动为nodejs添加环境变量</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/213.ophl1x6e4sp.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/213.ophl1x6e4sp.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h2" class="header__span"><h2 id="安装cnpm" class="header__dev"><b class="dev__fe"><i>3</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>4</i></b><b class="dev__developer"><span class="dev__title">安装cnpm</span></b></h2></span><br>
<p>在git bash里面执行下面的命令</p>
<code-box id="XXTSHp" style="position: relative;display: block;"><button code-id="XXTSHp" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=XXTSHp]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="XXTSHp" class="hljs coffeescript mCustomScrollbar _mCS_2 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_2" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_2_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-CimQnE"><code-line class="line-numbers-rows"></code-line>$ <span class="hljs-built_in">npm</span> install -g cnpm --registry=https:<span class="hljs-regexp">//</span>registry.<span class="hljs-built_in">npm</span>.taobao.org
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_2_scrollbar_vertical" class="mCSB_scrollTools mCSB_2_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_2_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_2_scrollbar_horizontal" class="mCSB_scrollTools mCSB_2_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_2_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p><strong>检查cnpm是否安装成功</strong></p>
<p>执行</p>
<code-box id="a6Q357" style="position: relative;display: block;"><button code-id="a6Q357" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=a6Q357]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="a6Q357" class="hljs elixir mCustomScrollbar _mCS_3 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_3" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_3_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-ih4ASn"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>cnpm -v 
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_3_scrollbar_vertical" class="mCSB_scrollTools mCSB_3_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_3_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_3_scrollbar_horizontal" class="mCSB_scrollTools mCSB_3_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_3_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>如果输出版本号就是安装成功了</p>
<hr>
<span title-type="h1" class="header__span"><h1 id="安装hexo和初始化博客" class="header__dev"><b class="dev__fe"><i>4</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">安装hexo和初始化博客</span></b></h1></span><br>
<span title-type="h2" class="header__span"><h2 id="安装hexo" class="header__dev"><b class="dev__fe"><i>4</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>1</i></b><b class="dev__developer"><span class="dev__title">安装hexo</span></b></h2></span><br>
<p>在git bash执行下面的命令安装hexo</p>
<code-box id="jPjQ8i" style="position: relative;display: block;"><button code-id="jPjQ8i" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=jPjQ8i]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="jPjQ8i" class="hljs avrasm mCustomScrollbar _mCS_4 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_4" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_4_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-Hf74mc"><code-line class="line-numbers-rows"></code-line>$ cnpm install hexo-<span class="hljs-keyword">cli</span> -g
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_4_scrollbar_vertical" class="mCSB_scrollTools mCSB_4_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_4_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_4_scrollbar_horizontal" class="mCSB_scrollTools mCSB_4_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_4_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<span title-type="h2" class="header__span"><h2 id="初始化博客" class="header__dev"><b class="dev__fe"><i>4</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>2</i></b><b class="dev__developer"><span class="dev__title">初始化博客</span></b></h2></span><br>
<p>选择一个文件夹，然后右键打开git bash</p>
<p>例如：我在F盘新建了一个blog文件夹，就在blog文件夹下打开git bash</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-23-38.xgw9p9u10qr.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-23-38.xgw9p9u10qr.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后这里会显示你当前目录</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-25-37.w75xfc7uqwj.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-25-37.w75xfc7uqwj.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后执行</p>
<code-box id="3xj76Q" style="position: relative;display: block;"><button code-id="3xj76Q" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=3xj76Q]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="3xj76Q" class="hljs elixir mCustomScrollbar _mCS_5 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_5" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_5_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-d4cxWW"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>hexo init
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_5_scrollbar_vertical" class="mCSB_scrollTools mCSB_5_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_5_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_5_scrollbar_horizontal" class="mCSB_scrollTools mCSB_5_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_5_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>到<code>Install dependencies</code>的时候你可能会卡住，这是大多数人基本都会遇到的</p>
<p>我们只需要在这里的时候结束命令，按<code>Ctrl + c</code>就可以结束命令</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-27-37.79mebxnx3oa.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-27-37.79mebxnx3oa.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后执行下面这个命令，就可以使用国内的镜像为你完成博客的初始化工作</p>
<code-box id="J7XFDG" style="position: relative;display: block;"><button code-id="J7XFDG" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=J7XFDG]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="J7XFDG" class="hljs cmake mCustomScrollbar _mCS_6 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_6" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_6_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-8CYw58"><code-line class="line-numbers-rows"></code-line>$ cnpm <span class="hljs-keyword">install</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_6_scrollbar_vertical" class="mCSB_scrollTools mCSB_6_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_6_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_6_scrollbar_horizontal" class="mCSB_scrollTools mCSB_6_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_6_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<blockquote>
<p>其他方法：</p>
<p>git clone <a href="https://e.coding.net/huanhao/hexoblog.git" target="_blank">https://e.coding.net/huanhao/hexoblog.git</a></p>
<p>cnpm install</p>
</blockquote>
<p>然后继续下面的步骤</p>
<p>等待命令完成后，就完成了初始化，现在就可以预览我们的博客了</p>
<p>执行下面这个命令</p>
<p><code>注意：请不要结束命令或者关闭终端</code></p>
<code-box id="iEmDZs" style="position: relative;display: block;"><button code-id="iEmDZs" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=iEmDZs]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="iEmDZs" class="hljs elixir mCustomScrollbar _mCS_7 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_7" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_7_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-hDRtKX"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>hexo s
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_7_scrollbar_vertical" class="mCSB_scrollTools mCSB_7_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_7_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_7_scrollbar_horizontal" class="mCSB_scrollTools mCSB_7_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_7_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-31-47.jmi628mj35e.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-31-47.jmi628mj35e.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后会出来一段http开头的网址，我们复制下来然后在浏览器打开</p>
<p>就会出现这么一个页面了</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-33-55.tyszma65r9.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-33-55.tyszma65r9.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h1" class="header__span"><h1 id="更换主题" class="header__dev"><b class="dev__fe"><i>5</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">更换主题</span></b></h1></span><br>
<p>你是否觉得上面的默认主题有点不好看呢？现在教你如何替换主题</p>
<p>hexo的所有主题都在下面这个地址：</p>
<blockquote>
<p><a href="https://hexo.io/themes/" target="_blank">https://hexo.io/themes/</a></p>
</blockquote>
<p>你可能会在这个地址看到很多好看的主题，但是我们要慢慢来，有些主题的配置难度还是很高的</p>
<p>我们要找一个功能齐全，配置简单的主题练练手</p>
<p>就是这个新手入门hexo必备的Next主题</p>
<blockquote>
<p>预览效果：<a href="https://theme-next.org/" target="_blank">https://theme-next.org/</a></p>
<p>项目地址：<a href="https://github.com/theme-next/hexo-theme-next" target="_blank">https://github.com/theme-next/hexo-theme-next</a></p>
<p>配置文档：<a href="https://theme-next.org/docs/getting-started/" target="_blank">https://theme-next.org/docs/getting-started/</a></p>
</blockquote>
<p>如你所见，其实每个主题都会包含这个三个东西</p>
<ul>
<li>预览效果</li>
<li>项目地址</li>
<li>配置文档</li>
</ul>
<p>点击主题的图片可以打开预览地址，点击主题的标题可以打开项目地址</p>
<p>配置文档我们需要自己去项目地址找，大多数主题的项目地址都是英文，大家可以开翻译找一下</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-40-40.h10pzhd3ikj.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-40-40.h10pzhd3ikj.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h2" class="header__span"><h2 id="如何下载主题" class="header__dev"><b class="dev__fe"><i>5</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>1</i></b><b class="dev__developer"><span class="dev__title">如何下载主题</span></b></h2></span><br>
<h3 id="方法1">方法1<button class="cnblogs-toc-button" title="显示目录导航" aria-expanded="false"></button></h3>
<p>打开主题的项目地址后，点击<code>Clone or download</code></p>
<p>然后复制https开头的地址</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-46-02.gnmyl5b7s2.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-46-02.gnmyl5b7s2.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后在你的博客文件夹下面打开git bash</p>
<p>执行：</p>
<code-box id="zJJKHP" style="position: relative;display: block;"><button code-id="zJJKHP" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=zJJKHP]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="zJJKHP" class="hljs crmsh mCustomScrollbar _mCS_8 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_8" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_8_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-ZWGaiB"><code-line class="line-numbers-rows"></code-line>git <span class="hljs-keyword">clone</span> <span class="hljs-title">复制的地址 themes</span>/主题名字
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_8_scrollbar_vertical" class="mCSB_scrollTools mCSB_8_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_8_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_8_scrollbar_horizontal" class="mCSB_scrollTools mCSB_8_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_8_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>如图：</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-50-23.o7ukcdqwa8e.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-50-23.o7ukcdqwa8e.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>现在给你解释一下这个命令</p>
<p>git clone 代表克隆，后面接上一串下载地址，最后面的themes/next是把文件夹下载到主题目录下，并把主题文件命名为next</p>
<hr>
<h3 id="方法2">方法2<button class="cnblogs-toc-button" title="显示目录导航" aria-expanded="false"></button></h3>
<p>如果你觉得比较麻烦，还有第二个办法</p>
<p>打开主题项目地址，然后点击<code>Clone or download</code>，然后点击Download ZIP</p>
<p>这样可以下载主题文件压缩包，前提是你已经登入了github（没有账号的，请自己注册一下）</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-53-14.hd54gibpilh.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-53-14.hd54gibpilh.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后解压压缩包，把文件夹放在博客目录下的themes目录，并把文件夹命名为主题的名字</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-56-33.xhx8o5z5d9.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_09-56-33.xhx8o5z5d9.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h2" class="header__span"><h2 id="修改配置文件" class="header__dev"><b class="dev__fe"><i>5</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>2</i></b><b class="dev__developer"><span class="dev__title">修改配置文件</span></b></h2></span><br>
<p>在博客的目录下有一个叫<code>_config.yml</code>的文件</p>
<p>将它打开</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-01-51.gwst228nama.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-01-51.gwst228nama.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>找到<code>themes</code>这一行，然后将主题名字修改为next</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-02-23.58o49hkjdki.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-02-23.58o49hkjdki.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>这样的话，主题就成功更换了</p>
<hr>
<span title-type="h2" class="header__span"><h2 id="预览主题" class="header__dev"><b class="dev__fe"><i>5</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>3</i></b><b class="dev__developer"><span class="dev__title">预览主题</span></b></h2></span><br>
<p>在博客目录打开git bash</p>
<p>执行</p>
<code-box id="Yb5KK2" style="position: relative;display: block;"><button code-id="Yb5KK2" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=Yb5KK2]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="Yb5KK2" class="hljs ebnf mCustomScrollbar _mCS_9 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_9" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_9_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-CAR4AF"><code-line class="line-numbers-rows"></code-line><span class="hljs-attribute">hexo s</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_9_scrollbar_vertical" class="mCSB_scrollTools mCSB_9_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_9_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_9_scrollbar_horizontal" class="mCSB_scrollTools mCSB_9_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_9_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>还是会出现一段浏览地址，我们在浏览器打开就行了</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-04-16.2dvd68y21dm.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-04-16.2dvd68y21dm.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<blockquote>
<p>注意：有些主题你更换之后是暂时无法预览的，因为有的主题还需要安装它需要的依赖，这一般都会在主题的文档里面提到，只有安装它的依赖之后才可以正常预览，这里暂时不做说明，会在hexo教程进阶篇说到</p>
</blockquote>
<hr>
<span title-type="h1" class="header__span"><h1 id="配置主题" class="header__dev"><b class="dev__fe"><i>6</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">配置主题</span></b></h1></span><br>
<p>这里不会做详细的配置介绍，在进阶篇会完整说明</p>
<p>我们需要认识两个文件</p>
<ul>
<li>站点配置文件</li>
</ul>
<p>指的是博客根目录下的<code>_config.yml</code></p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-01-51.gwst228nama.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-01-51.gwst228nama.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<ul>
<li>主题配置文件</li>
</ul>
<p>指的是某个主题下的<code>_config.yml</code></p>
<p>它们的名字都叫<code>_config.yml</code>但是你不能弄混淆</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-11-13.qayjeoclrer.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-11-13.qayjeoclrer.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>在我们看主题文档配置的时候，是必须要分清这两个概念的，不然会报错</p>
<p>我们先来几个基本的配置</p>
<span title-type="h2" class="header__span"><h2 id="设置语言" class="header__dev"><b class="dev__fe"><i>6</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>1</i></b><b class="dev__developer"><span class="dev__title">设置语言</span></b></h2></span><br>
<p>在Next主题的文档里面提到了如何更换语言</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-45-34.i8xhol7d05.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-45-34.i8xhol7d05.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>它要求我们更改的是站点配置文件，并且给出了代码示范</p>
<p>我们打开站点配置文件</p>
<p>按照要求，将language的配置改成zh-CN，然后保存文件</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-46-29.tuonuuuk6mm.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-46-29.tuonuuuk6mm.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<span title-type="h2" class="header__span"><h2 id="其他设置" class="header__dev"><b class="dev__fe"><i>6</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>2</i></b><b class="dev__developer"><span class="dev__title">其他设置</span></b></h2></span><br>
<p>现在再来尝试一个</p>
<p>Next主题里面有个Scheme选项，可以更改主题的外观</p>
<p>根据要求，我们需要更改的是主题配置文件</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-47-13.9mpo8qnzty.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-47-13.9mpo8qnzty.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>打开主题配置文件，我们尝试scheme改成双栏，也就是需要修改成Pisces</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-22-06.eq6mi8hrlka.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-22-06.eq6mi8hrlka.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>现在已经修改过两个配置了，为了检验是否修改成功，我们需要预览一下主题</p>
<p>在博客根目录下执行</p>
<code-box id="mfRrfP" style="position: relative;display: block;"><button code-id="mfRrfP" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=mfRrfP]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="mfRrfP" class="hljs ebnf mCustomScrollbar _mCS_10 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_10" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_10_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-JHsb2Z"><code-line class="line-numbers-rows"></code-line><span class="hljs-attribute">hexo s</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_10_scrollbar_vertical" class="mCSB_scrollTools mCSB_10_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_10_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_10_scrollbar_horizontal" class="mCSB_scrollTools mCSB_10_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_10_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>然后打开链接</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-49-17.j0ojrtmb8xm.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_10-49-17.j0ojrtmb8xm.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>可以看到都设置成功了</p>
<p>因为这个主题的主题文档是英文的，所以可能配置起来不太方便，我这里有一个中文的</p>
<p>是别人翻译的，不过现在不是最新版本的翻译</p>
<blockquote>
<p><a href="http://theme-next.iissnan.com/" target="_blank">http://theme-next.iissnan.com/</a></p>
</blockquote>
<p>如果你有能力，可以自己挑一个主题进行简单配置，在进阶篇中会使用其他主题为你展示更详细的配置教程</p>
<hr>
<span title-type="h1" class="header__span"><h1 id="生成文章的编辑工具" class="header__dev"><b class="dev__fe"><i>7</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">生成文章的编辑工具</span></b></h1></span><br>
<p>在博客根目录下面执行：</p>
<code-box id="45ThDf" style="position: relative;display: block;"><button code-id="45ThDf" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=45ThDf]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="45ThDf" class="hljs actionscript mCustomScrollbar _mCS_11 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_11" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_11_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-XiMrbG"><code-line class="line-numbers-rows"></code-line>$ hexo <span class="hljs-keyword">new</span> <span class="hljs-string">"文章链接"</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_11_scrollbar_vertical" class="mCSB_scrollTools mCSB_11_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_11_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_11_scrollbar_horizontal" class="mCSB_scrollTools mCSB_11_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_11_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>例如：你想创建一个名为”我的第一个博客“的文章</p>
<p>可以执行：</p>
<code-box id="BrcPXm" style="position: relative;display: block;"><button code-id="BrcPXm" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=BrcPXm]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="BrcPXm" class="hljs actionscript mCustomScrollbar _mCS_12 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_12" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_12_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-KMjHi4"><code-line class="line-numbers-rows"></code-line>$ hexo <span class="hljs-keyword">new</span> <span class="hljs-string">"my-first-blog"</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_12_scrollbar_vertical" class="mCSB_scrollTools mCSB_12_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_12_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_12_scrollbar_horizontal" class="mCSB_scrollTools mCSB_12_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_12_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>文章链接建议是英文，然后会显示你的文章生成的目录，每次生成的文章都固定在你的博客根目录下面的source/_posts下</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-10-30.ybyovivc8lp.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-10-30.ybyovivc8lp.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>可以看到是一个后缀为.md的文件，这个其实是一个markdown文件，如果你不知道markdown是什么，在进阶篇会告诉你，就算你不会markdown，你可以暂时把这个当成txt文件</p>
<p>我建议你安装Typora编辑.md文件</p>
<blockquote>
<p><a href="https://www.typora.io/" target="_blank">https://www.typora.io/</a></p>
</blockquote>
<p>按照目录打开my-firsy-blog.md文件，可以看到一个横线上面有一段信息</p>
<p>这里面是存放你博客信息的地方</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-16-37.oun3i88bw.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-16-37.oun3i88bw.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<ul>
<li>title 文章标题</li>
<li>date 文章日期</li>
<li>tag 文章标签 （暂时不说明如何配置，进阶篇会讲到）</li>
</ul>
<p>然后这时候你可以修改文章标题，并且在横线下面输入你文章的内容</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-17-14.7x7sfa9t9m8.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-17-14.7x7sfa9t9m8.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>保存之后，你可以在博客根目录打开git bash</p>
<p>执行</p>
<code-box id="W6nxdT" style="position: relative;display: block;"><button code-id="W6nxdT" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=W6nxdT]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="W6nxdT" class="hljs elixir mCustomScrollbar _mCS_13 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_13" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_13_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-wPWAMi"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>hexo s
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_13_scrollbar_vertical" class="mCSB_scrollTools mCSB_13_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_13_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_13_scrollbar_horizontal" class="mCSB_scrollTools mCSB_13_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_13_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>记得：预览博客都是这个命令</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-22-11.eoh9owyqu4j.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-22-11.eoh9owyqu4j.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<span title-type="h1" class="header__span"><h1 id="部署你的博客" class="header__dev"><b class="dev__fe"><i>8</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>0</i></b><b class="dev__developer"><span class="dev__title">部署你的博客</span></b></h1></span><br>
<p>现在我们的博客都是只能本地预览，如何将我们的上传到一个地方，然后通过域名访问呢？</p>
<p>你可能觉得需要一个服务器再买个域名绑定，我可以告诉你都不需要</p>
<p>下面介绍两种部署方法</p>
<p>先来个对比</p>
<p><strong>github：</strong></p>
<ul>
<li>国外网站，是英文</li>
<li>访问速度较慢</li>
<li>不需要实名认证</li>
<li>域名形式可以自定义</li>
</ul>
<p><strong>coding：</strong></p>
<ul>
<li>国内的平台，网站是中文</li>
<li>访问速度快</li>
<li>部署网站需要实名认证，只需要填写身份证号即可</li>
<li>域名是随机给的，所以很长而且不能自定义</li>
</ul>
<p>如果你有自己的域名，github和coding都可以绑定域名</p>
<span title-type="h2" class="header__span"><h2 id="coding" class="header__dev"><b class="dev__fe"><i>8</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>1</i></b><b class="dev__developer"><span class="dev__title">coding</span></b></h2></span><br>
<blockquote>
<p><a href="https://coding.net/user" target="_blank">https://coding.net/user</a></p>
</blockquote>
<p>注册一个coding的账号，这里不做演示</p>
<p>然后按照图片新建一个项目</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-25-47.8py42ifi1g3.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-25-47.8py42ifi1g3.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>选择devops</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-25-58.sm3tn54wui.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-25-58.sm3tn54wui.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>填入相关信息，记得勾选<strong><code>启用README.cd文件初始化项目</code></strong></p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-26-29.u2pyq6c928.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-26-29.u2pyq6c928.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后完成创建</p>
<hr>
<blockquote>
<p>我们暂时不能直接上传，需要进行一些配置，如下：</p>
</blockquote>
<p>接下来需要我们创建一个git秘钥</p>
<p>打开git bash（不要求在哪个目录）</p>
<p>执行： “这里面是你的邮箱”</p>
<p>不管出现什么信息，你只需要回车就可以了</p>
<code-box id="Hs8nhr" style="position: relative;display: block;"><button code-id="Hs8nhr" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=Hs8nhr]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="Hs8nhr" class="hljs elixir mCustomScrollbar _mCS_14 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_14" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_14_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-TEh6W4"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>ssh-keygen -t rsa -C “your_email<span class="hljs-variable">@youremail</span>.com“
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_14_scrollbar_vertical" class="mCSB_scrollTools mCSB_14_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_14_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_14_scrollbar_horizontal" class="mCSB_scrollTools mCSB_14_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_14_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>然后执行</p>
<code-box id="RenPGm" style="position: relative;display: block;"><button code-id="RenPGm" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=RenPGm]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="RenPGm" class="hljs elixir mCustomScrollbar _mCS_15 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_15" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_15_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-TsGt4m"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>cat ~<span class="hljs-regexp">/.ssh/id</span>_rsa.pub
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_15_scrollbar_vertical" class="mCSB_scrollTools mCSB_15_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_15_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_15_scrollbar_horizontal" class="mCSB_scrollTools mCSB_15_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_15_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>会输出你的秘钥，我们复制输出信息就行了</p>
<p>然后点击头像，打开个人设置--选择SSH公钥--新增公钥</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-33-54.hlvuud9w9ns.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-33-54.hlvuud9w9ns.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后将你复制的秘钥粘贴进去，记得勾选永久有效</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-34-42.zd3za7e4a6e.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-34-42.zd3za7e4a6e.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<hr>
<p>然后打开git bash</p>
<p>执行：</p>
<code-box id="3GRZrA" style="position: relative;display: block;"><button code-id="3GRZrA" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=3GRZrA]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="3GRZrA" class="hljs stylus mCustomScrollbar _mCS_16 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_16" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_16_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-FrhSH5"><code-line class="line-numbers-rows"></code-line>$  ssh -T git@git<span class="hljs-selector-class">.coding</span><span class="hljs-selector-class">.net</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_16_scrollbar_vertical" class="mCSB_scrollTools mCSB_16_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_16_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_16_scrollbar_horizontal" class="mCSB_scrollTools mCSB_16_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_16_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>会提示你下面这个，输入yes回车就行了</p>
<code-box id="EpRafP" style="position: relative;display: block;"><button code-id="EpRafP" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=EpRafP]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="EpRafP" class="hljs livescript mCustomScrollbar _mCS_17 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_17" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_17_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-AHAp55"><code-line class="line-numbers-rows"></code-line>Are you sure you want <span class="hljs-keyword">to</span> <span class="hljs-keyword">continue</span> connecting (<span class="hljs-literal">yes</span><span class="hljs-regexp">/no/</span>[fingerprint])? 
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_17_scrollbar_vertical" class="mCSB_scrollTools mCSB_17_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_17_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_17_scrollbar_horizontal" class="mCSB_scrollTools mCSB_17_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_17_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<hr>
<p>接下来打开你的项目选择SSH，然后复制右边git开头的地址</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-38-33.r8subsc5h7k.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-38-33.r8subsc5h7k.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>打开站点配置文件</p>
<p>修改deploy信息</p>
<code-box id="fMQhsB" style="position: relative;display: block;"><button code-id="fMQhsB" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=fMQhsB]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="fMQhsB" class="hljs dts mCustomScrollbar _mCS_18 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_18" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_18_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-Dyke4k"><code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">deploy:</span>
<code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">  type:</span> git
<code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">  repo:</span> 你复制的地址
<code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">  branch:</span> master
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_18_scrollbar_vertical" class="mCSB_scrollTools mCSB_18_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_18_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_18_scrollbar_horizontal" class="mCSB_scrollTools mCSB_18_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_18_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>例如：</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-44-14.it2uh45m4jq.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-44-14.it2uh45m4jq.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>在博客根目录下打开git bash</p>
<p>分别执行下面的命令：</p>
<p>yourname是你的名字</p>
<p>youremail是你的邮箱</p>
<code-box id="s2RSJn" style="position: relative;display: block;"><button code-id="s2RSJn" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=s2RSJn]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="s2RSJn" class="hljs routeros mCustomScrollbar _mCS_19 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_19" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_19_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-anpjnr"><code-line class="line-numbers-rows"></code-line>$ git<span class="hljs-built_in"> config </span>--global user.name <span class="hljs-string">"yourname"</span>
<code-line class="line-numbers-rows"></code-line>$ git<span class="hljs-built_in"> config </span>--global user.email <span class="hljs-string">"youremail"</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_19_scrollbar_vertical" class="mCSB_scrollTools mCSB_19_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_19_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_19_scrollbar_horizontal" class="mCSB_scrollTools mCSB_19_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_19_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>然后安装上传插件</p>
<code-box id="p4FwXD" style="position: relative;display: block;"><button code-id="p4FwXD" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=p4FwXD]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="p4FwXD" class="hljs sql mCustomScrollbar _mCS_20 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_20" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_20_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-ZDy4CN"><code-line class="line-numbers-rows"></code-line>cnpm <span class="hljs-keyword">install</span> hexo-deployer-git <span class="hljs-comment">--save</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_20_scrollbar_vertical" class="mCSB_scrollTools mCSB_20_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_20_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_20_scrollbar_horizontal" class="mCSB_scrollTools mCSB_20_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_20_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<hr>
<h3 id="上传">上传<button class="cnblogs-toc-button" title="显示目录导航" aria-expanded="false"></button></h3>
<blockquote>
<p>以上的配置完成之后，就可以上传了</p>
</blockquote>
<p>在博客根目录下打开git bash，执行下面的命令就可以上传了</p>
<code-box id="knCkMN" style="position: relative;display: block;"><button code-id="knCkMN" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=knCkMN]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="knCkMN" class="hljs ebnf mCustomScrollbar _mCS_21 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_21" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_21_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-HDRHd8"><code-line class="line-numbers-rows"></code-line><span class="hljs-attribute">hexo g -d</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_21_scrollbar_vertical" class="mCSB_scrollTools mCSB_21_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_21_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_21_scrollbar_horizontal" class="mCSB_scrollTools mCSB_21_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_21_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-49-05.lkmgvzcdzwh.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-49-05.lkmgvzcdzwh.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后打开项目，打开构建与部署--静态网站--立即发布静态网站</p>
<blockquote>
<p>注意：coding需要实名认证，只需要你输入身份证号就可以了，不用担心泄露隐私，因为coding现在是腾讯的</p>
</blockquote>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-50-05.b57ma6w5win.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-50-05.b57ma6w5win.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>我们只要填写网站名称就行了，然后保存</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-50-36.6fwfau0xu0w.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-50-36.6fwfau0xu0w.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>因为是刚构建的网站，所以要手动部署一下，以后上传就不需要手动部署</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-55-02.ki4y7hiyo2b.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-55-02.ki4y7hiyo2b.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后访问所给的地址，那个就是我们网站的地址了</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-56-21.b5y903lp4hk.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-56-21.b5y903lp4hk.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>之后每次修改完博客要上传的时候，只需执行上传命令</p>
<span title-type="h2" class="header__span"><h2 id="github部署" class="header__dev"><b class="dev__fe"><i>8</i></b><span class="dev__slash">|</span><b class="dev__ux"><i>2</i></b><b class="dev__developer"><span class="dev__title">github部署</span></b></h2></span><br>
<p>你还可以使用github部署你的博客</p>
<p>这里不演示如何注册账号</p>
<p>创建一个仓库</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-49-41.bjily8bk23.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-49-41.bjily8bk23.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>仓库名必须是用户名 + .github.io</p>
<p>然后勾选初始化README</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-51-22.58hhw0be4f9.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-51-22.58hhw0be4f9.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<blockquote>
<p>我们暂时不能直接上传，需要进行一些配置，如下：</p>
</blockquote>
<p>接下来需要我们创建一个git秘钥</p>
<p>打开git bash（不要求在哪个目录）</p>
<p>执行： “这里面是你的邮箱”</p>
<p>不管出现什么信息，你只需要回车就可以了</p>
<code-box id="J37M6j" style="position: relative;display: block;"><button code-id="J37M6j" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=J37M6j]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="J37M6j" class="hljs elixir mCustomScrollbar _mCS_22 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_22" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_22_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-RwWDiR"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>ssh-keygen -t rsa -C “your_email<span class="hljs-variable">@youremail</span>.com“
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_22_scrollbar_vertical" class="mCSB_scrollTools mCSB_22_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_22_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_22_scrollbar_horizontal" class="mCSB_scrollTools mCSB_22_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_22_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>然后执行</p>
<code-box id="itwHD3" style="position: relative;display: block;"><button code-id="itwHD3" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=itwHD3]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="itwHD3" class="hljs elixir mCustomScrollbar _mCS_23 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_23" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_23_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-DSbsiE"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span>cat ~<span class="hljs-regexp">/.ssh/id</span>_rsa.pub
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_23_scrollbar_vertical" class="mCSB_scrollTools mCSB_23_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_23_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_23_scrollbar_horizontal" class="mCSB_scrollTools mCSB_23_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_23_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>会输出你的秘钥，我们复制输出信息就行了</p>
<p>然后点击头像，点击Settings--SSH·····--New SSH Key</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-53-12.bnffwtcf66a.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-53-12.bnffwtcf66a.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>粘贴你复制的秘钥</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-55-05.lakxr64606k.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_14-55-05.lakxr64606k.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后打开git bash</p>
<p>执行：</p>
<code-box id="x7m4jW" style="position: relative;display: block;"><button code-id="x7m4jW" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=x7m4jW]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="x7m4jW" class="hljs elixir mCustomScrollbar _mCS_24 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_24" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_24_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-8tMeXj"><code-line class="line-numbers-rows"></code-line><span class="hljs-variable">$ </span> ssh -T git<span class="hljs-variable">@github</span>.com
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_24_scrollbar_vertical" class="mCSB_scrollTools mCSB_24_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_24_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_24_scrollbar_horizontal" class="mCSB_scrollTools mCSB_24_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_24_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>会提示你下面这个，输入yes回车就行了</p>
<code-box id="wiQKe4" style="position: relative;display: block;"><button code-id="wiQKe4" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=wiQKe4]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="wiQKe4" class="hljs livescript mCustomScrollbar _mCS_25 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_25" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_25_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-Dyy2iN"><code-line class="line-numbers-rows"></code-line>Are you sure you want <span class="hljs-keyword">to</span> <span class="hljs-keyword">continue</span> connecting (<span class="hljs-literal">yes</span><span class="hljs-regexp">/no/</span>[fingerprint])? 
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_25_scrollbar_vertical" class="mCSB_scrollTools mCSB_25_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_25_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_25_scrollbar_horizontal" class="mCSB_scrollTools mCSB_25_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_25_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>打开项目，点击绿色按钮，点击Use SSH</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-01-31.omf9nqgs46i.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-01-31.omf9nqgs46i.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>复制git开头的地址</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-01-38.kjtg51f14z.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-01-38.kjtg51f14z.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>打开站点配置文件</p>
<p>修改deploy信息</p>
<code-box id="FRnhCz" style="position: relative;display: block;"><button code-id="FRnhCz" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=FRnhCz]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="FRnhCz" class="hljs dts mCustomScrollbar _mCS_26 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_26" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_26_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-h5pbjy"><code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">deploy:</span>
<code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">  type:</span> git
<code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">  repo:</span> 你复制的地址
<code-line class="line-numbers-rows"></code-line><span class="hljs-symbol">  branch:</span> master
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_26_scrollbar_vertical" class="mCSB_scrollTools mCSB_26_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_26_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_26_scrollbar_horizontal" class="mCSB_scrollTools mCSB_26_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_26_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>例如：</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-01-58.3dtw3iersue.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-01-58.3dtw3iersue.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>在博客根目录下打开git bash</p>
<p>分别执行下面的命令：</p>
<p>yourname是你的名字</p>
<p>youremail是你的邮箱</p>
<code-box id="Yxr5PZ" style="position: relative;display: block;"><button code-id="Yxr5PZ" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=Yxr5PZ]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="Yxr5PZ" class="hljs routeros mCustomScrollbar _mCS_27 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_27" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_27_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-4Gds3P"><code-line class="line-numbers-rows"></code-line>$ git<span class="hljs-built_in"> config </span>--global user.name <span class="hljs-string">"yourname"</span>
<code-line class="line-numbers-rows"></code-line>$ git<span class="hljs-built_in"> config </span>--global user.email <span class="hljs-string">"youremail"</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_27_scrollbar_vertical" class="mCSB_scrollTools mCSB_27_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_27_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_27_scrollbar_horizontal" class="mCSB_scrollTools mCSB_27_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_27_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p>然后安装上传插件</p>
<code-box id="Ehhcch" style="position: relative;display: block;"><button code-id="Ehhcch" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=Ehhcch]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="Ehhcch" class="hljs sql mCustomScrollbar _mCS_28 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_28" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_28_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-BYPimW"><code-line class="line-numbers-rows"></code-line>cnpm <span class="hljs-keyword">install</span> hexo-deployer-git <span class="hljs-comment">--save</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_28_scrollbar_vertical" class="mCSB_scrollTools mCSB_28_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_28_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_28_scrollbar_horizontal" class="mCSB_scrollTools mCSB_28_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_28_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<hr>
<h3 id="上传-1">上传<button class="cnblogs-toc-button" title="显示目录导航" aria-expanded="false"></button></h3>
<blockquote>
<p>以上的配置完成之后，就可以上传了</p>
</blockquote>
<p>在博客根目录下打开git bash，执行下面的命令就可以上传了</p>
<code-box id="kDP65p" style="position: relative;display: block;"><button code-id="kDP65p" type="button" class="clipboard code-copay-btn" data-clipboard-action="copy" data-clipboard-target="pre[code-id=kDP65p]" aria-label="复制代码" style="color: rgb(98, 114, 164);"><i class="iconfont icon-fuzhi1"></i></button><pre highlighted="true" code-id="kDP65p" class="hljs ebnf mCustomScrollbar _mCS_29 mCS-autoHide" style="position: relative; overflow: visible;"><div id="mCSB_29" class="mCustomScrollBox mCS-minimal-dark mCSB_vertical_horizontal mCSB_outside" style="max-height: none;" tabindex="0"><div id="mCSB_29_container" class="mCSB_container mCS_y_hidden mCS_no_scrollbar_y" style="position: relative; top: 0px; left: 0px; width: 982px;" dir="ltr"><code-pre class="code-pre" id="pre-riPd4p"><code-line class="line-numbers-rows"></code-line><span class="hljs-attribute">hexo g -d</span>
<code-line class="line-numbers-rows"></code-line>
</code-pre></div></div><div id="mCSB_29_scrollbar_vertical" class="mCSB_scrollTools mCSB_29_scrollbar mCS-minimal-dark mCSB_scrollTools_vertical" style="display: none;"><div class="mCSB_draggerContainer"><div id="mCSB_29_dragger_vertical" class="mCSB_dragger" style="position: absolute; min-height: 50px; height: 0px; top: 0px;"><div class="mCSB_dragger_bar" style="line-height: 50px; background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div><div id="mCSB_29_scrollbar_horizontal" class="mCSB_scrollTools mCSB_29_scrollbar mCS-minimal-dark mCSB_scrollTools_horizontal" style="display: block;"><div class="mCSB_draggerContainer"><div id="mCSB_29_dragger_horizontal" class="mCSB_dragger" style="position: absolute; min-width: 50px; display: block; width: 384px; max-width: 602px; left: 0px;"><div class="mCSB_dragger_bar" style="background-color: rgb(98, 114, 164);"></div></div><div class="mCSB_draggerRail"></div></div></div></pre></code-box>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-49-05.lkmgvzcdzwh.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_12-49-05.lkmgvzcdzwh.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>然后打开项目，点击Settings</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-07-19.prpi9gjzgvn.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-07-19.prpi9gjzgvn.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>往下滑找到Github pages</p>
<p>点击none 选择master branch</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-11-58.91hsb6n2sg.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-11-58.91hsb6n2sg.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p>之后你会得到一个地址，这个就是你的网站地址了</p>
<p><a data-fancybox="gallery" href="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-06-38.5i4rmc7ha2g.png"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/blogcdn/img/Snipaste_2020-02-29_15-06-38.5i4rmc7ha2g.png" alt="image" loading="lazy" class="medium-zoom-image"></a></p>
<p><strong>教程结束，进阶篇请期待</strong></p>
<p>我的同步更新博客: <a href="https://mrhuanhao.cn/" target="_blank">https://mrhuanhao.cn/</a></p>

<br><p class="essaySuffix-eof">__EOF__</p><div class="essaySuffix-box"><div class="essaySuffix-box-left"><img src="https://cdn.jsdelivr.net/gh/kjhuanhao/cdn/blog/huanhao.jpg" alt=""></div><div class="essaySuffix-box-right"><span class="essaySuffix-right-title">本文作者</span>：<strong><span style="font-size: 12px;"><a href="https://www.cnblogs.com/huanhao/p/hexobase.html" target="_blank">HuanHao</a></span></strong> <br><span style="font-weight: bold; white-space:nowrap;">本文链接</span>：<a href="https://www.cnblogs.com/huanhao/p/hexobase.html" target="_blank">https://www.cnblogs.com/huanhao/p/hexobase.html</a><br><span class="essaySuffix-right-title">关于博主</span>：评论和私信会在第一时间回复。或者<a href="https://msg.cnblogs.com/msg/send/huanhao" target="_blank">直接私信</a>我。<br><span class="essaySuffix-right-title">版权声明</span>：本博客所有文章除特别声明外，均采用 <a href="https://creativecommons.org/licenses/by-nc-nd/4.0/" alt="BY-NC-SA" title="BY-NC-SA" target="_blank">BY-NC-SA</a> 许可协议。转载请注明出处！<br><span class="essaySuffix-right-title">声援博主</span>：如果您觉得文章对您有帮助，可以点击文章右下角<strong><span style="color: #ff0000; font-size: 12pt;">【<a id="post-up" onclick="votePost(hexobase,'Digg')" href="javascript:void(0);">推荐</a>】</span></strong>一下。您的鼓励是博主的最大动力！<br></div><div style="clear: both;"></div></div></div>

