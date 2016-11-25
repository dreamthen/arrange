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
  <caption></caption>:表示表格的标题
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
  summary:表示对表格的摘要
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
  如果上下邻节点都设置了margin，它会根据margin外边距边距大的一方进行外边距处理，而不会进行外边距累加
  而左右水平平铺的邻节点，不会进行的外边距合并，会进行外边距累加
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
    var arrayStringOne = ["yinwk","zhaoy","yinwk"];
    console.log(arrayString.join("|"));               //在控制台中显示:"yinwk|zhaoy"
    console.log(arrayString.concat(arrayNum));        //在控制台中显示:["yinwk","zhaoy",22,19,2,45,256,89,95,33]
    console.log(arrayNum.slice(3,5));                 //在控制台中显示:[45,256]
    arrayString.splice(1,0,"love");    
    console.log(arrayString);                         //在控制台中显示:["yinwk","love","zhaoy"]
    console.log(arrayString.splice(0,1));           
    console.log(arrayString);                         //在控制台中显示:["zhaoyue"]
    arrayString.splce(0,1,"尹文楷");
    console.log(arrayString);                         //在控制台中显示:["尹文楷","zhaoy"]
    console.log(arrayString.reverse());               //在控制台中显示:["zhaoy","yinwk"]
    console.log(arrayString.indexOf("zhaoy"));        //在控制台中显示:1
    console.log(arrayStringOne.lastIndexOf("yinwk")); //在控制台中显示:2
    console.log(arrayNum.sort());                     //在控制台中显示:[19,2,22,256,33,45,89,95]
    console.log(arrayNum.sort(function(a,b){
          return a - b;
    }));                                                //在控制台中显示:[2,19,22,33,45,89,95,256]
    console.log(arrayNum.push("笨笨熊"));               //在控制台中显示:[22,19,2,45,256,89,95,33,"笨笨熊"]
    console.log(arrayNum.pop());                       //在控制台中显示:[22,19,2,45,256,89,95]
    console.log(arrayNum.shift());                     //在控制台中显示:[19,2,45,256,89,95,33]
    console.log(arrayNum.unshift("熊笨笨"));            //在控制台中显示:["熊笨笨",22,19,2,45,256,89,95,33]
    arrayNum.forEach(function(item,index,array){
        console.log(item);                             //在控制台中显示:[22,19,2,45,256,89,95,33]
    });
    var arrAno = arrayNum.filter(function(item,index,array){
        return item < 80;                           
    });
    console.log(arrAno);                               //在控制台中显示:[22,19,2,45,33]
    var arrThird = arrayNum.map(function(item,index,array){
        return item + 10;
    });
    console.log(arrThird);                             //在控制台中显示:[32,29,12,55,266,99,105,43]
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
  console.log(date.getLocaleString());              //在控制台中显示:2016-9-25 上午12:52:11
  console.log(date.getLocaleTimeString());          //在控制台中显示:上午12:52:11
  console.log(date.getLocaleDateString());          //在控制台中显示:2016-9-25
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
  var stringTrim = " Hello,World~ ":
  trim = stringTrim.trim();
  console.log(trim.length);                         //在控制台中显示:"12"
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
###空函数对象继承
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
###多函数继承
~~~javascript
window.onload = function(){
  (function(global){
      function Person(name){
         this.name = name;
      }

      Person.prototype.getName = function(){
         return name;
      };

      function extend(subClass,superClass){
         function F(){}
         for(propTypes in superClass[prototype]){
            F[prototype][propTypes] = superClass[prototype][propTypes];
         }
         for(propF in F[prototype){
            subClass[prototype][propF] = F[prototype][propF];
         }
         subClass.prototype.constructor = subClass;
         subClass.superClasses = superClass;
         if(superClass.prototype.constructor === Object.prototype.constructor){
            superClass.prototype.constructor = superClass;
         }
      }

      function Transformer(){
          this.action = "";
      }

      Transformer.prototype.getAction = function(action){
          this.action = action;
          return this.action;
      }

      extend(Book,Person);
      extend(Book,Transformer);
      function Book(name,book){
          Book.superClasses.prototype.call(this,name);
          this.book = book;
      }
      Book.prototype.description = function(){
          return "借书名:"+this.book+",借书人:"+this.name;
      }

      var book = new Book("yinwk","鲁滨逊漂流记");
      Object.defineProperties(global,{
          book:{
            value:book,
            enumable:true,
            writable:true,
            configurable:true
          }
      });
  })(window);
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
  console.log(findByTag[0].parentNode.nodeName);                    //将全部节点中第一个p节点的父节点在控制台中显示出来
  var li = document.getElementsByTagName("li")[0];
  var ul = document.getElemetnsByTagName("ul")[0];
  ul.removeChild(li);                                               //将全部节点中的第一个li节点从全部节点中的第一个uli节点中删除
  var width = document.body.offsetWidth || document.documentElement.offsetWidth;                            
  //获取到当前页面当前的宽度,并兼容IE
  var height = document.body.offsetHeight || document.documentElement.offsetHeight;                          //获取到当前页面当前的高度,并兼容IE
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
###DOM在原有p节点的上方添加p节点
~~~javascript
  var p = document.getElementsByTagName("p")[0];
  var div = document.getElementById("div");
  var word = document.createElement("p");
  var text = document.createTextNode("笨熊熊爱小悦");
  word.appendChild(text);
  div.insertBefore(word,p);                                         //在p标签的上面添加了一行p,内容显示"笨笨熊爱小悦"
~~~
~~~html
  <html>
    <body>
      <div id="div">
          <p>在这一行上面添加一行p</p>
      </div>
    </body>
  </html>
~~~
##读取和获取节点属性
~~~javascript
  var attr = document.getElementById("attr");
  console.log(attr.style.color);                                     //在控制台中显示:#2dc3e8的rgb的形式
  console.log(attr.attributes.title);                                //在控制台中显示:title="attrMost"
  console.log(attr.getAttribute("title"));                           //在控制台中显示:attrMost
  attr.style.color = "#000";                                         //将节点style样式中的color样式,由"#2dc3e8"变为"#000"
  attr.setAttribute("style","color:#000");                           //将节点style样式中的color样式,由"#2dc3e8"变为"#000"
  attr.removeAttribute("title");                                     //将节点title属性删除
  console.log(attr.getAttribute("title"));                           //由于title属性已被删除,所以在控制台中显示:undefined
~~~
~~~html
  <head>
  </head>
  <body>
    <div id="attr" class="attr-get" title="attrMost" style="color:#2dc3e8">
        attributes
    </div>
  </body>
~~~
##浏览器对象
###window
~~~javascript
  var width = window.innerWidth;                                    //获取到屏幕内层的宽度
  var height = window.innerHeight;                                  //获取到屏幕内层的高度
  var outerWidth = window.outerWidth;                               //获取到屏幕外层的宽度
  var outerHeight = window.outerHeight;                             //获取到屏幕外层的高度
  window.open("http://www.baidu.com","_blank","width=300,height=300,top=100,left=100,toolbar=yes,menubar=yes,scrollbars=yes");
  //在一个新页面上打开百度的URL,这个新页面宽度为300px,高度为300px,距离顶部100px,距离左部100px,设置导航栏,设置菜单栏,必须有滚动条
  window.close();
  //关闭页面
  window.print();
  //打印页面
~~~
###location对象
~~~javascript
  var url = window.location.href;                                   //获取到整个URL
  var host = window.location.host;                                  //获取到ip地址+端口号
  var hostName = window.location.hostname;                          //获取到URL的ip地址
  var port = window.location.port;                                  //获取到URL的端口
  var pathName = window.location.pathname;                          //获取到URL的路径
  var search = window.location.search;                              //获取到URL的参数
  var hash = window.location.hash;                                  //获取到URL的hash指针
  var protocol = window.location.protocol;                          //获取到URL的协议
  window.location.assign("http://www.baidu.com");                  //页面执行载入,加载出百度首页
  window.location.reload();                                         //本页面重新加载
~~~
###history对象
~~~javascript
  window.history.go(0);                                             //本页面重新加载
  window.history.go(1);                                             //页面跳到历史记录下一个浏览的页面
  window.history.go(-1);                                            //页面跳到历史记录上一个浏览的页面
  window.history.back();                                            //页面跳到历史记录上一个浏览的页面
  window.history.forward();                                         //页面跳到历史记录写一个浏览的页面
~~~
###screen对象
~~~javascript
  var screenWidth = window.screen.Width;                            //获取到屏幕的宽度
  var screenHeight = window.screen.Height;                          //获取到屏幕的高度
  var avaWidth = window.screen.availWidth;                          //获取到屏幕的最大宽度
  var avaHeight = window.screen.availHeight;                        //获取到屏幕的最大高度
~~~
###计时器
~~~javascript
  function getTime(){
    var date = new Date();
    var y = changeStatus(date.getFullYear());
    var month = changeStatus(date.getMonth()+1);
    var d = changeStatus(date.getDate());
    var h = changeStatus(date.getHours());
    var m = changeStatus(date.getMinutes());
    var s = changeStatus(date.getSeconds());
    var time = y + "年" + month + "月" + d + "日 " + h + "时" + m + "分" + s + "秒";
    console.log(time);
  }
  setTimeInterval(getTime,1000);                                     //不断执行的时间,在页面上显示:2016年09月09日 21时39分59秒,并不断执行刷新
  setTimeOut(getTime,1000);                                          //只执行一次,执行时间
  function changeStatus(time){
    if(time<10){
      time = "0" + time;
    }
    return time;
  }
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
###jQuery获取节点
~~~javascript
  $(document).ready(function(){
      var id =  $("#div");                                           //Jquery获取到id为div的节点
      var class = $(".className");                                   //Jquery获取到class为className的节点数组
      var p = $("p");                                                //Jquery获取到所有的p节点数组
      var title = $("input[title*='only']");                           //Jquery获取到所有的input中的title属性包含"only"字符串的节点数组
      var name = $("input[name='userName']");                        //Jquery获取到所有的input节点中的name属性等于"userName"字符串的节点数组
      var alt = $("img[alt~='panda']");                             //Jquery获取到所有的img节点中的alt属性特定等于"panda"字符串的节点数组
  });
~~~
###jQuery自定义事件
~~~javascript
  $(document).ready(function(){
      var button = $("#button");
      button.click(function(){
        var e = jQery.Event("myEvent");
        button.trigger(e);
      });
      
      button.bind("myEvent",function(event){
        console.log(event);                                           //jQuery.Event进行自定义事件,这个内置对象是指myEvent
      });
  });
~~~
###jQuery内置对象
~~~javascript
  $(document).ready(function(){
      var div = $("#div");
      var button = $("#button");
      div.on("click",function(e){
          console.log("div");
          e.stopPropagation();                                        //取消父级冒泡事件
          e.stopImmediatePropagation();                               //取消所有节点的冒泡事件
      });
      
      button.on("click",function(e){
          console.log("button");
      });
  });
~~~
~~~html
<html>
  <head>
    <style>
      html,body{
        margin:0;
        padding:0;
      }
      #div{
        width:400px;
        height:400px;
        background-color:brown;
      }
    </style>
  </head>
  <body>
      <div id="div">
          <button id="button">点击</button>
      </div>
  </body>
</html>
~~~
###jQuery绑定事件
~~~javascript
//由于jQery的事件click,dblclick....事件太占用电脑和浏览器内存,所以使用绑定事件
$(document).ready(function(){
    var div = $("#div");
    div.bind("click",clickOne);                                         //bind进行事件绑定点击事件,在控制台中显示"divOne"
    
    function clickOne(e){
        console.log("divOne");
    }
    
    div.unbind("click",clickOne);                                       //unbind进行事件解绑点击事件,在控制台中没有显示
    div.on("click",clickOne);                                           //on进行事件绑定点击事件,在控制台中显示"divOne"
    div.off("click",clickOne);                                          //off进行事件解绑点击事件,在控制台中没有显示
});
~~~
###jQuery判断滚动条是否到底
~~~javascript
$(function(){
  $(window).scroll(function(){
      var scrollTop = $(document).scrollTop();                           //获取到滚动条距离document顶端的距离
      var windowHeight = $(window).height();                             //获取到窗口的高度
      var documentHeight = $(document).height();                         //获取到整个页面document的高度
      if(scrollTop >= (documentHeight - windowHeight)){                  //判断是否到达页面的底端
          console.log("到达底端~");                                       //将页面滚动条滑到底端,在控制台中显示"到达底端~"
      }
  });
});
~~~
###jQuery获取DOM对象
~~~javascript
$(function(){
  var objQuery = $("#objQuery");
  console.log(objQuery.get(0));                                           //获取到jQuery对象的DOM对象,在控制台显示:"DivElement"
});
~~~
~~~html
<head>
  <style>
  </style>
</head>
<body>
  <div id="objQuery"></div>
</body>
~~~
#Git版本管理工具
##设置ssh keygen命令
~~~javascript
ssh-keygen -t rsa -b 4096 -c "dreamthen.00@gmail.com"                     //对自己的邮箱进行ssh加密,保存在自己的C盘的用户文件夹的yinwk文件夹的.ssh文件夹的底下
~~~
##Git命令
~~~javascript
git clone git@github.com:dreamthen/Altitude.git                           //对项目克隆并复制到本地
git status                                                                //显示出此git项目其中改动文件的状态
git status -s                                                             //显示出此git项目改动文件的状态,git add之前如果修改了文件,会在这个文件前面两位的第二位显示一个红色的M,而新添加的文件会在前面两位的第一位显示一个红色的A;git add之后,git commit之前如果修改了文件,会在这个文件前面两位的第二位显示一个绿色的M,而新添加的文件会在前面两位的第一位显示一个绿色的A
git diff                                                                  //git add之前,对此git项目中的文件修改区别进行显示,添加了什么会用+号显示,删除了什么会用-号显示
git diff --staged                                                         //git add之后,git commit之前,对此git项目中的文件修改区别进行显示,添加了什么会用+号显示,删除了什么会用-号显示
git reset 文件名                                                          //git add之后,git commit之前,如果想恢复到没有add之前加入到working directory中的状态,进行git reset 文件名
git checkout 文件名                                                        //git commit之后,如果想恢复到git add之后,git commit之前加入到staged area的状态,进行git checkout 文件名
git checkout HEAD 文件名                                                   //git commit之后,如果想恢复到git add之前加入到working directory的状态,进行git checkout HEAD 文件名
git add stylesheets                                                       //添加stylesheets这个文件夹到github库
git commit -m "altitude"                                                  //你进行此次添加操作的注解或者说是说明
git commit -am 文件名 "altitude"                                          //进行提交版本操作,一步到位,相当于git add和git commit两步操作,将修改或者添加的文件从working directory添加到staged area,再从staged area添加到history
git push                                                                  //提交进入github库,并进行远程github网站项目同步
git reset                                                                 //消除上一步的git操作
git config --global user.email "dreamthen.00@gmail.com"                   //设置默认提交的邮箱为dreamthen.00@gmail.com
git config --global user.name "dreamthen"                                 //设置默认提交的姓名为dreamthen
git config --list                                                         //显示设置列表
git init                                                                  //初始化一个git项目,会出现一个.git文件,其中都是初始化的文件
git log                                                                   //显示之前提交过到github上所有版本commit的记录
git reset --hard [git log想要回到过去的版本号]                              //回到过去提交代码之前项目的状态
git reflog                                                                //显示过去每一次操作项目的状态记录
git reset --hard [git reflog想要去往将来的版本号]                           //去往将来最新一次提交代码项目的状态
git checkout master                                                       //切换到master分支
git merge origin/dueTo1008-1027                                           //将dueTo1008-1027分支合并到master分支上
git rm README.md                                                          //git永久删除文件README.md
git rm --cached README.md                                                 //git删除远程分支文件README.md,本地working directory还保留有文件README.md
git mv README.md README.txt                                               //git对文件名字进行修改,rename
git stash                                                                 //想要使得自己修改的文件回到修改前最原始的状态,包含(git add之后git commit之前)
git stash list                                                            //列出git stash命令的操作历史列表
git stash pop                                                             //想要使得自己修改的文件回到git stash列表里面最新git stash状态,git commit之后
git cat-file -t HEAD                                                      //查找HEAD文件中的commit状态
git cat file -p HEAD                                                      //查找HEAD文件中的commit提交版本状态中的git tree码
git cat-file -t 7a78c                                                     //查找git tree码中commit状态,显示tree
git cat-file- p 7a78c                                                     //查找git tree码中文件tree码或者blob码
git branch test                                                           //新建一个分支test
git branch -d test                                                        //删除分支test
git checkout 分支名(test)                                                  //切换分支到某个分支,比如test分支
git checkout -b test                                                      //新建一个分支test,并切换到test分支
git log --oneline                                                         //显示之前提交过到github上所有版本commit 简化版的记录
~~~
##tree-ish
~~~javascript
cd .git
cat refs/heads/master                                                     //获取到master版本现在的git码
git cat-file -t master                                                    //获取到master版本现在的状态commit
git cat-file -p master                                                    //获取到master版本现在的状态commit git tree码
git log --oneline                                                         //显示之前提交过到github上所有版本commit 简化版的记录
git rev-parse HEAD                                                        //获取到HEAD文件中的commit提交版本状态中的git tree码
git rev-parse HEAD~                                                       //获取到HEAD~指向的HEAD下层提交commit版本状态中的git tree码
git rev-parse HEAD~4                                                      //获取到HEAD~4指向的HEAD~3下层提交commit版本状态中的git tree码
git rev-parse HEAD~4^{tree}                                               //获取到HEAD~4指向的HEAD~3下层提交commit版本状态中的git tree独有码
git cat-file -p HEAD~4:readme.md                                          //获取到HEAD~4指向的HEAD~3下层提交commit版本状态中的reademe.md内容describle介绍和method方法
~~~
#树型结构Tree
##ant design树型结构
#nodeJs
##node命令
~~~javascript
node -v                                                                   //获取到本机的nodeJs的版本
node                                                                      //输入node命令如同进入了浏览器控制台,由于都是用的Chrome的V8引擎,所以可以输入并运行javascript代码
node me.js                                                                //也可以运行javascript文件以及文件中的代码
npm init                                                                  //对于npm依赖包进行初始化
npm install jquery --save                                                 //npm下载外部依赖jquery包,并保存在npm init初始化的package.json中
~~~
##淘宝镜像cnpm
~~~javascript
npm install -g cnpm --registry=https://registry.npm.taobao.org            //npm从内网https://registry.npm.taobao.org下载淘宝镜像cnpm,这样下载外部依赖包下载速度会秒下
cnpm install jquery --save                                                //用淘宝镜像cnpm下载外部依赖包jquery包,并保存在npm init初始化的package.json中,速度很快,秒下
~~~
##淘宝镜像cnpm bug
~~~javascript
//下载多个外部依赖包会出现循环依赖,因此不建议用cnpm进行下载外部依赖包
//改进:
npm config set registry https://registry.npm.taobao.org                  //使用npm下载外部依赖包并走淘宝镜像下载路线,不会出现循环依赖
~~~
##NodeJs原理
~~~javascript
const fs = require("fs");
fs.readFile("me.json", (error, data)=>{
  if(error) throw error;
  console.log(data);
});
console.log("why first is me");                                           //先打印why first is me
                                                                          //再打印<Buffer 7b 0a 09 22 6e 61 6d 65 22 3a 22 47 61 72 79 22 0a 7d 0a>
~~~
~~~javascript
const fs = require("fs");
const data = fs.readFileSync("me.json");
console.log(data);
fs.readFile("me.json",(error, data)=>{
  if(error) throw error;
  console.log(data);
})
read = (name, callback) =>{
  callback(name);
}
read("CLAY",(name)=>{
  console.log("why is "+name);
});
console.log("why first is me");                                            //在控制台中显示:
                                                                           //<Buffer 7b 0a 09 22 6e 61 6d 65 22 3a 22 47 61 72 79 22 0a 7d 0a>
                                                                           //why is CLAY
                                                                           //why first is me
                                                                           //<Buffer 7b 0a 09 22 6e 61 6d 65 22 3a 22 47 61 72 79 22 0a 7d 0a>
~~~
##使用express
~~~javascript
const express = require("express");
const app = express();
app.get("/", (req, res)=>{
  res.send("Hello World");
});
app.listen(3000);                                                          //nodeJs express监听端口3000,地址localhost:3000网站显示Hello World
~~~
#react
##react project
~~~javascript
/**
  ListItem
*/
const ListItem = React.createClass({
  remove(){
    this.props.onRemove(this.props.id);
  },
  update(){
    this.props.onUpdate(this.props.id,this.props.name);
  },
  render(){
    return(
      <li className="list-group-item" id={this.props.id}>
          {this.props.name}
          <i className="glyphicon glyphicon-ban-circle" onClick={this.remove}>
          
          </i>
          <i className="glyphicon glyphicon-edit" onClick={this.update}>
          
          </i>
      </li>
    )
  }
});

/**
  ListEditItem
*/
const ListEditItem = React.createClass({
  getInitialState(){
    return {
      name:this.props.name
    }
  },
  changeHandle(event){
    this.setState({
      name:event.target.value
    })
  },
  save(){
    this.props.onSave(this.props.id,this.state.name);
  },
  remove(){
    this.props.onRemove(this.props.id);
  },
  render(){
    return(
      <li className="list-group-item" id={this.props.id}>
          <input type="text" value={this.state.name} onChange={this.changeHandle} />
          <i className="glyphicon glyphicon-share share-person" onClick={this.save}>
            
          </i>
          <i className="glyphicon glyphicon-ban-circle share-person" onClick={this.remove}>
          
          </i>
      </li>
    )
  }
})

/**
  List
*/
const List = React.createClass({
  getInitialState(){
    return{
       list:new Map(),
       editList:new Map(),
       key:0
    }
  },
  
  add(){
    const {editList} = this.state;
    let key = ++this.state.key;
    editList.set(key,{name : ""});
    this.forceUpdate();
  },
  
  removeList(id){
    const {list} = this.state;
    list.delete(id);
    this.forceUpdate();
  },
  
  updateList(id,name){
    const {list, editList} = this.state;
    list.delete(id);
    editList.set(id, {name:name});
    this.forceUpdate();
  },
  
  removeEditList(id){
    const {editList} = this.state;
    editList.delete(id);
    this.forceUpdate();
  },
  
  saveEditList(id, name){
    const {list, editList} = this.state;
    editList.delete(id);
    list.set(id,{name:name});
    this.forceUpdate();
  },
  
  render(){
    const listDom = [];
    const listEditDom = [];
    const {list, editList} = this.state;
    for(let item of list){
        listDom.push(<ListItem id={item[0]} key={item[0]} name={item[1].name} onRemove={this.removeList} onUpdate={this.updateList}/>);
    }
    for(let editItem of editList){
        listEditDom.push(<ListEditItem id={editItem[0]} key={editItem[0]} name={editItem[1].name} onRemove={this.removeEditList} onSave={this.saveEditList}/>);
    }
    return(
       <div className="container">
         <button className="btn btn-default" onClick={this.add}>Add</button>
         <ul className="list-group">
            {listDom}
            {listEditDom}
         </ul>
       </div> 
    )
  }
});
ReactDOM.render(<List />,document.getElementById("containerDiv"));
~~~
~~~css
@charset "utf-8"
.list-group{
  margin-top: 6px; 
}
.list-group-item > i {
    float: right;
    font-size: 20px;
    cursor: pointer;
    margin-right: 8px;
    color: rgb(59, 111, 165);
}

.add-person {
    outline: none;
    border-width: 0 0 1px 0;
    width: 150px;
}

.list-group-item > i.share-person {
    float: none;
    position: relative;
    display: inline-block;
    top:4px;
}
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
<link rel="stylesheet" type="text/css" href="bootstrap.min.css">
<link rel="stylesheet" type="text/css" href="reactTest.css">
<script type="text/javascript" src="jquery.min.js"></script>
<script type="text/javascript" src="bootstrap.min.js"></script>
<script type="text/javascript" src="react.min.js"></script>
<script type="text/javascript" src="react-dom.min.js"></script>
<script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div id="containerDiv"></div>
<script type="text/babel" src="reactTest.js"></script>
</body>
</html>
~~~
##react optimise project
~~~javascript
/**
  ListItem
*/
const ListItem = React.createClass({
  getInitialState(){
    return{
      isEdit:true
    }
  },
  save(){
    const {id} = this.props;
    this.props.onSave(id, this.refs.inputText.value);
    this.setState({
      isEdit:false
    });
  },
  remove(){
    const {id} = this.props;
    this.props.onRemove(id);
  },
  update(){
    this.setState({
      isEdit:true
    })
  },
  render(){
    const {isEdit} = this.state; 
    return(
      {
        isEdit ? <li className="list-group-item" id={this.props.id}>
          <input ref="inputText" defaultValue={this.props.name} className="add-person" type="text" />
          <i className="glyphicon glyphicon-share share-person" onClick={this.save}>
          
          </i>
          <i className="glyphicon glyphicon-ban-circle share-person" onClick={this.remove}>
          
          </i>
        </li>:<li className="list-group-item" id={this.props.id}>
          this.props.name
          <i className="glyphicon glyphicon-ban-circle" onClick={this.remove}>
          
          </i>
          <i className="glyphicon glyphicon-edit" onClick={this.update}>
          </i>
        </li>
      }
    )
  }
});
/**
  List
*/
const List = React.createClass({
  getInitialState(){
    return{
      list:new Map(),
      key:0
    }
  },
  add(){
    const {list} = this.state;
    let key = ++this.state.key;
    list.set(key, {name:""});
    this.forceUpdate();
  },
  saveList(id, name){
    const {list} = this.state;
    list.set(id, {name:name});
    this.forceUpdate();
  },
  removeList(id){
    const {list} = this.state;
    list.delete(id);
    this.forceUpdate();
  },
  render(){
    const listDom = [];
    const {list} = this.state;
    for(let item of list){
      listDom.push(<ListItem id={item[0]} key={item[0]} name={item[1].name} onSave={this.saveList} onRemove={this.removeList}/>);
    }
    return(
      <div className="container">
        <button className="btn btn-default" onClick={this.add}>Add</button>
        <ul className="list-group">
          {listDom}
        </ul>
      </div>
    )
  }
});
~~~
~~~css
@charset "utf-8"
.list-group{
  margin-top: 6px; 
}
.list-group-item > i {
    float: right;
    font-size: 20px;
    cursor: pointer;
    margin-right: 8px;
    color: rgb(59, 111, 165);
}

.add-person {
    outline: none;
    border-width: 0 0 1px 0;
    width: 150px;
}

.list-group-item > i.share-person {
    float: none;
    position: relative;
    display: inline-block;
    top:4px;
}
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
<link rel="stylesheet" type="text/css" href="bootstrap.min.css">
<link rel="stylesheet" type="text/css" href="reactTest.css">
<script type="text/javascript" src="jquery.min.js"></script>
<script type="text/javascript" src="bootstrap.min.js"></script>
<script type="text/javascript" src="react.min.js"></script>
<script type="text/javascript" src="react-dom.min.js"></script>
<script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div id="containerDiv"></div>
<script type="text/babel" src="reactTest.js"></script>
</body>
</html>
~~~
##JSX语法
~~~javascript
const ListItem = React.createClass({
  render(){
    return(
      <li className="list-group-item" style={{backgroundColor:"#2dc3e8"}}>
          one one Line!
      <li>
    )
  }
});
//可以以JSX标签的形式来显示
ReactDOM.render(<ul className="list-group">
  <li className="list-group-item">
    one one Line!
  </li>
  <li className="list-group-item">
    one one Line!
  </li>
</ul>,document.getElementById("containerDiv"));
//也可以用Javascript的形式来显示
ReactDOM.render(React.createElement('ul',{className:"list-group"},
[React.createElement('li',{className:"list-group-item"},'one one Line!'),
 React.createElement('li',{className:"list-group-item"},'one one Line!')
 ]));
//JSX标签形式显示属性
ReactDOM.render(<ul className="list-group">
  <li className="list-group-item" style={{backgroundColor:"#2dc3e8"}}>one one Line!</li>
  <ListItem />
</ul>,document.getElementById("containerDiv"));
//Javascript形式显示属性
ReactDOM.render(React.createElement('ul',{className:"list-group"},
[React.createElement('li',{className:"list-group-item",style:{backgroundColor:"#2dc3e8"}},'one one line!'),
React.createElement(ListItem)]),document.getElementById("containerDiv"));
//JSX标签形式-三元运算符
const bool = false;
ReactDOM.render(<ul className="list-group">
  {
      bool ? <ListItem/><ListItem/>:<h1 style={{backgroundColor:"#2dc3e8"}}>Clown Laugh At You</h1><ListItem/>
  }
</ul>,document.getElementById("containerDiv"));
//Javascript形式-三元运算符
ReactDOM.render(React.createElement('ul',{className:"list-group"},
bool ? [React.createElement(ListItem),React.createElement(ListItem)] : [React.createElement('h1',{style:{backgroundColor:"#2dc3e8"}},'Clown Laugh At You'),React.createElement(ListItem)]));
//JSX标签形式-三元运算符+数组
const bool = false;
const result = [];
if(bool){
  result.push(<ListItem/>);
  result.push(<ListItem/>);
}else{
  result.push(<h1 style={{backgroundColor:"#2dc3e8"}}>Clown Laugh At You</h1>);
  result.push(<ListItem/>);
}
ReactDOM.render(<ul className="list-group">
  {result}
  <ListItem/>
</ul>,document.getElementById("containerDiv"));
//Javascript形式-三元运算符+数组
const bool = false;
const result = [];
if(bool){
  result.push(React.createElement(ListItem));
  result.push(React.createElement(ListItem));
}else{
  result.push(React.createElement('h1',{style:{backgroundColor:"#2dc3e8"}},'Clown Laugh At You'));
  result.push(React.createElement(ListItem));
}
ReactDOM.render(React.createElement('ul',{className:"list-group"},
[result,React.createElement(ListItem)]));
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
  <head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactText.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
  </head>
  <body>
    <div id="containerDiv">
    </div>
    <script type="text/babel" src="reactText.js"></script>
  </body>
</html>
~~~
##Component和Element
~~~javascript
HTML tag标签只是做描述 --- DOM才是其形成的原理
react Element只是做描述 --- Component组件才是其进行搭建框架的main structure
~~~
~~~javascript
//es5语法
const ref = {
  test(){
    console.log("Legend!"+this.props.group);
  }
};

const Item = React.createClass({
  //displayName:"Item"
  getInitialState(){
    return {
      List:[]
    }
  },
  getDefaultProps(){
    return {
      group:"CLAY"
    }
  },
  mixins:[ref],
  render(){
    return {
      <div>
         <h1 style={{backgroundColor:"#2dc3e8"}}>Clown Laugh At You!{this.props.group}</h1>
         <input type="button" onClick={this.test} value="Click it"/>
      </div>
    }
  }
});
//es6语法
class Item extends React.Component {
  //displayName:"Item"
  constructor(props) {
    super(props);
    //getInitialState
    this.state = {
      List:[]
    }
  }
  //getDefaultProps
  static get defaultProps() {
    return {
      group:"CLAY"
    }
  }
  //mixins
  test(){
    console.log("Legend!"+this.props.group);
  }
  render() {
    return {
      <div>
         <h1 style={{backgroundColor:"yellow"}}>Clown Laugh At You!{this.props.group}</h1>
         <input type="button" onClick={this.test.bind(this)} value="Click it"/>
      </div>
    }
  }
}
//ReactDOM.render(<Item />,document.getElementById("containerDiv"));
ReactDOM.render(React.createElement(Item),document.getElementById("containerDiv"));
//在界面显示
//Clown Laugh At You!CLAY(背景为黄色)
//在控制台中打印
//Legend!CLAY
~~~
##生命周期
###初始化阶段
~~~javascript
const Item = React.createClass({
  displayName:"Item",
  getInitialState(){
    console.log("get initial state");
    return{
      main:"Clown Laugh At You!"
    }
  },
  getDefaultProps(){
    console.log("get default props");
    return{
      group:"Gary Love Zhaoy!"
    }
  },
  render(){
    return (
      <div>
        {this.state.main + this.props.group}
      </div>
    )
  }
});
ReactDOM.render(<div><Item /><Item /><Item /></div>,document.getElementById("containerDiv"));
//在界面上显示
//Clown Laugh At You!Gary Love Zhaoy!
//Clown Laugh At You!Gary Love Zhaoy!
//Clown Laugh At You!Gary Love Zhaoy!
//在控制台中打印
//get default props
//get initial state
//get initial state
//get initial state
~~~
###装载阶段
~~~javascript
const Item = React.createClass({
  displayName:"Item",
  getInitialState(){
    console.log("get initial state");
    return {
       main:"Clown Laugh At You!"
    }
  },
  getDefaultProps(){
    console.log("get default props");
    return {
       group:"Gary Love Zhaoy!"
    }
  },
  componentWillMount(){
    console.log("component will mount");
  },
  componentDidMount(){
    console.log("component did mount");
  },
  render(){
    console.log("render");
    return(
      <div>
        {this.state.main + this.props.group}
      </div>
    )
  }
});
ReactDOM.render(<Item />,document.getElementById("containerDiv"));
//在界面上显示
//Clown Laugh At You!Gary Love Zhaoy!
//在控制台中显示
//get default props
//get initial state
//component will mount
//render
//component did mount
~~~
###更新阶段
~~~javascript
const Item = React.createClass({
  displayName:"Item",
  getInitialState(){
    console.log("get initial state");
    return {
       main:"Clown Laugh At You!"
    }
  },
  getDefaultProps(){
    console.log("get default props");
    return {
       group:"Gary Love Zhaoy!"
    }
  },
  componentWillMount(){
    console.log("component will mount");
  },
  componentDidMount(){
    console.log("component did mount");
  },
  test(){
    this.setState({
        main:"Google!"
    });
  },
  componentWillReceiveProps(nextProps){
    console.log("component will receive props");
  },
  componentWillUpdate(nextPorps, nextState){
    console.log("component will update");
  },
  componentDidUpdate(oldProps, oldState){
    console.log("component did update");
    const dom = ReactDOM.findNodeDOM(this);
    dom.style.backgroundColor = "#2dc3e8";
    let bool = false;
    setInterval(function(){
        if(bool){
          dom.style.backgroundColor = "#2dc3e8";
          bool = false;
        }else{
          dom.style.backgroundColor = "yellow";
          bool = true;
        }
    },2000);
  },
  shouldComponentUpdate(nextProps, nextState){
    console.log("should component update");
    return true;
  },
  render(){
    console.log("render");
    return(
      <div>
        {this.state.main + this.props.group}
        <input type="button" value="click it" onClick={this.test.bind(this)} />
      </div>
    )
  }
});
function render(){
  ReactDOM.render(<Item />,document.getElementById("containerDiv"));
}
render();
render();
//在界面上显示
//Clown Laugh At You!Gary Love Zhaoy!click it按钮
//背景在两秒之内黄蓝交替呈现
//在控制台中显示
//get default props
//get initial state
//component will mount
//render
//component did mount
//should component update
//component will update
//render
//component did update
//点击按钮之后,在界面中显示
//Google!Gary Love Zhaoy!click it按钮
//背景在两秒之内黄蓝交替呈现
//点击按钮之后,在控制台中显示
//should component update
//component will update
//render
//component did update
//如果shouldComponentUpdate中返回true,且点击按钮之后使用了this.setState,点击按钮之后
//在控制台中显示
//should component update
//component will update
//render
//component did update
//如果shouldComponentUpdate中返回false,且点击按钮之后使用了this.setState,点击按钮之后
//在控制台中显示
//should component update
//如果shouldComponentUpdate中返回true,且点击按钮之后使用了this.forceUpdate,点击按钮之后
//在控制台中显示
//component will update
//render
//component did update
//如果shouldComponentUpdate中返回false,且点击按钮之后使用了this.forceUpdate,点击按钮之后,同上
~~~
###卸载阶段
~~~javascript
const Item = React.createClass({
  displayName:"Item",
  getInitialState(){
    console.log("get initial state");
    return {
       main:"Clown Laugh At You!",
       loopName:""
    }
  },
  getDefaultProps(){
    console.log("get default props");
    return {
       group:"Gary Love Zhaoy!"
    }
  },
  componentWillMount(){
    console.log("component will mount");
  },
  componentDidMount(){
    console.log("component did mount");
  },
  test(){
    this.setState({
        main:"Google!"
    });
  },
  componentWillReceiveProps(nextProps){
    console.log("component will receive props");
  },
  componentWillUpdate(nextPorps, nextState){
    console.log("component will update");
  },
  componentDidUpdate(oldProps, oldState){
    console.log("component did update");
    const dom = ReactDOM.findNodeDOM(this);
    dom.style.backgroundColor = "#2dc3e8";
    let bool = false;
    this.state.loopName = setInterval(function(){
        if(bool){
          dom.style.backgroundColor = "#2dc3e8";
          bool = false;
        }else{
          dom.style.backgroundColor = "yellow";
          bool = true;
        }
    },2000);
  },
  shouldComponentUpdate(nextProps, nextState){
    console.log("should component update");
    return true;
  },
  componentWillUnmount(){
    console.log("component will unmount");
    clearInterval(this.state.loopName);
  },
  render(){
    console.log("render");
    return(
      <div>
        {this.state.main + this.props.group}
        <input type="button" value="click it" onClick={this.test.bind(this)} />
      </div>
    )
  }
});
function render(bool){
  React.render(<div><Item />{bool ? <Item /> : ""}</div>,document.getElementById("containerDiv"));
}
render(true);
$("#clear").on("click",function(e){
  render();
});
//在界面中显示
//Clown Laugh At You!Gary Love Zhaoy!click it按钮
//Clown Laugh At You!Gary Love Zhaoy!click it按钮
//背景在两秒之内黄蓝交替呈现
//点击clear按钮之后,在控制台中显示
//component will receive props
//should component update
//component will update
//render
//component will unmount
//component did update
~~~
###生命周期Demo
~~~javascript
let list = [];
const database = {
  add(newGroupData){
    list.push(newGroupData);
    return list.length - 1;
  },
  del(index){
    list[index] = null;
  },
  update(index,newGroupData){
    list.splice(index,1,newGroupData);
  },
  get list(){
    return list;
  }
};
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      value:this.props.value,
      dbKey:0,
      currentHistoryIndex:0,
      history:[this.props.value]
    }
  }
  
  static get defaultProps(){
    return {
      value:"no value"
    }
  }
  
  componentWillMount(){
    console.log("component will mount");
  }
  
  componentWillReceiveProps(){
    console.log("component will receive props");
  }
  
  shouldComponentUpdate(){
    console.log("should component update");
  }
  
  componentWillUpdate(){
    console.log("component will update");
  }
  
  componentDidUpdate(){
    console.log("component did update");
  }
  
  componentDidMount(){
    console.log("component did mount");
  }
  
  onChangeHandler(event){
    this.setState({
      value:event.target.value
    });
  }
  
  render(){
    const {value,history,currentHistoryIndex} = this.state; 
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group" style={{marginTop:"8px"}}>
            <input type="text" className="form-control" ref="inputText" value={value} onChange={this.onChangeHandler.bind(this)} style={{width:"90%",display:"inline-block",marginRight:"8px",float:"left"}}/>
            <button className="btn btn-info" onClick={this.save.bind(this)} style={{width:"8%",display:"inline-block",float:"left"}}>save</button>
          </div>
          <div className="form-group" style={{marginTop:"8px"}}>
            <button className="btn btn-default" onClick={this.prev.bind(this)}>prev</button>
            <def className="display:inline-block;height:34px;line-height:34px;padding:0 8px;">history[currentHistoryIndex]</def>
            <button className="btn btn-default" onClick={this.next.bind(this)}>next</button>
          </div>
        </div>
      </div>
    )
  }
}

ReactDOM.render(<Item />,document.getElementById("containerDiv"));
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
  <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
  <link rel="stylesheet" type="text/css" href="reactTest.css">
  <script type="text/javascript" src="jquery.min.js"></script>
  <script type="text/javascript" src="bootstrap.min.js"></script>
  <script type="text/javascript" src="react.min.js"></script>
  <script type="text/javascript" src="react-dom.min.js"></script>
  <script type="text/javascript" src="browser.js"></script>
</head>
<body>
  <div id="containerDiv">
  
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
</html>
~~~
