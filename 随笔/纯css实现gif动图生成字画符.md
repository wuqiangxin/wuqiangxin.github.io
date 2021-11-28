<div class="article-detail">
                    <h2 class="header">
                        纯css实现gif动图生成字画符
                                                                    </h2>
<p>转载于  https://my.oschina.net/codingDog</p>
                                                                        <div class="tags">
                                <a class="ui horizontal label" href="https://my.oschina.net/codingDog?q=javascript">javascript</a><a class="ui horizontal label" href="https://my.oschina.net/codingDog?q=webkit">webkit</a>                            </div>
                                            
                    <div class="content" id="articleContent">
                                                                           
                                    
                        <p style="color:#1a1a1a; text-align:start">之前有一篇博客试过使用 <a href="https://my.oschina.net/codingDog/blog/1845658" target="_blank">JavaScript生成字符画</a>，但是最终没有实现gif转字画符，事实上用当时说的方法：把gif每帧抽取出来，然后绘制到canvas上即可。</p> 
<p style="color:#1a1a1a; text-align:start">不过这次要说的实现方式并非js，而是纯css实现，核心的属性是<span style="color:#ffffff"><span style="background-color:#999999">&nbsp;background-clip </span></span>和<span style="color:#ffffff"><span style="background-color:#999999">&nbsp;text-fill-color </span></span>，由于这俩属性目前并没有被纳入标准，所以需要加上 -webkit-前缀。当初发现这个属性是真的像发现了个宝藏，通过它们的组合可以实现非常多有意思的效果。前者用于对背景裁剪，后者用于和背景颜色叠加。</p> 
<p style="color:#1a1a1a; text-align:start">于是就有了下图的效果（背景是一张动图，然后使用文字对背景进行裁剪。字体透明填充，与背景叠加）</p> 
<p style="color:#1a1a1a; text-align:start"><img alt="" height="347" src="https://oscimg.oschina.net/oscnet/up-0b0adace9f28fbb5d8432c707401bda8356.gif" width="248" class="zoom-in-cursor"></p> 
<p style="color:#1a1a1a; text-align:start">&nbsp;</p> 
<p style="color:#1a1a1a; text-align:start">html结构：</p> 
<pre><code class="hljs html xml"><span class="hljs-meta">&lt;!doctype html&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">html</span> <span class="hljs-attr">lang</span>=<span class="hljs-string">"zh-cn"</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">head</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">charset</span>=<span class="hljs-string">"UTF-8"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"viewport"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">http-equiv</span>=<span class="hljs-string">"X-UA-Compatible"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"ie=edge"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">title</span>&gt;</span>css ascii srt<span class="hljs-tag">&lt;/<span class="hljs-name">title</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">style</span>&gt;</span><span class="css">
    <span class="hljs-comment">/* 样式 */</span>
  </span><span class="hljs-tag">&lt;/<span class="hljs-name">style</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">head</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">body</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">p</span>&gt;</span>
  色欲一事，乃舉世人之通病不特中下之人，被色所迷。即上根之人，若不戰兢自持，乾惕在念，則亦難免不被所迷。試觀古今來多少出格豪傑，固足為聖為賢。
  祗由打不破此關，反為下愚不肖。兼復永墮惡道者，蓋難勝數。楞嚴經云，若諸世界六道眾生，其心不淫，則不隨其生死相續。汝修三昧，本出塵勞。淫心不除，塵不可出。
  學道之人，本為出離生死。苟不痛除此病，則生死斷難出離，即念佛門，雖則帶業往生。然若淫習固結，則便與佛隔，難於感應道交矣。欲絕此禍，莫如見一切女人，皆作親想，怨想，不淨想。親想者。
  見老者作母想淘宝特卖眼线润肤乳排行榜好左旋肉碱哪个牌子好去黑头化妆水哪个牌子好有效的哪个保健补品好，長者作姊想，少者作妹想，幼者作女想，欲心縱盛，斷不敢於母姊妹女邊起不正念。
  視一切女人，總是吾之毋姊妹女。則理制於欲，欲無由發矣。怨想者，凡見美女，便起愛心。由此愛心，便墮惡道。長劫受苦，不能出離。如是則所謂美麗嬌媚者，比劫賊虎狼、毒蛇惡蠍，砒霜鴆毒，烈百千倍。
  於此極大怨家，尚猶戀戀著念，豈非迷中倍人。不淨者，美貌動人，只外面一層薄皮耳。若揭去此皮，則不忍見矣。骨肉膿血，屎尿毛髮，淋漓狼藉，了無一物可令人愛。但以薄皮所蒙。則妄生愛戀。
  華瓶盛糞，人不把玩。今此美人之薄皮，不異華瓶。皮內所容，比糞更穢。何得愛其外皮，而忘其裏之種種穢物，漫起妄想乎哉。苟不戰兢乾惕，痛除此習。則唯見其姿質美麗，致愛箭入骨，不能自拔。
  平素如此，致其沒後不入女腹，不可得也。入人女腹猶可。入畜女腹，則將奈何。試一思及，心神驚怖。
  然欲于見境不染心，須于未見境時，常作上三種想，則見境自可不隨境轉。否則縱不見境，意地仍復纏綿，終被淫欲習氣所縛。固宜認真滌除惡業習氣，方可有自由分。
<span class="hljs-tag">&lt;/<span class="hljs-name">p</span>&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">script</span>&gt;</span><span class="javascript">
  <span class="hljs-comment">// 脚本</span>
</span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">body</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">html</span>&gt;</span></code></pre> 
<p style="color:#1a1a1a; text-align:start">样式：</p> 
<pre><code class="hljs css">* {
  <span class="hljs-attribute">margin</span>: <span class="hljs-number">0</span>;
  <span class="hljs-attribute">padding</span>: <span class="hljs-number">0</span>;
}
<span class="hljs-selector-tag">html</span>,
<span class="hljs-selector-tag">body</span> {
  <span class="hljs-attribute">width</span>: <span class="hljs-number">100%</span>;
  <span class="hljs-attribute">height</span>: <span class="hljs-number">100%</span>;
}
<span class="hljs-selector-tag">body</span> {
  <span class="hljs-attribute">position</span>: relative;
  <span class="hljs-attribute">overflow</span>: hidden;
}
<span class="hljs-selector-tag">p</span> {
  <span class="hljs-attribute">font-weight</span>: <span class="hljs-number">600</span>;
  <span class="hljs-attribute">position</span>: absolute;
  <span class="hljs-attribute">width</span>: <span class="hljs-number">100%</span>;
  <span class="hljs-attribute">overflow</span>: hidden;
  <span class="hljs-attribute">left</span>: <span class="hljs-number">50%</span>;
  <span class="hljs-attribute">top</span>: <span class="hljs-number">50%</span>;
  <span class="hljs-attribute">transform</span>: <span class="hljs-built_in">scale</span>(0.9);
  <span class="hljs-attribute">background-repeat</span>: no-repeat;
  <span class="hljs-attribute">background-position</span>: center;
  <span class="hljs-attribute">background-size</span>: contain;
  <span class="hljs-attribute">-webkit-background-clip</span>: text;
  <span class="hljs-attribute">-webkit-text-fill-color</span>: transparent;
  <span class="hljs-attribute">transform-origin</span>: <span class="hljs-number">50%</span> <span class="hljs-number">50%</span>;
  <span class="hljs-comment">/*js生成*/</span>
  <span class="hljs-comment">/*font-size: 12px;*/</span>
  <span class="hljs-comment">/*line-height: 12px;*/</span>
  <span class="hljs-comment">/*width: 400px;*/</span>
  <span class="hljs-comment">/*height: 400px;*/</span>
  <span class="hljs-comment">/*margin-left:-200px;*/</span>
  <span class="hljs-comment">/*margin-top:-200px;*/</span>
  <span class="hljs-comment">/*background-image: url(./img/test.jpg);*/</span>
}</code></pre> 
<p>脚本：</p> 
<pre><code class="hljs javascript"><span class="hljs-keyword">const</span> $p = <span class="hljs-built_in">document</span>.getElementsByTagName(<span class="hljs-string">'p'</span>)[<span class="hljs-number">0</span>]
<span class="hljs-comment">// 字体大小</span>
<span class="hljs-keyword">const</span> fontSize = <span class="hljs-number">12</span>
<span class="hljs-comment">// 背景图片</span>
<span class="hljs-keyword">const</span> imgUrl = <span class="hljs-string">'./mememe.gif'</span>
$p.style.cssText = <span class="hljs-string">`font-size:<span class="hljs-subst">${fontSize}</span>px;line-height:<span class="hljs-subst">${fontSize}</span>px;`</span>
<span class="hljs-keyword">const</span> text = $p.innerHTML.replace(<span class="hljs-regexp">/(\s+)/g</span>, <span class="hljs-string">''</span>)
<span class="hljs-keyword">const</span> textLength = text.length

<span class="hljs-keyword">const</span> img = <span class="hljs-keyword">new</span> Image()
img.src = imgUrl
img.complete ? onImgLoaded() : (img.onload = onImgLoaded)

<span class="hljs-function"><span class="hljs-keyword">function</span> <span class="hljs-title">onImgLoaded</span> (<span class="hljs-params"></span>) </span>{
  <span class="hljs-keyword">const</span> imgRatio = img.width / img.height
  <span class="hljs-keyword">let</span> imgWidth = <span class="hljs-built_in">window</span>.innerWidth
  <span class="hljs-keyword">let</span> imgHeight = imgWidth / imgRatio
  <span class="hljs-keyword">if</span> (imgHeight &gt; <span class="hljs-built_in">window</span>.innerHeight) {
    imgHeight = <span class="hljs-built_in">window</span>.innerHeight
    imgWidth = imgHeight * imgRatio
  }
  <span class="hljs-keyword">const</span> needTextLength = (imgWidth / fontSize) * (imgHeight / fontSize)
  <span class="hljs-keyword">if</span> (needTextLength &gt; textLength) {
    $p.innerHTML = <span class="hljs-keyword">new</span> <span class="hljs-built_in">Array</span>(<span class="hljs-built_in">Math</span>.floor(needTextLength / textLength) + <span class="hljs-number">1</span>).fill(text).join(<span class="hljs-string">''</span>)
  }
   $p.style.cssText += <span class="hljs-string">`margin-left:<span class="hljs-subst">${-imgWidth<span class="hljs-regexp">/2}px;margin-top:${-imgHeight/</span><span class="hljs-number">2</span>}</span>px;width:<span class="hljs-subst">${imgWidth}</span>px;height:<span class="hljs-subst">${imgHeight}</span>px;background-image:url(<span class="hljs-subst">${imgUrl}</span>);`</span>
}</code></pre> 
<p style="color:#333333; text-align:left"><img height="23" src="https://static.oschina.net/uploads/space/2017/0630/180033_T7KY_1389094.png" width="50"><span>&nbsp;</span><a href="https://gitee.com/kaysama/blog-source-host/blob/master/%E5%AD%97%E7%AC%A6%E7%94%BB/ascii_art_css.html" target="_blank">完整代码戳这里</a></p> 
<p style="color:#333333; text-align:left"><img height="23" src="https://static.oschina.net/uploads/space/2017/0630/180033_T7KY_1389094.png" width="50"><a href="https://kaysama.gitee.io/blog-source-host/%E5%AD%97%E7%AC%A6%E7%94%BB/ascii_art_css.html" target="_blank">在线演示1</a>、<a href="https://codepen.io/oj8kay/pen/NWxEzgx" target="_blank">在线演示2</a></p>
                    </div>

                                               