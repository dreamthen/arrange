# arrange
用来整理我的前端所学知识，以及样式和插件的汇总
# HTML与HTML5
##常用标签
~~~html
  <b></b>:加粗标签
  <strong></strong>:加粗标签(表示强调)
  <i></i>:倾斜标签
  <em></em>:倾斜标签(表示特殊语气)
  <u></u>:标签表示加下划线
  <ins></ins>:标签表示着重语气,加下划线
  <del></del>:标签进行删除,从中间加横线
  <s></s>:标签进行删除,从中间加横线
  <span></span>:内联块,标注
  <var></var>:对象的定义标签
  <code></code>:写入代码的标签
  <samp></samp>:标签表示一段用户应该对其没有什么其他解释的文本字符
  <kdb></kdb>:键值对,表示键和值的标签
  <cite></cite>:表示对某个文献的引用
  <dfn></dfn>:表示特殊术语或者短语的定义
  <bdo></bdo>:表示对可调换字符位置的定义标签
  <address></address>:表示对地址的描述
  <mark></mark>:表示对标记定义的标签
  <time></time>:表示对时间戳的定义
  <ruby><ruby>:表示对特殊字符的定义标签
  <rp></rp>:表示特殊字符的父级,比如难写的中文字,要进行标注拼音,这就表示的是中文字部分,在ruby标签中
  <rt></rt>:表示特殊字符的子级,如上,表示的时标注拼音部分,在ruby标签中
  <pre></pre>:表示内容会按照原来有换行和空格形式显示，适合写入程序
  <p></p>:段落标签
  <a></a>:链接标签
  <blockquote></blockquote>:段落模块儿标签
  <sub></sub>:上角标识标签
  <sup></sup>:下角标识标签
  <header></header>:表示网页开头部分标签
  <main></main>:表示网页主要部分标签
  <section></section>:表示网页模块部分标签,没有标题或者进行装容的容器不可使用section
  <aside></aside>:表示网页边栏部分标签
  <article></article>:表示网页内容文章部分标签,此部分非常独立,可做插件容器<embed></embed>
  <nav></nav>:表示导航栏部分标签
  <figure></figure>:表示承载图片部分标签
  <figcaption></figcaption>:表示对图片进行注解部分标签,在figure标签中
  <hgroup></hgroup>:表示承载标题部分标签
  <footer></footer>:表示网页结尾部分标签
  <ul></ul>:表示无序列表标签
  <ol></ol>:表示有序列表标签
  <li></li>:表示有序和无序列表子标签
  <abbr></abbr>:表示对文字缩写与简称的描述
  <audio></audio>:表示装容音频的标签
  <video></video>:表示装容视频的标签
  <source></source>:表示音频视频的资源标签,一般被包容在audio和video标签里面
  <h1></h1>:表示一级标题
  <h2></h2>:表示二级标题
  <h3></h3>:表示三级标题
  <h4></h4>:表示四级标题
  <h5></h5>:表示五级标题
  <h6></h6>:表示六级标题
  <button></button>:表示按钮按键的标签
  <input type="text">:表示文本输入框
  <input type="password">:表示密码输入框
  <input type="number">:表示数字输入框
  <input type="email">:表示邮箱输入框
  <input type="url">:表示地址链接输入框
  <input type="color">:表示颜色输入框
  <input type="file">:表示文件输入框
~~~
##属性
~~~html
  contentEditable:表示标签可编辑
  designModel:表示页面可编辑
  hidden:表示属性隐藏
  spellcheck:表示检查单词是否正确
  datetime:在time标签显示的属性,对现在的时间节点进行定义和解释
  pubdate:发布日期属性,指对article和time标签发布日期的定义和解释
  controls:音频和视频的控制栏,controls值表示显示控制栏
  autoplay:音频和视频是否开始自动播放,autoplay值表示自动播放
~~~
##meta,手机Ipad的适配、兼容的工具和开头网站信息的描述
~~~html
  <meta name="keywords" content="壳艺兼职">:表示关键字，有利于搜索引擎查找
  <meta name="author" content="Gary">:表示作者
  <meta name="description" content="不一样的兼职就在壳艺">:表示对网站的描述
  <meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0,user-scalable=no">:表示对手机和平板的适配，在这里最大的适配宽度是与PC网页端相同，在手机和平板上面适配100%宽度
  <meta http-equiv="x-ua-compatible" content="IE=edge,chrome=1.0">:表示兼容IE最高Edge版本的DOM文档结构和操作，谷歌浏览器chrome也兼容最新版本的DOM文档结构和操作
~~~
# css和css3汇总
##选择器
~~~css
  p,h1,h2{
    /*元素选择器*/
  }
  #id{
    /*id选择器*/
  }
  .class{
    /*类选择器*/
  }
  .p1.p2{
    /*多类选择器*/
  }
  .hbig.hsmall{
    /*多类选择器*/
  }
  p[title="col-lg-p"]{
    /*属性选择器,选择title="col-lg-p"的元素节点*/
  }
  p[title*="col-"]{
    /*属性选择器,选择title内容里面包含"col-"的元素节点,*=是指内容包含"col-"*/
  }
  p > span{
    /*子元素选择器,对p节点的子代样式进行操作*/
  }
  p span{
    /*后代选择器,对p节点的后代,无论是子代还是孙代,样式进行操作*/
  }
  .num-ul > li:first-child+li{
    /*兄弟同胞选择器,+=是指对类名为num-ul的第一个子代li的兄弟同胞节点,样式进行操作*/
  }
~~~
##css兼容老版本浏览器
~~~css
  html,body{
    *color:#FF0000; /*兼容IE6,7,8*/
    _color:#CDCDCD; /*兼容IE6*/
    .color:#C0C0C0; /*兼容IE7*/
  }
~~~
##长宽大小
~~~css
  width:元素块儿的宽度
  min-width:元素块儿最小的宽度
  max-width:元素块儿最大的宽度
  height:元素块儿的高度
  min-height:元素块儿的最小的高度
  max-height:元素块儿的最大的高度
  line-height:设置每行的行高以及行间距的大小
~~~
##分类
~~~css
  cursor:移到元素块儿上面的时候,鼠标显示的形状,常用:pointer,inherit
  display:设置元素块儿的显示表现方式,inerit继承父节点的显示表现方式,inline内联表现方式,inline-block内联块表现方式,block块表现方式,none元素块儿消失,不占用显现时所处位置区域
  position:元素块儿的定位方式,absolute固定布局固定定位方式,relative相对布局相对定位方式,static静态定位,是默认定位方式,fixed绝对固定布局,这种定位方式会使元素块儿定位在窗口的某一块儿区域,不会随着滚动条的滚动而消失,会依然处在窗口的某一块儿区域
  visiblity:设置元素块儿的显示表现方式,占用显现时所处位置区域,hidden元素内容消失,但是还是位置还是占用
~~~
##背景
~~~css
  background-color:背景颜色
  background-image:背景图片
  background-repeat:背景是否重复
  background-position:背景图片的位置
  background-size:背景图片的大小,常用cover,contain(100%)
  background-origin:背景图片的定位位置
  background-clip:背景图片的切片位置
~~~
##文本
~~~css
  color:字体颜色
  text-align:内容位置
  text-indent:指段落空格的长度
  text-decoration:内容标记
  text-transform:内容改写,常用capitalize(单词第一个字母大写),uppercase(所有字母都大写),lowercase(所有字母都小写)
  text-shadow:内容文本阴影
  letter-spacing:内容文字或者字母之间的间距
  word-spacing:单词之间的间距
  white-space:空格或者换行所显示的状态
  word-wrap:单词换行状态，是否让单词字母不分开
  line-height:设置行间距
~~~
##文字
~~~css
  font-size:字体大小
  font-family:文字类型
  font-weight:文字粗细程度
  font-style:文字样式变形程度
  @font-face{
    font-family:
    src:
  }
  自己设置文字的类型,调用外部字体包
~~~
##链接
~~~css
  a:link 链接没点击时候的状态
  a:visited 链接点击后的状态
  a:hover 链接移上去后的状态
  a:active 链接点击后的状态
~~~
##列表
~~~css
  list-style-type:列表标记的类型
  list-style-image:列表标记图片
  list-style-position:列表标记(默认类型或者图片)位置
~~~
##表格
~~~css
  border-collapse:collapse 将表格边框折叠
~~~
##外边框
~~~css
  outline:#CDCDCD double 3px; 外边框的框宽度为2px,框类型为双框,框颜色为#CDCDCD(浅灰色)
~~~
##定位
~~~css
  position:static; 定位的默认值static,静态
  position:absolute; 定位的固定布局absolute,不占用空间,可覆盖,相当于在原来的层面上再添加一层,top和left移动的距离默认相对于body整个页面的左上角部分,但是当父级节点以及父级以上节点含有position:relative相对布局时,会根据最近的上层节点的左上角进行top和left移动距离
  position:relative; 定位的相对布局relative,可相对于本位置进行相对偏移,top和left相对于本位置进行距离顶部和左部的距离设置
  position:fixed; 定位的绝对布局fixed,不占用空间,同position:absolute,但是会固定在窗口的设定的位置,如果页面随着滚动条滚动,也不会消失,是根据页面窗口位置进行设置
~~~
##浮动
~~~css
  float:none; 不进行浮动
  float:left; 向左进行浮动
  float:right; 向右进行浮动
  float:inherit; 继承父节点的浮动设置
  clear:left; 清除向左浮动
  clear:right; 清除向右浮动
  clear:both; 清除向左向右两边浮动
~~~
##清除浮动例子
~~~css
<style>
  .example-float-events:after {
    content:".";
    display:block;
    clear:both;
    visiblity:hidden;
    height:0;
  }
</style>  
~~~
##三列布局,两边浮动,中间自适应(浮动例子)
###第一种方法:圣杯布局
~~~css
<style>
  .example-float-left-events {
    width:200px;
    height:200px;
    float:left;
    background-color:#866ab3;
  }
  .example-float-right-events{
    width:200px;
    height:200px;
    float:right;
    background-color:#8a6d3b;
  }
  .example-float-none-events{
    width:auto;
    height:200px;
    margin:0 210px;
    background-color:brown;
  }
</style>  
~~~
~~~html
<html>
  <body>
    <div class="example-float-left-events"></div>
    <div class="example-float-right-events"></div>
    <div class="example-float-none-events"></div>
  </body>  
</html>  
~~~
###第二种方法:圣杯布局加强版
~~~css
<style>
  html,body{
    padding:0;
    margin:0;
  }
  .header,
  .main,
  .footer{
    width:80%;
    margin:0 auto;
  }
  
  .header,.footer{
    height:90px;
  }
  
  .header{
    background-color:#7a43b6;
  }
  
  .main{
    height:1000px;
    padding:0 150px 0 100px;
    background-color:#0D3349;
  }
  
  .footer{
    background-color:#8a6d3b;
  }
  
  .left,.medium,.right{
    display:block;
  }
  
  .left{
    width:100px;
    float:left;
    margin-left:-100%;
    position:relative;
    right:100px;
    text-align:center;
  }
  
  .medium{
    width:100%;
    float:left;
  }
  
  .right{
    width:150px;
    float:left;
    margin-left:-150px;
    position:relative;
    left:150px;
    text-align:center
  }
</style>  
~~~
~~~html
<html>
  <body>
    <header class="header">
      头部
    </header>
    <main class="main">
      <section class="medium">
          我是中间部分
      </section>
      <section class="left">
          我是左边部分
      </section>
      <section class="right">
          我是右边部分
      </section>
    </main>
    <footer class="footer">
      底部
    </footer>
  </body>
</html>  
~~~
###第三种方法:双飞翼布局
~~~css
<style>
  html,body{
    padding:0;
    margin:0;
  }
  .header,
  .main,
  .footer{
    width:80%;
    margin:0 auto;
  }
  
  .header{
    background-color:#7a43b6;
  }
  
  .footer{
    background-color:#8a6d3b;
  }
  
  .main{
    height:1000px;
    background-color:#0D3349;
    overflow:hidden;
  }
  
  .left,
  .medium,
  .right{
    display:block;
  }
  
  .left{
    width:100px;
    float:left;
    margin-left:-100%;
    padding-bottom:9999px;
    margin-bottom:-9999px;
    text-align:center;
  }
  
  .right{
    width:150px;
    float:left;
    margin-left:-150px;
    padding-bottom:9999px;
    margin-bottom:-9999px;
    text-align:center;
  }
  
  .medium{
    width:100%;
    float:left;
    padding-bottom:9999px;
    margin-bottom:-9999px;
  }
  
  .medium > .inner{
    margin:0 150px 0 100px;
  }
</style>
~~~
~~~html
<html>
  <body>
    <header>
      头部
    </header>
    <main class="main">
      <section class="medium">
        <div class="inner">我是中间</div>
      </section>
      <section class="left">
        我是左边
      </section>
      <section class="right">
        我是右边
      </section>
    </main>
    <footer class="footer">
      底部
    </footer>
  </body>
</html>
~~~
##元素块儿居中
~~~css
  margin:0 auto; 将元素块儿居中,上下为0px,两边为自适应外边距,进行水平居中
~~~
#css盒子模型
##内边距
~~~css
  padding:上 右 下 左; 指对盒子内边距进行批量设置,根据上右下左进行批量设置
  padding:上下 左右; 指对盒子内边距进行批量设置,根据上下 左右进行批量设置
  padding-left:指对盒子内左边距进行设置
  padding-right:指对盒子内右边距进行设置
  padding-top:指对盒子内上边距进行设置
  padding-bottom:指对盒子下边距进行设置
~~~
##边框
~~~css
  border-width:边框的宽度
  border-style:边框的类型,常用的有solid(直线),double(双线),dashed(曲线),dotted(曲线)
  border-color:边框的颜色
  border:3px double #CDCDCD; 指对边框进行批量设置，根据border-width border-style border-color进行批量设置
  border-radius:对盒子标签元素进行圆角处理
  box-shadow:2px 2px 1px 1px #C0C0C0; 对盒子标签元素进行阴影设置，根据水平方向宽度 竖直方向宽度 加粗处理宽度 加粗模糊宽度 颜色设置进行批量设置
  border-image:对盒子标签元素边框进行图片设置
~~~
##外边距
~~~css
  margin:上 右 下 左; 指对盒子外边距进行批量设置，根据上 右 下 左进行批量设置
  margin:上下 左右; 指对盒子外边距进行批量设置，根据上下 左右进行批量设置
  margin-left:指对盒子外左边距进行设置
  margin-right:指对盒子外右边距进行设置
  margin-top:指对盒子外上边距进行设置
  margin-bottom:指对盒子外下边距进行设置
~~~
##外边距合并
~~~css
  如果邻节点都设置了margin,它会根据margin外边距边距大的一方进行外边距处理，而不会进行外边距累加
~~~
#CSS3精致特效
##2D,3D动画
~~~css
  transform:translate(100px,100px); 沿着x轴右移100px,沿着y轴上移100px,translate平移,沿着x轴和y轴方向进行平移,负值沿各自反方向平移
  transform:translateX(100px); 沿着x轴右移100px,translateX沿着x轴方向进行平移,负值沿x轴反方向平移
  transform:translateY(100px); 沿着y轴上移100px,translateY沿着y轴方向进行平移,负值沿y轴反方向平移
  transform:scale(2); 对元素标签模块儿进行放大,在这里,scale宽和高都放大两倍
  transform:scale(2,0.5); 对元素标签模块儿进行放大,在这里,scale宽放大两倍,高缩小1/2
  transform:rotate(45deg); 对元素标签模块儿进行旋转,在这里,rotate沿x轴方向旋转45度角(deg),沿y轴方向旋转45度角(deg)
  transform:rotate(45deg,60deg); 对元素标签模块儿进行旋转,在这里,rotate沿x轴方向旋转45度角(deg),沿y轴方向旋转60度角(deg)
  transform:rotateX(30deg) rotateY(90deg); 对元素标签模块儿进行旋转,在这里,rotateX沿x轴方向旋转30度角(deg),沿y轴方向旋转90度角(deg)
  transform:skew(45deg,30deg); 对元素标签模块儿进行倾斜,在这里,skew沿x轴方向倾斜45度角(deg),沿y轴方向倾斜30度角(deg)
  transform:skewX(60deg) skewY(30deg); 对元素标签模块儿进行倾斜,在这里,skew沿x轴方向倾斜60度角(deg),沿y轴方向倾斜40度角(deg)
  transform-origin:0 0; 将坐标轴的原点进行重新设置,设置为元素标签模块儿的左上角,(0,0)点
  PS:需要加前缀进行兼容
~~~
##过渡
~~~css
  transition-property:要进行过渡动画的样式名称
  transition-duration:过渡动画进行的时间
  transition-timing-function:过渡动画进行的运动曲线
  transition-delay:哪个时刻进行过渡动画，也就是延迟过渡动画执行的时间
  transition:all 1.8s ease-in-out 0s; 指对过渡动画的批量设置，根据transition-property transition-duration transition-timing-function transition-delay进行对过渡动画的批量设置
  PS:需要加前缀进行兼容
~~~
##动画
~~~css
  animation-name:要进行动画播放的名字
  animation-duration:动画播放的时间
  animation-timing-function:动画播放执行的时间曲线
  animation-iteration-count:动画播放次数
  animation-direction:动画播放是否可退回播放
  animation-delay:哪个时刻进行动画播放，也就是延迟动画播放执行的时间
  animation-fill-mode:动画执行前和动画执行之后执行的动画方式
~~~
##多列
~~~css
  column-count:分列的数量，也就是分几列
  column-gap:分列之后，列与列之间的间隔宽度
  column-width:分列的每列宽度
  column-rule:列与列之间边框的宽度、样式类型和颜色，根据边框的宽度、样式类型和颜色进行批量设置
~~~
#响应式布局
##媒介查询
~~~html
  <link rel="stylesheet" type="text/css" href="" media="only screen and (min-width:960px)"> <!--指的是此css外部引导css文件只针对页面宽度为960px及其以上的宽度生效-->
~~~
~~~css
  @media screen and (min-width:640px){
    /*在这儿样式针对页面宽度为640px及其以上的宽度生效*/
  }
  
  @media screen and (min-width:320px) and (max-width:640px){
    /*
      在这样式针对页面宽度最大不超过为640px,最小不低于320px的宽度生效
    */
  }
~~~
#JavaScript
##方法
###Array数组的方法:
~~~Javascript
    var arrayNum = [22,19,2,45,256,89,95,33];
    var arrayString = ["yinwk","zhaoy"];
    console.log(arrayString.join("|"));             //在控制台中显示:"yinwk|zhaoy"
    console.log(arrayString.concat(arrayNum));      //在控制台中显示:["yinwk","zhaoy",22,19,2,45,256,89,95,33]
    console.log(arrayNum.slice(3,5));               //在控制台中显示:[45,256]
    arrayString.splice(1,0,"love");    
    console.log(arrayString);                       //在控制台中显示:["yinwk","love","zhaoy"]
    console.log(arrayString.splice(0,1));           
    console.log(arrayString);                       //在控制台中显示:["zhaoyue"]
    arrayString.splce(0,1,"尹文楷");
    console.log(arrayString);                       //在控制台中显示:["尹文楷","zhaoy"]
    console.log(arrayString.reverse());             //在控制台中显示:["zhaoy","yinwk"]
    console.log(arrayNum.sort());                   //在控制台中显示:[19,2,22,256,33,45,89,95]
    console.log(arrayNum.sort(function(a,b){
          return a - b;
    }));                                            //在控制台中显示:[2,19,22,33,45,89,95,256]
    console.log(arrayNum.push("笨笨熊"));           //在控制台中显示:[22,19,2,45,256,89,95,33,"笨笨熊"]
    console.log(arrayNum.pop());                    //在控制台中显示:[22,19,2,45,256,89,95]
    console.log(arrayNum.shift());                  //在控制台中显示:[19,2,45,256,89,95,33]
    console.log(arrayNum.unshift("熊笨笨"));        //在控制台中显示:["熊笨笨",22,19,2,45,256,89,95,33]
~~~
###Number类型Math各种数学函数的方法
~~~javascript
   var num = 1314.356;
   var absTest = -100.256;
   console.log(Math.abs(absTest));                  //在控制台中显示:100.256
   console.log(Math.PI);                            //在控制台中显示:3.1415926...
   console.log(Math.round(num));                    //在控制台中显示:1314
   console.log(Math.min(25,67,3,100,256,34,0,-45)); //在控制台中显示:-45
   console.log(Math.max(25,67,3,100,256,34,0,-45)); //在控制台中显示:256
   console.log(Math.ceil(8.1));                     //在控制台中显示:9
   console.log(Math.floor(10.9));                   //在控制台中显示:10
   console.log(Math.pow(2,4));                      //在控制台中显示:16
   console.log(Math.sqrt(144));                     //在控制台中显示:12
   console.log(num.toFixed(2));                     //在控制台中显示:1314.36
   console.log(num.toExponential());                //在控制台中显示:1.314356*10^4
   console.log(num.toPrecision(5));                 //在控制台中显示:1314.4
~~~
###Date类型方法
~~~javascript
  var date = new Date();
  console.log(date.getFullYear());                  //在控制台中显示:2016
  console.log(date.getDate());                      //在控制台中显示:4
  console.log((date.getMonth()+1));                 //在控制台中显示:9
  console.log(date.getHours());                     //在控制台中显示:20
  console.log(date.getMinutes());                   //在控制台中显示:23
  console.log(date.getSeconds());                   //在控制台中显示:24
~~~
###Date计时器
~~~javascript
  time();
  var time = function(){
      var date = new Date();
      var div = document.getElementsByTagName("div")[0];
      var y = date.getFullYear();
      var month = checkDate(date.getMonth()+1);
      var d = checkDate(date.getDate());
      var h = checkDate(date.getHours());
      var m = checkDate(date.getMinutes());
      var s = checkDate(date.getSeconds());
      var dateMine = y + "年" + month + "月" + d + "日 " + h + "时" + m + "分" + s +"秒";
      div.innerHTML = dateMine;
      setTimeOut(function(){
        time();
      },1000);
  }
  
  function checkDate(timecheck){
      if(timecheck<10){
        timeCheck = "0" + timeCheck;
      }
      return timeCheck;
  }
~~~
~~~html
  <html>
    <body>
      <div class="div">
      </div>
    </body>
  </html>
~~~
###String字符串的方法
~~~javascript
  var string = "Hello World";
  console.log(string.charAt(4));                    //在控制台中显示:"o"
  console.log(string.charCodeAt(4));                //在控制台中显示:111
  console.log(string.concat(" yinwk"));             //在控制台中显示:"Hello World yinwk"
  console.log(string.slice(3,5));                   //在控制台中显示:"lo"
  console.log(string.substring(3,5));               //在控制台中显示:"lo"
  console.log(string.substr(3,2));                  //在控制台中显示:"lo"
  console.log(string.slice(3,-2));                  //在控制台中显示:"lo Wor"
  console.log(string.substring(3,-2));              //在控制台中显示:"Hel"
  console.log(string.substr(3,-2));                 //在控制台中显示:""
  console.log(string.search(/[l]/g));               //在控制台中显示:2
  console.log(string.match(/[l]/g));                //在控制台中显示:["l","l","l"]
  console.log(string.split(" "));                   //在控制台中显示:["Hello","World"]
  console.log(string.replace(/[l]/g,"m"));          //在控制台中显示:Hemmo Wormd
  console.log(string.indexOf("o"));                 //在控制台中显示:4
  console.log(string.indexOf("o",5));               //在控制台中显示:7
  console.log(string.lastIndexOf("o"));             //在控制台中显示:7
  console.log(string.lastIndexOf("o",5));           //在控制台中显示:4
  console.log(string.toUpperCase());                //在控制台中显示:"HELLO WORLD"
  console.log(string.toLowerCase());                //在控制台中显示:"hello world"
  console.log(string.toLocaleUpperCase());          //在控制台中显示:"HELLO WORLD"
  console.log(string.toLocaleLowerCase());          //在控制台中显示:"hello world"
~~~
##面向对象封装
~~~javascript
window.onload = function(){
  var app = {};
  (function(obj){
      function Person(name,age){
          this.name = name;
          this.age = age;
      }
      Person.prototype.description = function(){
          return "姓名:" + this.name + ",年龄:" + this.age;
      };
      Object.defineProperties(obj,{
          Person:{
            value:Person,
            writable:true,
            configurable:true,
            enumable:true
          }
      });
  })(app);
  var person = new app.Person("尹文楷",23);
  console.log(person.description());                //在控制台中显示:"姓名:尹文楷,年龄:23"
}  
~~~
##面向对象继承
~~~javascript
window.onload = function(){
  var app = {};
  (function(obj){
      function Person(name){
        this.name = name;
      }
      Person.prototype.getName = function(){
        return "姓名:" + this.name;
      };
      function extend(subClass,superClass){
        var F = function(){};
        F.prototype = superClass.prototype;
        subClass.prototype = new F();
        subClass.prototype.constructor = subClass;
        subClass.superClasses = superClass.prototype;
        if(superClass.prototype.constructor == Object.prototype.constructor){
            superClass.prototype.constructor = superClass;
        }
      }
      extend(Store,Person);
      function Store(name,books){
        this.book = books;
        Store.superClasses.constructor.call(this,name);
      }
      Store.prototype.getName = function(){
        return "书名:" + this.book + ",借书者:" + this.name;
      }
      Object.defineProperties(obj,{
          Store:{
            value:Store,
            writable:true,
            configurable:true,
            enumable:true
          }
      });
  })(app);
  var book = new app.Store("赵悦","鲁滨逊漂流记");
  console.log(book.getName());                      //在控制台中显示:"书名:鲁滨逊漂流记,借书者:赵悦"
}  
~~~
##DOM
~~~javascript
  var findById = document.getElementById("div");                    //在全局节点中寻找id值为div的节点
  var findByClass = document.getElementsByClassName("classFirst");  //在全局节点中寻找class值为classFirst的节点数组
  var findByName = document.getElementsByName("userName");          //在全局节点中寻找name值为userName的节点数组
  var findByTag = document.getElementsByTagName("p");               //在全局节点中寻找全部的p节点数组
  var p = document.createElement("p");                              //创建一个p标签DOM节点
  var text = document.createTextNode("yinwk love zhaoy");           //创建一个文本节点,内容为"yinwk love zhaoy"
  p.appendChild(text);                                              //将文本节点"yinwk love zhao"加入到p标签DOM节点里面
  findById.appendChild(p);                                          //将id值为div的节点里面加入子节点p标签DOM节点
~~~
###DOM获取子节点、类型以及值
~~~javascript
  var ul = document.getElementsByTagName("ul")[0];
  console.log(ul.childNodes.length);                                //在控制台中显示:7
  for(var i = 0; i < ul.childNodes.length; i++){
      if(ul.childNodes[i].nodeType !== 3){
          console.log(ul.childNodes[i].nodeName);                   //在控制台中显示:LI
                                                                    //              LI
                                                                    //              LI
      }
      console.log(ul.childNodes[i].nodeName);                       //在控制台中显示:#text
                                                                    //              LI
                                                                    //              #text
                                                                    //              LI
                                                                    //              #text
                                                                    //              LI
                                                                    //              #text
  }
~~~
~~~html
  <html>
    <body>
      <ul>
        <li>yinwk</li>
        <li>zhaoy</li>
        <li>liuzj</li>
      </ul>
    </body>
  </html>
~~~
##老版本浏览器兼容html5标签方法
~~~Javascript
  (function(global){
      if(!0){
        return;
      }
      var e = "header,footer,section,article,aside,figure,figcaption".split(","),i=e.length;
      while(i--){
        document.createElement(e[i]);
      }
  })(window);
~~~
##函数
~~~Javascript
  function func(){
    /*定义函数的一种方式*/
  }
  var func = function(){
    /*定义函数的另一种方式*/
  }
  
  var n = 10;
  function func(name,age){
    var result = "姓名:"+name+",年龄:"+age;
    console.log("姓名:"+name+",年龄:"+age);
    return result;
  }
  var myResult = func("Gary",23); //传递参数name("Gary")和age(23)进到函数里面,返回"姓名:Gary,年龄:23",而且还会在控制台显示"姓名:Gary,年龄:23"
  console.log(result); //会报错,因为result是局部变量
  console.log(n); //n是全局变量,在控制台显示10
  console.log(name+","+age); //name,age是全局变量,作为参数的全局变量,在控制台中显示"Gary,23"
~~~
#jQuery
