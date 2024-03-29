# arrange
用来整理我的前端所学知识，以及样式和插件的汇总
# HTML与HTML5
## 常用标签
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
git clone -b origin/release git@github.com:dreamthen/Altitude.git         //对项目进行分支选择克隆并复制到本地
git push origin boss-christmas-dueTo1222                                  //将新建的boss-christmas-dueTo1222分支push到远程
git status                                                                //显示出此git项目其中改动文件的状态
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
##模块化
~~~javascript
//在module文件夹中的模块js module.js
console.log("This is a module~");
module.exports = function moduleOne(){
  console.log("moduleOne");
}
//在module文件夹之外的nodeModule.js
const moduleOne = require("./module/module");
moduleOne();
moduleOne();
//执行结果:
//This is a module~
//moduleOne
//moduleOne
//在module文件夹中的模块js moduleAno.js
console.log("This is a moduleAno~");
exports.moduleOne = function(){
  console.log("moduleOne");
}

exports.moduleTwo = function(){
  console.log("moduleTwo");
}
//在module文件夹之外的nodeModuleAno.js
const module = require("./module/moduleAno");
module.moduleOne();
module.moduleOne();
module.moduleTwo();
//执行结果:
//This is a moduleAno~
//moduleOne
//moduleOne
//moduleTwo
~~~
##统一的事件驱动
~~~javascript
//先执行如下命令下载依赖包
npm install events --save
npm install util --save
//然后编写事件驱动代码
const eventEmitter = require("events").EventEmitter;
const util = require("util");
function MyEvent(){
  eventEmitter.call(this);
}
util.inherits(MyEvent, eventEmitter);
const emitter = new MyEvent();
emitter.on("changeName", (name)=>{
  console.log("This is a person, his name is",name);
});
emitter.emit("changeName", "Clown Laugh At You~");
//运行node nodeEvents
//运行结果如下:
//This is a person, his name is Clown Laugh At You~
~~~
##Http Client 客户端
~~~javascript
const http = require("http");
http.get({
  hostname:"baidu.com",
  path:"/",
  port:80
},(res)=>{
  let bufList = [];
  res.on("readable", ()=>{
    let buffer = res.read();
    if(buffer) {
      bufList.push(buffer);
      console.log(bufList.toString());
    } else {
      let result = Buffer.concat(bufList);
      console.log(result.toString());
    }
  });
});
console.log("head end~");
//运行node nodeHttpClient.js
//运行结果如下:
//head end~
//<html>
//<meta http-equiv="refresh" content="0;url=http://www.baidu.com/">
//</html>
~~~
##Http Server 服务器端
~~~javascript
const http = require("http");
const fs = require("fs");
let server = http.createServer((req, res)=>{
  res.writeHead(200, {"Content-Type":"text/html"});
  fs.readFile("./html/http.html", (err, data)=>{
    if(err) throw err;
    res.end(data);
  });
});
server.listen(3000);
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <title>nodeJs</title>
</head>
<body>
    <h1 style="color: #2dc3e8;">Hello Http Server Api~</h1>
    <h3>Very Cool</h3>
</body>
</html>
~~~
##Http Server 服务器端(灵活)
~~~javascript
const http = require("http");
const fs = require("fs");
let server = http.createServer();
server.on("request", (req, res)=>{
  res.writeHead(200,{"Content-Type", "text/html"});
  fs.readFile("./html/http.html",(err, data)=>{
    if(err) throw err;
    res.end(data);
  });
});
server.on("request",(req, res)=>{
  console.log("log......");
});

server.listen(3000);
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <title>nodeJs</title>
</head>
<body>
    <h1 style="color: #2dc3e8;">Hello Http Server Api~</h1>
    <h3>Very Cool</h3>
</body>
</html>
~~~
##文件系统和数据流
~~~javascript
const http = require("http");
const fs = require("fs");
let server = http.createServer();
server.on("request", (req, res)=>{
  res.writeHead(200,{"Content-Type", "text/html"});
  fs.readFile("./html/http.html",(err, data)=>{
    if(err) throw err;
    res.end(data);
  });
  let readStream = fs.createReadStream("./affair/message.txt");
  let writeStream = fs.createWriteStream("./affair/me.txt");
  readStream.on("data", (data)=>{
    writeStream.write(data);
  });
  readStream.on("end", ()=>{
    console.log("read end~");
    writeStream.end();
  });
  fs.watchFile("./affair/me.txt",(event,fileName)=>{
    console.log("文件发生改动~~");
  });
});

server.on("request",(req, res)=>{
  console.log("log......");
});

server.listen(3000);
//在node控制台中显示如下:
//log......
//read end~
//log......
//read end~
//文件发生改动~~
//文件发生改动~~
//生成me.txt文件，me.txt内容与message.txt内容相同
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <title>nodeJs</title>
</head>
<body>
    <h1 style="color: #2dc3e8;">Hello Http Server Api~</h1>
    <h3>Very Cool</h3>
</body>
</html>
~~~
##集群实例
~~~javascript
const cluster = require("cluster");
const http = require("http");
const npmCpus = require("os").cpus().length;
if(cluster.isMaster){
  console.log("主进程");
  for(let i = 0; i < npmCpus; i++){
    cluster.fork();
  }
} else {
  console.log("子进程");
  let server = http.createServer();
  server.on("request", (req, res)=>{
    res.writeHead(200,{"Content-Type": "text/html"});
    fs.readFile("./html/html.html", (err, data)=>{
      if(err) throw err;
      res.end(data);
    });
  });
  
  server.on("request",()=>{
    console.log("log......");
  });
  server.listen(3000);
}
//在node控制台中显示如下:
//主进程
//子进程
//子进程
//log......
//log......
~~~
~~~html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <title>nodeJs</title>
</head>
<body>
    <h1 style="color: #2dc3e8;">Hello Http Server Api~</h1>
    <h3>Very Cool</h3>
</body>
</html>
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
##React生命周期
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
###React生命周期Demo
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
      history:[this.props.value],
      loopName:""
    }
  }
  
  static get defaultProps(){
    return {
      value:"no value"
    }
  }
  
  componentWillMount(){
    console.log("component will mount");
    const {value} = this.state;
    let dbKey = database.add({value:value});
    this.setState({
      dbKey
    });
  }
  
  componentWillReceiveProps(){
    console.log("component will receive props");
  }
  
  shouldComponentUpdate(){
    console.log("should component update");
    return true;
  }
  
  componentWillUpdate(){
    const {dbKey,value} = this.state;
    console.log("component will update");
    database.update(dbKey, {value:value});
  }
  
  componentDidUpdate(){
    console.log("component did update");
    const {dom} = this.refs.inputText;
    dom.style.border = "1px solid rgb(217,237,247)";
    setTimeout(function(){
      dom.style.border = "none";
    },2000);
  }
  
  componentDidMount(){
    console.log("component did mount");
    const {dom} = ReactDOM.findDOMNode(this);
    dom.style.backgroundColor = "rgb(217,237,247)";
    let bool = false;
    
    this.state.loopName = setInterval(function(){
        if(bool) {
          dom.style.backgroundColor = "rgb(217,237,247)";
          bool = false;
        } else {
          dom.style.backgroundColor = "#fff";
          bool = true;
        }
    },1000);
  }
  
  componentWillUnmount(){
    console.log("component will unmount");
    const {loopName} = this.state;
    clearInterval(loopName);
  }
  
  onChangeHandler(event){
    this.setState({
      value:event.target.value
    });
  }
  
  save(){
    const {value} = this.state;
    let {history} = this.state;
    let currentHistoryIndex = this.state.currentHistoryIndex + 1;
    history.push(value);
    this.setState({
      history,
      currentHistoryIndex
    });
  };
  
  prev(){
    let {currentHistoryIndex} = this.state;
    if(currentHistoryIndex !== 0){
      this.setState({
        currentHistoryIndex:currentHistoryIndex - 1;
      })
    }
  };
  
  next(){
    let {currentHistoryIndex,history} = this.state;
    if(currentHistoryIndex !== history.length - 1){
      this.setState({
        currentHistoryIndex:currentHistoryIndex + 1;
      })
    }
  };
  
  render(){
    const {value,history,currentHistoryIndex} = this.state; 
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group form-clear" style={{marginTop:"8px"}}>
            <input type="text" className="form-control" ref="inputText" value={value} onChange={this.onChangeHandler.bind(this)} style={{width:"90%", display:"inline-block", marginRight:"8px", float:"left"}}/>
            <button className="btn btn-info" onClick={this.save.bind(this)} style={{width:"8%", display:"inline-block", float:"left"}}>save</button>
          </div>
          <div className="form-group" style={{marginTop:"8px"}}>
            <button className="btn btn-default" onClick={this.prev.bind(this)}>prev</button>
            <def className="display:inline-block;height:34px;line-height:34px;padding:0 8px;border-radius:4px;backgroundColor:rgb(217,237,247);">history[currentHistoryIndex]</def>
            <button className="btn btn-default" onClick={this.next.bind(this)}>next</button>
          </div>
        </div>
      </div>
    )
  }
}

ReactDOM.render(<Item />,document.getElementById("containerDiv"));
~~~
~~~css
charset "utf-8";
.form-clear::after{
  clear:both;
  display:"block";
  height:0;
  content:".";
  visibility:hidden;
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
  <div id="containerDiv">
      
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
</html>
~~~
##React refs属性
###React refs属性Demo
~~~javascript
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state={
      
    }
  }
  
  static get defaultProps(){
    return {
    
    }
  }
  
  onClickHandler(e){
    const dom = this.refs.inputText;
    dom.focus();
  }
  
  componentDidMount(){
    console.log("component did mount");
    const dom = this.refs.inputText;
    dom.focus();
  }
  
  render(){
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group form-clear">
            <input type="text" ref="inputText" className="form-control" style={{width:"90%", display:"inline-block", float:"left", marginRight:"8px"}}/>
            <button onClick={this.onClickHandler.bind(this)} className="btn btn-default" style={{width:"8%", float:"left", display:"inline-block"}}>click me</button>
          </div>
          <div className="form-group form-clear">
            <input type="text" className="form-control" ref={function(dom){
                console.log("ref component start");
                dom.focus();
            }} style={{width:"90%", display:"inline-block", float:"left"}} />
          </div>
        </div>
      </div>
    )
  }
}
ReactDOM.render(<Comp />,document.getElementById("containerDiv"));
~~~
~~~css
charset "utf-8";
.form-clear::after{
  clear:both;
  content:".";
  visibility:hidden;
  height:0;
  display:block;
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
  <div id="containerDiv">
      
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
</html>
~~~
##React表单事件
###React表单事件Demo
~~~javascript
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      value:this.props.value,
      valueAno:this.props.value,
      checkboxValue:false,
      checkboxValueAno:true,
      radioValue:false,
      selectValue:"乙",
      selectValueArr:["乙","丙"],
      textAreaValue:this.props.value
    }
  }
  
  static get defaultProps(){
    return {
      value:"no value"
    }
  }
  
  onChangeHandler(event){
    this.setState({
      value:event.target.value
    });
  }
  
  onChangeHandlerAno(event){
    this.setState({
      valueAno:event.target.value
    });
  }
  
  onCheckBoxHandler(event){
    let checkboxValue = this.state.checkboxValue;
    this.setState({
      checkboxValue:!checkboxValue
    });
  }
  
  onCheckBoxHandlerAno(event){
    let checkboxValueAno = this.state.checkboxValue;
    this.setState({
      checkboxValueAno:!checkboxValueAno
    });
  }
  
  onRadioHandler(event){
    let radioValue = this.state;radioValue;
    this.setState({
      radioValue:!radioValue
    });
  }
  
  onSelectHandler(event){
    this.setState({
       selectValue:event.target.value
    });
  }
  
  onSelectHandlerArr(event){
    let selectValueArr = [];
    selectValueArr.push(event.target.value);
    this.setState({
      selectValueArr
    });
  }
  
  onTextAreaHandler(event){
    this.setState({
      textAreaValue:event.target.value
    });
  }
  
  render(){
    const {value, valueAno, checkboxValue, checkboxValueAno, radioValue, selectValue, selectValueArr, textAreaValue} = this.state;
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group" style={{marginTop:"8px"}}>
            <label htmlFor="inputTest">React输入框:</label>
            <input id="inputTest" className="form-control" value={value} onChange={this.onChangeHandler.bind(this)} />
          </div>
          <div className="form-group" style={{marginTop:"8px"}}>
            <label htmlFor="inputTestAno">另一个React输入框:</label>
            <input id="inputTestAno" className="form-control" defaultValue={valueAno} onChange={this.onChangeHandlerAno.bind(this)} />
          </div>
          <div className="form-group">
            <label htmlFor="testCheckbox">React复选框</label>
            <input id="testCheckbox" type="checkbox" checked={checkboxValue} onChange={this.onCheckBoxHandler.bind(this)} />
          </div>
          <div className="form-group">
            <label htmlFor="testCheckboxAno">另一个React复选框</label>
            <input id="testCheckboxAno" type="checkbox" defaultChecked={checkboxValueAno} onChange={this.onCheckBoxHandlerAno.bind(this)} />
          </div>
          <div className="form-group">
            <label htmlFor="testRadio">React单选框</label>
            <input id="testRadio" type="radio" checked={radioValue} onChange={this.onRadioHandler.bind(this)}/>
          </div>
          <select className="form-control" value={selectValue} onChange={this.onSelectHandler.bind(this)}>
            <option value="甲">甲</option>
            <option value="乙">乙</option>
            <option value="丙">丙</option>
          </select>
          <select multiple className="form-control" value={selectValueArr} onChange={this.onSelectHandlerArr.bind(this)}>
            <option value="甲">甲</option>
            <option value="乙">乙</option>
            <option value="丙">丙</option>
          </select>
          <textArea className="form-control" value={textAreaValue} onChange={this.onTextAreaHandler.bind(this)}>
          </textArea>
        </div>
      </div>
    )
  }
}

ReactDOM.render(<Comp />,document.getElementById("containerDiv"))
~~~
~~~html
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
##React键盘事件
###React键盘事件Demo
~~~javascript
//根据左(37)、上(38)、右(39)、下(40)
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      top:0,
      left:0
    }
  }
  
  static get defaultProps(){
    return {
      
    }
  }
  
  keyDown(event){
    let {top, left} = this.state;
    switch(event.keyCode){
      case 37:
          if(left > 0){
              this.setState({
                left:left - 5
              });
          }
          break;
      case 38:
          if(top > 0){
              this.setState({
                top:top - 5
              });
          }
          break;
      case 39:
          if(left !== 550){
              this.setState({
                left:left + 5
              });
          }
          break;
      case 40:
          if(top !== 550){
              this.setState({
                top:top + 5
              });
          }    
          break;
    }
  }
  
  render(){
    const {top,left} = this.state;
    return (
      <div className="container outerContainer" tabIndex={1} style={{top:top, left:left}} onKeyDown={this.keyDown.bind(this)}>
        <div className="innerContainer">
        
        </div>
      <div>
    )
  }
}
~~~
~~~css
charset "utf-8";
.outerContainer{
  position:relative;
  width:560px;
  height:560px;
  background-color:rgb(217,237,247);
  z-index:1;
}

.innerContainer{
  position:absolute;
  width:10px;
  height:10px;
  background-color:yellow;
  z-index:2;
}
~~~
~~~html
<!DOCTYPE html>
<html>
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
  <div className="containerDiv">
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##React鼠标事件
###React鼠标事件Demo
~~~javascript
const data = new Map();
data.set("one", {name: "Clown"});
data.set("two", {name: "Laugh"});
data.set("three", {name: "At"});
data.set("four", {name: "You"});
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:this.props.name,
      id:this.props.id
    }
  }
  
  static get defaultProps(){
    return {
      id:"",
      name:""
    }
  }
  
  render(){
    const {id, name} = this.state;
    return (
      <p id={id} draggable={true} onDragStart={this.props.dragStart}>
         {name}
      </p>
    )
  }
}

class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      leftData:new Map(),
      rightData:this.props.data,
      id:""
    }
  }
  
  static get defaultProps(){
    return {
      data:new Map()
    }
  }
  
  drag(id,event){
    this.setState({
      id:id
    });
  }
  
  drop(){
    let {leftData, rightData, id} = this.state;
    let name = rightData.get(id).name;
    leftData.set(id, {name:name});
    rightData.delete(id);
    this.setState({
      leftData:leftData,
      rightData:rightData
    });
  }
  
  dropAno(){
    let {leftData, rightData, id} = this.state;
    let name = leftData.get(id).name;
    rightData.set(id, {name:name});
    leftData.delete(id);
    this.setState({
      leftData:leftData,
      rightData:rightData
    });
  }
  
  render(){
    const {leftData, rightData} = this.state;
    let leftList = [];
    let rightList = [];
    for(let leftItem of leftData){
      leftList.push(<Item key={leftItem[0]} dragStart={this.drag.bind(this,leftItem[0])} id={leftItem[0]} name={leftItem[1].name} />);
    }
    for(let rightItem of rightData){
      rightList.push(<Item key={rightItem[0]} dragStart={this.drag.bind(this,rightItem[0])} id={rightItem[0] name={rightItem[1].name} />);
    }
    return (
      <div className="containerDiv form-clear">
        <div className="leftContainer" onDragEnter={e=>e.preventDefault()} onDragOver={e=>e.preventDefault()} 
             onDrop={this.drop.bind(this)}>
          {leftList}
        </div>
        <div className="rightContainer" onDrapEnter={e=>e.preventDefault()} onDragOver={e=>e.preventDefault()}
             onDrop={this.dropAno.bind(this)}>
          {rightList}
        </div>
      </div>
    )
  }
}
ReactDOM.render(<Comp data={data} />,document.getElementById("containerDiv"));
~~~
~~~css
.form-clear::after{
  clear:both;
  content:".";
  display:block;
  height:0;
  visibility:hidden;
}

.leftContainer,.rightContainer{
  width: 300px;
  height: 400px;
  float: left;
  background-color: #4183c4;
}

.rightContainer{
  background-color: mediumpurple;
}
~~~
~~~html
<!DOCTYPE html>
<html>
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
  <div className="containerDiv">
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##React自定义事件
###React自定义事件Demo
~~~javascript
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:this.props.name
    }
  }
  
  static get defaultProps(){
    return {
      name:"no value"
    }
  }
  
  changeHandler(event){
    let {name} = this.state;
    this.setState({
      name:event.target.value
    });
    this.props.clickDemo(name);
  }
  
  render(){
    const {name} = this.state;
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group">
            <label htmlFor="inputText">React文本框:</label>
            <input id="inputText" type="text" className="form-control" value={name} onChange={this.changeHandler.bind(this)} />
          </div>
        </div>
      </div>
    )
  }
}
function clickDemoEvent(name){
  console.log(name);
}
ReactDOM.render(<Comp clickDemo={clickDemoEvent.bind(this)} />,document.getElementById("containerDiv"));
~~~
~~~html
<!DOCTYPE html>
<html>
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
  <div className="containerDiv">
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##React父与子通信、子与父通信
###React父与子通信、子与父通信Demo
~~~javascript
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:this.props.name,
      actived:this.props.actived
    }
  }
  
  static get defaultProps(){
    return {
      name:"",
      actived:false
    }
  }
  
  componentWillReceiveProps(nextProps){
    if(this.props.actived !== nextProps.actived){
      this.setState({
        actived:nextProps.actived
      });
    }
  }
  
  render(){
    const {name, actived} = this.state;
    let style = actived ? {border:"2px solid #2dc3e8"} : {};
    return (
      <li className="list-group-item" style={style} onClick={this.props.clickItem.bind(this)}>
        {name}
      </li>
    )
  }
}
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      list:[]
    }
  }
  
  static get defaultProps(){
    return {
      data:[]
    }
  }
  
  componentWillMount(){
    let list = this.props.data.map((dataItem, dataIndex) => {
       return {name:dataItem, actived:false};
    });
    this.setState({
       list: list
    });
  }
  
  componentDidMount(){
    const {list} = this.state;
    setTimeout(() => {
      list[2].actived = true;
      this.setState({
        list:list
      });
    },3000);
  }
  
  sayItem(name){
    alert(name);
  }
  
  render(){
    let {list} = this.state;
    let listMine = list.map((listItem, listIndex) => {
       return <Item clickItem={this.sayItem.bind(this,listItem.name)} actived={listItem.actived} name={listItem.name}/>
    });
    return (
      <div className="container">
        <ul className="list-group">
            {listMine}
        </ul>
      </div>
    )
  }
}
const data = [
  "AAA",
  "BBB",
  "CCC",
  "DDD"
];
ReactDOM.render(<Comp data={data} />,document.getElementById("containerDiv"));
~~~
~~~html
<!DOCTYPE html>
<html>
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
  <div className="containerDiv">
  </div>
  <script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##事件总线
###事件总线Demo one
~~~javascript
//下载bower
npm install -g bower
//初始化bower
bower init
//下载EventEmitter
bower install eventEmitter --save
~~~
~~~javascript
const busEventEmitter = new EventEmitter();
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:this.props.name,
      actived:this.props.actived
    }
  }

  static get defaultProps(){
    return {
      name:"",
      actived:false
    }
  }
  
  componentWillReceiveProps(nextProps){
    if(this.props.actived !== nextProps.actived){
      this.setState({
         actived:nextProps.actived
      });
    }
  }
  
  render(){
    let {name,actived} = this.state;
    let style = actived ? {border:"2px solid #2dc3e8"} : {};
    return (
      <li className="list-group-item" style={style} onClick={this.props.alertName.bind(this)}>
        {name}
      </li>
    )
  }
}
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      list:[],
      name:this.props.name
    }
  }

  static get defaultProps(){
    return {
      data:[],
      name:""
    }
  }
  
  componentWillMount(){
    let {name} = this.state;
    let list = this.props.data.map((dataItem,dataIndex)=>{
        return {name:dataItem,actived:false};
    });
    this.setState({
        list
    });
    this.props.busEvent.on("test_event",()=>{
        console.log(name);
    });
  }
  
  componentDidMount(){
    let {list} = this.state;
    setTimeout(()=>{
      list[2].actived = true;
      this.setState({
         list
      });
    },3000);
  }
  
  sayName(name){
    alert(name);
  }
  
  render(){
    let {list} = this.state;
    let listDOM = list.map((listItem,listIndex)=>{
      return <Item name={listItem.name} actived={listItem.actived} alertName={this.sayName.bind(this,listItem.name)} />;
    });
    return (
      <div className="container">
        <ul className="list-group">
          {listDOM}
        </ul>
      </div>
    )
  }
}
const data = [
    "AAA",
    "BBB",
    "CCC",
    "DDD"
];
ReactDOM.render(<div><Comp data={data} busEvent={busEventEmitter} name="component first"/><Comp data={data} busEvent={busEventEmitter} name="component second"/></div>,document.getElementById("containerDiv"));
setTimeout(()=>{
  busEventEmitter.emit("test_event");
},5000);
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="EventEmitter.js"></script>
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
###事件总线Demo two
~~~javascript
const busEventEmitter = new EventEmitter();
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:this.props.name,
      color:this.props.color,
      colorIndex:this.props.id,
      id:this.props.id
    }
  }
  
  static get defaultProps(){
    return {
      name:"",
      color:["rgb(111, 168, 0)", "rgb(254, 114, 0)"],
      colorIndex:0,
      id:0
    }
  }
  
  componentWillMount(){
    this.props.busEvent.on("changeColor", (idAno, colorAno, colorIndexAno)=>{
        if(this.state.id !== idAno && this.state.color[this.state.colorIndex] === colorAno[colorIndexAno]){
          this.changeColor();
        }
    });
  }
  
  changeColor(){
    let {colorIndex} = this.state;
    this.setState({
      colorIndex:colorIndex ? 0 : 1
    });
    setTimeout(()=>{
      this.props.busEvent.emit("changeColor", this.state.id, this.state.color, this.state.colorIndex);
    },3000);
  }
  
  render(){
    let {name,color,colorIndex} = this.state;
    return (
      <div className="container" style={{backgroundColor:color[colorIndex],padding:"4px 8px"}}>
        <span className="componentSpan">{name}</span>
        <button className="btn btn-default" onClick={this.changeColor.bind(this)}>click me!</button>
      </div>
    )
  }
}
ReactDOM.render(<div><Comp id={0} name="first Component" busEvent={busEventEmitter} /><Comp id={1} name="seconde Component" busEvent={busEventEmitter} /></div>,document.getElementById("containerDiv"));
~~~
~~~css
.componentSpan {
    display: inline-block;
    margin: 0 6px 0 0;
}
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="EventEmitter.js"></script>
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##react object another
~~~javascript
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
       id:this.props.id,
       name:this.props.name,
       checkJudge:true
    }
  }
  
  static get defaultProps(){
    return {
      id:0,
      name:""
    }
  }
  
  changeHandler(event){
    this.setState({
      name:event.target.value
    });
  }
  
  deleteData(){
    let {id} = this.state;
    this.props.deleteMine.bind(this)(id);
  }
  
  updateData(){
    this.setState({
      checkJudge:true
    });
  }
  
  saveData(){
    this.setState({
      checkJudge:false
    });
  }
  
  render(){
    const {name, checkJudge} = this.state;
    return (
      checkJudge ? <li className="list-group-item">
                      <input className="add-person" type="text" ref="inputText" value={name} onChange={this.changeHandler.bind(this)} />
                      <i className="glyphicon glyphicon-share share-person" onClick={this.saveData.bind(this)}>
                      
                      </i>
                      <i className="glyphicon glyphicon-ban-circle share-person" onClick={this.deleteData.bind(this)}>
                        
                      </i>
                   </li>:<li className="list-group-item">
                      {name}
                      <i className="glyphicon glyphicon-edit" onClick={this.updateData.bind(this)}>
                      
                      </i>
                      <i className="glyphicon glyphicon-ban-circle" onClick={this.deleteData.bind(this)}>
                        
                      </i>
                   </li>;
    )
  }
}
class Comp extends React.Component{
  consturctor(props){
    super(props);
    this.state = {
      list:new Map(),
      key:0
    }
  }
  
  static get defaultProps(){
    return {
    
    }
  }
  
  add(){
    let {list} = this.state;
    this.state.key = this.state.key + 1;
    list.set(this.state.key, {name:""});
    this.forceUpdate();
  }
  
  delete(id){
    let {list} = this.state;
    list.delete(id);
    this.forceUpdate();
  }
  
  render(){
    const {list} = this.state;
    let listDOM = [];
    for(let listItem of list){
      listDOM.push(<Item key={listItem[0]} id={listItem[0]} name={listItem[1].name} deleteMine={this.delete.bind(this)} />);
    }
    return (
      <div className="container">
        <button className="btn btn-default" onClick={this.add.bind(this)}>Add</button>
        <ul className="list-group">
          {listDOM}
        </ul>
      </div>
    )
  }
}
ReactDOM.render(<Comp />,document.getElementById("containerDiv"));
~~~
~~~css
.list-group {
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
<html>
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
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##react object third
~~~javascript
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
       id:this.props.id,
       name:this.props.name,
       checkJudge:true
    }
  }
  
  static get defaultProps(){
    return {
      id:0,
      name:""
    }
  }
  
  componentWillReceiveProps(nextProps){
    if(this.props.name !== nextProps.name){
      this.setState({
        name:nextProps.name
      });
    }
  }
  
  deleteData(){
    let {id} = this.state;
    this.props.deleteMine.bind(this)(id);
  }
  
  updateData(){
    this.setState({
      checkJudge: true
    });
  }
  
  saveData(){
    let {id} = this.state;
    let name = this.refs.inputText.value;
    this.setState({
      checkJudge:false
    });
    this.props.saveMine.bind(this)(id, name);
  }
  
  render(){
    let {checkJudge} = this.state;
    return (
      checkJudge ? <li className="list-group-item">
          <input className="add-person" type="text" defaultValue={name} ref="inputText" />
          <i className="glyphicon glyphicon-share share-person" onClick={this.saveData.bind(this)}>
          
          </i>
          <i className="glyphicon glyphicon-ban-circle share-person" onClick={this.deleteData.bind(this)}>
          
          </i>
      </li> : <li className="list-group-item">
          {name}
          <i className="glyphicon glyphicon-edit" onClick={this.updateData.bind(this)}>
          
          </i>
          <i className="glyphicon glyphicon-ban-circle" onClick={this.deleteData.bind(this)}>
          
          </i>
      </li>
    )
  }
}

class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      list: new Map(),
      key:0
    }
  }
  
  static get defaultProps(){
    return {
      
    }
  }
  
  delete(id){
    let {list} = this.state;
    list.delete(id);
    this.forceUpdate();
  }
  
  add(){
    let {list} = this.state;
    this.state.key = this.state.key + 1;
    list.set(this.state.key, {name: ""});
    this.forceUpdate();
  }
  
  save(id, name){
    let {list} = this.state;
    list.set(id, {name: name});
    this.forceUpdate();
  }
  
  render(){
    let {list} = this.state;
    let listDOM = [];
    for(let listItem of list){
      listDOM.push(<Item key={listItem[0]} id={listItem[0]} name={list[1].name} deleteMine={this.delete.bind(this)} saveMine={this.save.bind(this)}/>);
    }
    return (
      <div className="container">
        <button className="btn btn-default" onClick={this.add.bind(this)}>
          Add
        </button>
        <ul className="list-group">
          {listDOM}
        </ul>
      </div>
    )
  }
}
~~~
~~~css
.list-group {
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
<html>
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
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##React双向绑定
###React双向绑定Demo one
~~~javascript
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:""
    }
  }
  
  static get defaultProps(){
    return {
    
    }
  }
  
  changeHandler(event){
    this.setState({
      name:event.target.value
    });
  }
  
  render(){
    let {name} = this.state;
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group">
            <input className="form-control" type="text" value={name} onChange={this.changeHandler.bind(this)}/>
            {name}
          </div>
        </div>
      </div>
    )
  }
}
ReactDOM.render(<Comp />,document.getElementById("containerDiv"));
~~~
~~~html
<!DOCTYPE html>
<html>
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
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
###React双向绑定Demo two
~~~javascript
const linkedStateMixin = React.addons.LinkedStateMixin;
const Comp = React.createClass({
  displayName:"Comp",
  getInitialState(){
    return {
      name:""
    }
  },
  
  getDefaultProps(){
    return {
    
    }
  },
  
  mixins:[linkedStateMixin],
  
  render(){
    let {name} = this.state
    return (
      <div className="containerDiv">
        <div className="form-horizontal">
          <div className="form-group">
            <input type="text" className="form-control" valueLink={this.linkState('name')} />
            {name}
          </div>
        </div>
      </div>
    )
  }
});
ReactDOM.render(<Comp />,document.getElementById("containerDiv"))
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-with-addons.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
###React双向绑定Demo three
~~~javascript
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:""
    }
  }
  
  static get defaultProps(){
    return {
    
    }
  }
  
  render(){
    let {name} = this.state;
    const myLink = {
      value:name,
      requestChange:(newValue)=>{
        this.setState({
          name:newValue
        });
      }
    }
    return (
      <div className="container">
        <div className="form-horizontal">
          <div className="form-group">
            <input type="text" className="form-control" valueLink={myLink} />
            {name}
          </div>
        </div>
      </div>
    )
  }
}
ReactDOM.render(<Comp />,document.getElementById("containerDiv"));
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-with-addons.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
###React双向绑定Demo four
~~~javascript
class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      name:"",
      nameOne:"",
      nameTwo:""
    }
  }
  
  static get defaultProps(){
    return {
      
    }
  }
  
  linkState(name){
    return {
      value:this.state[name],
      requestChange:(newValue)=>{
        this.setState({
          [name]:newValue
        });
      }
    }
  }
  
  render(){
    let {name,nameOne,nameTwo} = this.state;
    <div className="containerDiv">
      <div className="form-horizontal">
        <div className="form-group">
          <input type="text" className="form-control" valueLink={this.linkState('name')}/>
          {name}
        </div>
        <div className="form-group">
          <input type="text" className="form-control" valueLink={this.linkState('nameOne')}/>
          {nameOne}
        </div>
        <div className="form-group">
          <input type="text" className="form-control" valueLink={this.linkState('nameTwo')}/>
          {nameTwo}
        </div>
      </div>
    </div>
  }
}
ReactDOM.render(<Comp />,document.getElementById("containerDiv"));
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-with-addons.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##React动画效果
###React动画效果Demo
~~~javascript
const ReactCSSTransitionGroup = React.addons.CSSTransitionGroup;
class Item extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      id:this.props.id,
      name:this.props.name,
      changeJudge:this.props.changeJudge
    }
  }
  
  static get defaultProps(){
    return {
      id:0,
      name:"",
      changeJudge:true
    }
  }
  
  saveData(){
    this.setState({
      changeJudge:true
    });
  }
  
  changeHandler(event){
    this.setState({
      name:event.target.value
    });
  }
  
  deleteData(){
    let {id} = this.state;
    this.props.deleteMine.bind(this)(id);
  }
  
  render(){
    let {changeJudge} = this.state;
    return (
      changeJudge ? <li className="list-group-item">
        {name}
      </li> : <li className="list-group-item">
        <input className="add-person" type="text" value={name} onChange={this.changeHandler.bind(this)} />
        <i className="glyphicon glyphicon-share share-person" onClick={this.saveData.bind(this)}>
        
        </i>
        <i className="glyphicon glyphicon-ban-circle share-person" onClick={this.deleteData.bind(this)}>
        
        </i>
      </li>
    )
  }
}

class Comp extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      list:[],
      key:0
    }
  }
  
  static getDefaultProps(){
    data:[]
  }
  
  componentWillMount(){
    let list = this.props.data((dataItem, dataIndex)=>{
      this.state.key = this.state.key + 1;
      this.setState({
        key:this.state.key
      });
      return {id:this.state.key, name:dataItem, actived:true};
    });
    this.setState({
      list
    });
  }
  
  add(){
    let {list} = this.state;
    this.state.key = this.state.key + 1;
    list.push({id:this.state.key, name:"", actived:false});
    this.forceUpdate();
  }
  
  deleted(id){
    let {list} = this.state;
    list.map((listItem, listIndex)=>{
      if(listItem.id === id){
        list.splice(list.indexOf(listItem), 1);
      }
    });
    this.forceUpdate();
  }
  
  render(){
    let {list} = this.state;
    let listDOM = list.map((listItem, listIndex)=>{
      return <Item id={listItem.id} name={listItem.name} changeJudge={listItem.actived} deleteMine={this.deleted.bind(this)} />;
    });
    return (
      <div className="container">
        <button className="btn btn-default" onClick={this.add.bind(this)}>Add</button>
        <ul className="list-group">
          <ReactCSSTransitionGroup transitionName="list" transitionEnterTimeout={1500} transitionLeaveTimeout={1500}>
            {listDOM}
          </ReactCSSTransitionGroup>
        </ul>
      </div>
    )
  }
}
const data = [
  "Clown Laugh At You",
  "Legend",
  "hello ReactJs"
];

ReactDOM.render(<Comp data={data} />,document.getElementById("containerDiv"));
~~~
~~~css
.list-group {
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

.list-enter{
  opacity:0.01;
  transition:opacity 1.5s ease-in-out;
}

.list-enter.list-enter-active{
  opacity:1
}

.list-leave{
  opacity:1;
  transition:opacity 1.5s ease-in-out;
}

.list-leave.list-leave-active{
  opacity:0.01;
}
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
    <script type="text/javascript" src="react.min.js"></script>
    <script type="text/javascript" src="react-with-addons.min.js"></script>
    <script type="text/javascript" src="react-dom.min.js"></script>
    <script type="text/javascript" src="browser.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/babel" src="reactTest.js"></script>
</body>
<html>
~~~
##配置React模块开发
~~~javascript
//将Comp,Item组件和主文件分成三个文件，Comp和Item分别以文件的形式放进component文件夹中
//Comp.js
const React = require("react");
const Item = require("./Item");
class Comp extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            list: new Map(),
            key: 0
        }
    }

    static get defaultProps() {
        return {}
    }

    add() {
        let {list}= this.state;
        this.state.key = this.state.key + 1;
        list.set(this.state.key, {name: ""});
        this.forceUpdate();
    }

    deleteData(id) {
        let {list} = this.state;
        list.delete(id);
        this.forceUpdate();
    }

    saveData(id, name) {
        let {list} = this.state;
        list.set(id, {name: name});
        this.forceUpdate();
    }

    render() {
        let {list} = this.state;
        let listDOM = [];
        for (let listItem of list) {
            listDOM.push(<Item key={listItem[0]} id={listItem[0]} name={listItem[1].name}
                               onDelete={this.deleteData.bind(this)} onSave={this.saveData.bind(this)}
                               changeStatus={true}/>);
        }
        return (
            <div className="container">
                <div className="form-horizontal">
                    <button className="btn btn-default" style={{marginTop: "4px"}} onClick={this.add.bind(this)}>Add
                    </button>
                    <ul className="list-group">
                        {listDOM}
                    </ul>
                </div>
            </div>
        )
    }
}
module.exports = Comp;
//Item.js
const React = require("react");
class Item extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            id: this.props.id,
            name: this.props.name,
            changeStatus: this.props.changeStatus
        }
    }

    static get defaultProps() {
        return {
            id: 0,
            name: "",
            changeStatus: true
        }
    }

    deleteMine() {
        let {id} = this.state;
        this.props.onDelete(id);
    }

    saveMine() {
        let {id} = this.state;
        let name = this.refs.inputText.value;
        this.setState({
            changeStatus: false
        });
        this.props.onSave(id, name);
    }

    updateMine() {
        this.setState({
            changeStatus: true
        });
    }

    componentWillReceiveProps(nextProps) {
        if (this.props.name !== nextProps.name) {
            this.setState({
                name: nextProps.name
            })
        }
    }

    changeHandler() {
        this.setState({
            name: event.target.value
        });
    }

    render() {
        const {name, changeStatus} = this.state;
        return (
            changeStatus ? <li className="list-group-item">
                {/*<input type="text" className="add-person" value={name} onChange={this.changeHandler.bind(this)}/>*/}
                <input type="text" className="add-person" defaultValue={name} ref="inputText" />
                <i className="glyphicon glyphicon-share share-person" onClick={this.saveMine.bind(this)}>

                </i>
                <i className="glyphicon glyphicon-ban-circle share-person" onClick={this.deleteMine.bind(this)}>

                </i>
            </li> : <li className="list-group-item form-clear">
                {name}
                <i className="glyphicon glyphicon-edit" onClick={this.updateMine.bind(this)}>

                </i>
                <i className="glyphicon glyphicon-ban-circle" onClick={this.deleteMine.bind(this)}>

                </i>
            </li>
        )
    }
}
module.exports = Item;
//主文件
const React = require("react");
const ReactDOM =require("react-dom");
const Comp = require("../component/Comp");
ReactDOM.render(<Comp />,document.getElementById("containerDiv"));
//然后执行如下命令
npm install browserify --save
npm install babelify --save
npm install --save-dev babel-preset-es2015 babel-preset-react
//在package.json的"scripts"对象中添加"start"属性
"start":"browserify ./react/scripts/indexSixteen.js > build.js -t [ babelify --presets [ es2015 react ] ]"
//最后执行如下命令
npm start
//就可在本地服务器运行，看到配置模块化之后的界面
~~~
~~~css
@charset "utf-8";
.list-group {
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
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/javascript" src="build.js"></script>
</body>
<html>
~~~
##React树 Tree Demo
~~~javascript
//先下载依赖包tree-node
npm install tree-node --save
//将Tree，TreeNode和主文件分为三个文件，Tree和TreeNode分别以文件的形式放进component文件夹中
//TreeNode.js
const React = require("react");
class TreeNode extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      open:true,
      className:""
    }
  }
  
  static get defaultProps(){
    return {
      
    }
  }
  
  opt(){
    let {open} = this.state;
    if(open){
      this.state.className = "gary-leave gary-leave-active";
      this.forceUpdate();
      setTimeout(()=>{
        this.setState({
          open:false
        });
      }, 200);
    }else{
      this.setState({
        open:true
      });
      setTimeout(()=>{
        this.setState({
          className:"gary-enter gary-enter-active"
        });
      }, 200);
    }
  }
  
  menu(event){
    if(event.button === 2){
      let {node} = this.props;
      let x = event.clientX;
      let y = event.clientY;
      this.props.show.bind(this)(x, y, node.id);
    }
  }
  
  render(){
    let listDOM = [];
    let {open} = this.state;
    let {node} = this.props;
    for(let nodeId of node.childIdsList){
      let childId = node.childs[nodeId];
      listDOM.push(<TreeNode id={childId.id} node={childId} show={this.props.show.bind(this)} />);
    }
    return (
      <li>
          <h4 onMouseDown={this.menu.bind(this)}>
            <a href="javascript:void(0);" onClick={this.opt.bind(this)}><i className={open ? "glyphicon glyphicon-minus" : "glyphicon glyphicon-plus"}>
                
            </i></a>{node.data.title}
          </h4>
        <ul className={className} style={{display: open ? "block" : "none"}}>
          {listDOM}
        </ul>
      </li>
    )
  }
}
//Tree.js
const React = require("react");
const TreeNode = require("./TreeNode");
const TNode = require("tree-node");
class Tree extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      treeData = new TNode(),
      showMenu:false,
      top:0,
      left:0,
      id:0
    }
  }
  
  static get defaultProps(){
    return {
      
    }
  }
  
  componentWillMount(){
    if(this.props.json){
      let {treeData} = this.state;
      let {json} = this.props;
      treeData.reborn(json);
    }
  }
  
  show(x, y, nodeId){
    let top = y,
        left = x;
    this.setState({
        top,
        left,
        showMenu:true,
        id:nodeId
    });
  }
  
  add(){
    let {treeData, id} = this.state;
    let newData = window.confirm("title");
    let newNode = new TNode;
    newNode.data("title", newData);
    treeData.getNode(id).appendChild(newNode);
    this.forceUpdate();
  }
  
  del(){
    let {treeData, id} = this.state;
    treeData.removeChild(id);
    this.closeMenu.bind(this)();
  }
  
  up(){
    let {treeData, id} = this.state;
    treeData.up(id);
    this.closeMenu.bind(this)();
  }
  
  down(){
    let {treeData, id} = this.state;
    treeData.down(id);
    this.closeMenu.bind(this)();
  }
  
  closeMenu(){
    this.setState({
      showMenu:false
    });
  }
  
  render(){
    let listDOM = [];
    let {treeData, showMenu, left, top} = this.state;
    for(let nodeId of treeData.childIds){
      let childId = treeData.getNode(nodeId);
      listDOM.push(<TreeNode key={childId.id} node={childId.json} show={this.show.bind(this)} />);
    }
    return (
      <div className="container" onContextMenu={(e) => {
        e.preventDefault();
      }}>
          <ul>
            {listDOM}
          </ul>
          <div onMouseLeave={this.closeMenu.bind(this)} className="showMenu" style={{display: showMenu ? "block" : "none", top: top, left: left}}>
            <ul className="list-group">
              <li className="list-group-item">
                <a href="javascript:void(0);" onClick={this.add.bind(this)}>添加</a>
              </li>
              <li className="list-group-item">
                <a href="javascript:void(0);" onClick={this.del.bind(this)}>删除</a>
              </li>
              <li className="list-group-item">
                <a href="javascript:void(0);" onClick={this.up.bind(this)}>上移</a>
              </li>
              <li className="list-group-item">
                <a href="javascript:void(0);" onClick={this.down.bind(this)}>下移</a>
              </li>
            </ul>
          </div>
      </div>
    )
  }
}
module.exports = Tree;
//主文件tree文件夹下面的index.js
const React = require("react");
const ReactDOM = require("react-dom");
const Tree = require("../component/Tree");
const TNode = require("tree-node");
const root = new TNode();
const nodeOne = new TNode;
nodeOne.data("title","Clown Laugh At You");
const nodeTwo = new TNode;
nodeTwo.data("title","Legend");
root.appendChild(nodeOne).appendChild(nodeTwo);
const nodeThree = new TNode;
nodeThree.data("title","hello reactJs");
const nodeFour = new TNode;
nodeFour.data("title","sunshine~");
nodeTwo.appendChild(nodeThree).appendChild(nodeFour);
ReactDOM.render(<Tree json={root.json} />, document.getElementById("containerDiv"));
~~~
~~~css
.showMenu{
  position:absolute;
}

.showMenu ul{
  padding:6px 18px;
  background-color:#4183c4;
}

.showMenu ul li a{
  color:#4183c4;
  display:block;
  text-decoration:none;
}

.gary-enter{
  opacity:0.01;
  transition:opacity .2s ease-in-out;
  -webkit-transition:opacity .2s ease-in-out;
  -o-transition:opacity .2s ease-in-out;
}

.gary-enter.gary-enter-active{
  opacity:1;
}

.gary-leave{
  opacity:1;
  transition:opacity .2s ease-in-out;
  -webkit-transition:opacity .2s ease-in-out;
  -o-transition:opacity .2s ease-in-out;
}

.gary-leave.gary-leave-active{
  opacity:0.01;
}
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
    <link rel="stylesheet" type="text/css" href="reactTest.css">
    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript" src="bootstrap.min.js"></script>
</head>
<body>
<div className="containerDiv">
</div>
<script type="text/javascript" src="tree.js"></script>
</body>
<html>
~~~
##Store demo
~~~javascript
//建立一个名为store_project的文件夹，然后执行如下命令
npm init
npm install babel-cli browserify babelify babel-preset-es2015 babel-preset-react --save-dev
npm install angularjs events bootstrap react react-dom jquery util fs express http --save
//在package.json的文件中在"scripts"底下建立如下属性和值
"compile":"babel --presets es2015,react component -d dist"
"browser":"browserify ./dist/index.js -o storeIndex.js -t [ babelify --presets [ es2015 react ] ]"
~~~
~~~javascript
//Store.js
let EventEmitter = require("events").EventEmitter;
class Store extends EventEmitter{
  constructor(){
    super();
    this._List = []
  }
  
  _add(storeItem){
    this._List.push(storeItem);
    return this._List;
  }
  
  get List(){
    return this._List;
  }
}
//List.js
const React = require("react");
const Store = require("./Store");
let store = new Store();
class List extends React.Component{
  constructor(props){
    super(props);
    this.state = {
      list:[],
      value:""
    }
  }
  
  static get defaultProps(){
    return {
      
    }
  }
  
  componentWillMount(){
    store.on("change",(list)=>{
      this.setState({
        list
      });
    });
  }
  
  doChangeValue(e){
    this.setState({
      value:e.target.value
    });
  }
  
  doChangeList(){
    let {value} = this.state;
    store.emit("change",store._add(value));
  }
  
  render(){
    let listDOM = [];
    let {list, value} = this.state;
    list.map((listItem, listIndex)=>{
      listDOM.push(<li key={listIndex} className="list-group-item">{listItem}</li>);
    });
    return (
      <div className="container">
        <ul className="list-group">
          {listDOM}
        </ul>
        <div className="form-group">
          <input value={value} className="form-control" style={{display:"inline-block", width:"90%"}} onChange={this.doChangeValue.bind(this)} />
          <button className="btn btn-info" onClick={this.doChangeList.bind(this)}>Add</button>
        </div>
      </div>
    )
  }
}
//index.js
const React = require("react");
const ReactDOM = require("react-dom");
const List = require("./List");
ReactDOM.render(<List />,document.getElementById("containerDiv"));
~~~
~~~javascript
//在命令行中执行如下命令
npm run compile
npm run browser
~~~
~~~html
<!DOCTYPE html>
<html>
<head>
  <link type="text/javascript" rel="stylesheet" href="bootstrap.min.css">
  <link type="text/javascript" rel="stylesheet" href="index.css">
</head>
<body>
  <div id="containerDiv">
  </div>
  <script type="text/javascript" src="storeIndex.js"></script>
</body>
</html>
~~~
#你不知道的JavaScript
##TYPES & GRAMMER
~~~javascript
//基本类型:string,boolean,number,undefined,null
//对象类型:object
var a = "42";
var b = 42;
var c = true;
var d = { name : "Yinwk" };
var e;
var f = null;
var h = function(){
};
var i = [2, 8, 10];
console.log(a);    //42      
console.log(b);    //42
console.log(c);    //true
console.log(d);    //{ name : "Yinwk" }
console.log(e);    //undefined
console.log(f);    //null
console.log(g);    //g is not defined
console.log(h);    //function(){}
console.log(i);    //[2, 8, 10]
console.log(typeof a);    //string
console.log(typeof b);    //number
console.log(typeof c);    //boolean
console.log(typeof d);    //object
console.log(typeof e);    //undefined
console.log(typeof f);    //object
console.log(typeof g);    //undefined
console.log(typeof h);    //function
console.log(typeof i);    //object
//识别声明的变量是否为null
if(!f && typeof f === "object"){
  console.log("f是一个null值");
}
//typeof规避错误
if(typeof barz === "undefined"){
  barz = function(){
  }
}
//IIFE typeof规避错误
(function(){
  function barz(){
  }
  
  function doSomethingCool(){
    var harz = (typeof barz !== "undefined") ? barz : function(){};
    harz();
  }
  
  doSomethingCool();
})();
//依赖注入 typeof规避错误
function barz(){
}
function doSomethingCool(barz){
  var harz = barz || function(){};
  harz();
}
doSomethingCool(barz);
//数组
var arr = ['100',true,[256]];
console.log(arr[0]);    //100(字符串)
console.log(arr[1]);    //true
console.log(arr[2][0]);    //256

var arr = [];
arr[0] = '144';
arr[1] = false;
arr[2] = [356];
console.log(arr.length);    //3
console.log(arr[0]);    //144
console.log(arr[1]);    //false
console.log(arr[2][0]);    //356

var arr = [];
arr[0] = '144';
arr[2] = [356];
console.log(arr.length);    //3
console.log(arr[1]);    //undefined,此undefined和arr[1] = undefined不同

var arr = [];
arr[0] = "Gary";
arr[2] = 125;
arr["foobar"] = "foobar";
console.log(arr.length);    //3
console.log(arr["foobar"]);    //foobar
console.log(arr.foobar);    //foobar

function doSomeThingCool(){
  var array = Array.prototype.slice.call(arguments);
  array.push("barm");
  console.log(array);
}
doSomeThingCool("barz","bary");    //[barz, bary, barm]
//字符串
//字符串和数组共有的方法有:concat,slice,indexOf,lastIndexOf,length
var string = "foo";
var array = ["f", "o", "o"];
console.log(string.length);    //3
console.log(array.length);    //3
string[1] = string[1].toUpperCase();
array[1] = array[1].toUpperCase();
console.log(string);    //foo
console.log(array);    //["f", "O", "o"]

//join
var string = "foo";
var array = ["f", "o", "o"];
console.log(array.join("-"));    //f-o-o
var stringAno = Array.prototype.map.call(string, function(stringArr, index){
  return stringArr.toUpperCase();
});
var stringResult = Array.prototype.join.call(stringAno, "-");
console.log(stringResult);    //F-O-O

//reverse
var string = "foo";
var array = ["f", "o", "o"];
console.log(array.reverse());    //["o", "o", "f"]
var stringAno = string.split("")
                      .reverse()
                      .join("");
console.log(stringAno);    //oof
//数字
var a = 42;
var b = 42.3;
var c = 42.0;
var d = 42.;
var e = 0.42;
var f = .42;
console.log(a + "," + b + "," + c + "," + d + "," + e + "," + f);    //42,42.3,42,42,0.42,0.42

var number = 5E10;
console.log(number);    //50000000000
console.log(number.toExponential());    //5e+10

var num = 23.1415926
console.log(num.toFixed(0));    //23
console.log(num.toFixed(1));    //23.1
console.log(num.toFixed(2));    //23.14
console.log(num.toFixed(3));    //23.142
console.log(num.toFixed(4));    //23.1416
console.log(num.toFixed(5));    //23.14159

var n = 23.1415926
console.log(num.toPrecision(2));    //23
console.log(num.toPrecision(3));    //23.1
console.log(num.toPrecision(4));    //23.14
console.log(num.toPrecision(5));    //23.142
console.log(num.toPrecision(6));    //23.1416
console.log(num.toPrecision(7));    //23.14159

console.log((23.1415926).toPrecision(5));    //23.142
console.log((42.0).toPrecision(2));    //42
console.log(.42.toPrecision(1));    //0.4
console.log(42.toPrecision(2));    //报错啦~Error~
console.log(42..toPrecision(2));    //42
console.log(42 .toPrecision(2));    //42
~~~
##Javascript运行方式
~~~javascript
1、语法分析，将代码以空格分隔开，找到关键字和声明方式
2、词法分析，有一个抽象词法书，在这里编译器会在作用域中声明函数和变量，并进行LHS和RHS的解析，LHS:赋值操作的目标是谁;RHS:谁是赋值操作的源头
3、代码生成并执行，引擎根据词法分析中所声明的位置对函数和变量进行赋值
~~~
##作用域
~~~javascript
var a = 2;是两个不同的声明:
1.var a;    //编译器先到作用域中查找是否存在声明a变量,如果不存在,进行声明a变量
2.a = 2;    //浏览器引擎再到作用域中查询是否存在a变量声明,如果存在,对a变量进行赋值2;如果不存在,继续查询下去

function foo(a){
  var b = a - 1;
  return a + b;
}
var c = foo(3);
//首先是foo函数的调用:RHS引用;接着将参数a进行赋值3:LHS引用;随后声明一个b变量,参数a - 1赋其值,其中赋值:LHS引用,参数a的引用:RHS引用;然后返回a + b之和,分别用了a的应用和b的引用:RHS引用;最后声明一个c变量,并把函数foo返回的值赋给它:LHS引用

//规避作用域
//两种方式:eval和with
function foo(words){
  eval(words);
  console.log(b);
}
var b = 2;
foo("var b = 3");    //3
//eval修改了词法作用域,本来b赋值为2的,被eval强行修改作用域,被赋值为3
function foo(obj){
  with(obj){
    a = 2;
  }  
}
var objOne = {
  a: 100
};
var objTwo = {
  b:255
};
foo(objOne);
console.log(objOne.a);    //2
foo(objTwo);
console.log(objTwo.a);    //undefined
console.log(a);    //2
//with建立了新的词法作用域,但是可能会泄露其中的属性给全局,并声明新变量
//根据Javascript的编译和执行的运行方式,eval和with会大大降低代码的运行效率,建议不要使用

//隐藏作用域、解决冲突和自动执行的函数表达式(IIFE)
function doCool(b){
  function doSomeThing(a){
     return a - 1;
  }
  
  var result = a + doSomeThing(b);
  return result * 3;
}
doCool(3);
//隐藏作用域代码,在控制台中打印:15
//在一个大的作用域气泡中,如果要使用同一个变量名的话,要进行重新声明

(function foo(){
  var a = 22;
  console.log(a);
})();
var a = 30;
console.log(a);
//在控制台中打印:
//22
//30

var a = 100;
(function doSomeThing(global){
  var a = 66;
  console.log(a);
  console.log(global.a);
})(window);
//在控制台中打印:
//66
//100

setTimeout(function timePicker(){
  console.log("lose my time~");
}, 1000);
//在控制台中隔一秒钟后打印:
//lose my time~

var a = 100;
(function define(def){
  def(window);
})(function def(global){
  var a = 66;
  console.log(a);
  console.log(global.a);
});
//在控制台中打印:
//66
//100

//块作用域
var foo = true;
if(foo){
  var bar = foo * 2;
  console.log(bar);
}
console.log(bar);
//Javascript中没有块作用域的概念,如果在块作用域中声明了变量,它会直接暴露在全局作用域或者块作用域外部的作用域中
//在控制台中显示:
//2
//2

//创建块作用域——with
var obj = {};
function foo(obj){
  with(obj){
    a = 100;
    b = 56;
  }
}
var a = 101;
foo(obj);
console.log(a);
//在控制台中显示:
//100

//ES3 try——catch作用域
try{
  console.log(blog);
} catch(err) {
  console.log(err);
}
console.log(err);
//在控制台中显示:
//以日志形式打印:Reference Error:blog is not defined
//以错误形式打印:Reference Error:err is not defined

//ES6 引入let,隐式劫持块作用域,但是let无法做到提升
var flag = true;
if(flag){
    {
       let bar = flag * 2;
       console.log(bar);
    }
}
console.log(bar);
//在控制台中显示:
//2
//Reference Error:bar is not defined

{
    for(let i = 0; i < 10; i++){
      {
          console.log(i);
      }
    }
    console.log(i);
}
//在控制台中显示:
//0
//1
//2
//3
//4
//5
//6
//7
//8
//9
//Reference Error:i is not defined

var foo = true, baz = 10;
if(foo){
  var bar = 3;
  if(bar > baz) {
    console.log("<>>");
  } else {
    console.log("<<>");
  }
}

//transfrom
var foo = true, baz = 10;
if(foo){
  var bar = 3;
}
if(bar > baz){
  console.log("<>>");
} else {
  console.log("<<>");
}
//两种形式在控制台中显示:
//<<>

//引入let
var foo = true, baz = 10;
if(foo){
  {
    let bar = 3;
    if(bar > baz){
      console.log("<>>");
    } else {
      console.log("<<>");
    }
  }
}
//在控制台中显示:
//<<>
//无法进行transform变换
var foo = true, baz = 10;
if(foo) {
  {
    let bar = 3;
  }
}

if(bar > baz) {
  console.log("<>>");
} else {
  console.log("<<>");
}
//在控制台中显示:
//Reference Error:bar is not defined

//经典闭包案例
{
  let arr = [];
  function foo(){
    let array = [];
    for(var i = 0; i < 10; i++){
      array.push(function listItem(){    //妈妈快看，这是闭包
        console.log(i);
      });
    }
    return array;
  }
  arr = foo();
  arr[3]();
  arr[7]();
  arr[8]();
}
//在控制台中显示:
//10
//10
//10

{
  let arr = [];
  function foo(){
    let array = [];
    for(var i = 0; i < 10; i++){
      array.push((function listItem(i){
        return function(){
          console.log(i);
        }
      })(i));
    }
    return array;
  }
  arr = foo();
  arr[3]();
  arr[7]();
  arr[8]();
}
//在控制台中显示:
//3
//7
//8

{
  let arr = [];
  function foo(){
    let array = [];
    for(let i = 0; i < 10; i++){
      array.push(function(){
        console.log(i);
      });
    }
    return array;
  }
  arr = foo();
  arr[3]();
  arr[7]();
  arr[9]();
}
//在控制台中显示:
//3
//7
//9

//提升
a = 2;
var a;
console.log(a);
//先有蛋(声明),再有鸡(赋值),词法作用域的作用
//相当于:
//var a;
//a = 2;
//console.log(a);
//在控制台中显示:
//2

console.log(a);
var a = 2;
//相当于:
//var a;
//console.log(a);
//a = 2;
//在控制台中显示:
//undefined

foo();
function foo(){
  console.log(a);
  var a = 2;
}
//相当于:
//function foo(){
// var a;
// console.log(a);
// a = 2;
//}
//foo();
//在控制台中显示:
//undefined

foo();
function foo(){
  console.log(1);
}
var foo;
foo = function(){
  console.log(2);
}
//相当于:
//function foo(){
//  console.log(1);
//}
//foo();
//foo = function(){
//  console.log(2);
//}
//在控制台中显示:
//1

foo();
function foo(){
  console.log(1);
}
var foo;
foo = function bar(){
  console.log(2);
};
function foo(){
  console.log(3);
}
//相当于:
//function foo(){
// console.log(1);
//}
//function foo(){
// console.log(3);
//}
//foo();
//foo = function(){
//  var bar = ...self...;
//  console.log(2);
//}
//在控制台中显示:
//3

foo();
var foo = function(){
  console.log("hello world");
}
//相当于:
//var foo;
//foo();
//foo = function(){
//  console.log("hello world");
//}
//在控制台中显示:
//TypeError

foo();
var flag = true;
if(flag) {
  function foo(){ console.log("a"); }
} else {
  function foo(){ console.log("b"); }
}
//在这里if的块作用域起不到作用,函数只遵循词法作用域
//在控制台中显示:
//b

//闭包
//其实质含义是指函数中包含着函数,其内函数进行传递或者返回,在其他作用域或者全局作用域中可以看到外函数释放之后的作用域,使得外函数的作用域放大
function foo(){
  var a = 100;
  function bar(){
    console.log(a);
  }
  bar();
}
foo();
//这可以看作闭包,但是实际上并不是闭包
//在控制台中显示:
//100

function foo(){
  var a = 245;
  function bar(){
    console.log(a);
  }
  return bar;
}
var baz = foo();
baz();
//这才是闭包
//在控制台中显示:
//245

function foo(){
  var a = 255;
  function bar(){
    console.log(a);
  }
  baz(bar);
}
function baz(fn){
  fn();
}
foo();
//在控制台中显示:
//255

var baz;
function foo(){
  var a = 265;
  function bar(){
    console.log(a);
  }
  baz = bar;
}
function result(fn){
  fn();
}
foo();
result(baz);
//在控制台中显示:
//265

//闭包随处可见,实际上就是回调函数
function warning(message){
  setTimeout(function timer(){
    console.log(message);
  }, 1000);
}
warning("warning message");
//在控制台中延迟一秒钟之后显示:
//warning message

function clickMe(name, selector){
  $(selector).click(function clickMine(evt){
    console.log("Click Button:" + name);
  });  
}
clickMe("Button One","#btnFirst");
clickMe("Button Two","#btnSecond");
//点击两个按钮,在控制台中显示:
//Button One
//Button Two

//循环闭包
function foo(){
  for(var i = 0; i <= 5; i++){
    setTimeout(function timer(){
      console.log(i);
    }, i*1000);
  }
}
foo();
//在控制台中6秒钟隔一秒一显示:
//6
//6
//6
//6
//6
//6

function foo(){
  for(var i = 0; i <= 5; i++){
    setTimeout((function timer(i){
      return function(){
        console.log(i);
      }
    })(i), i*1000);
  }
}
foo();
//在控制台中6秒钟隔一秒一显示:
//0
//1
//2
//3
//4
//5

function foo(){
  for(let i = 0; i <= 5; i++){
    setTimeout(function timer(){
      console.log(i);
    }, i*1000);
  }
}
foo();
//在控制台中6秒钟隔一秒一显示:
//0
//1
//2
//3
//4
//5

//模块
function coolMoudle(){
  var cool = "very cool";
  var coolArray = [44,38,56];
  function doCool(){
    console.log(cool);
  }
  function doCoolArray(){
    console.log(coolArray.join("_"));
  }
  return {
    doCool:doCool,
    doCoolArray:doCoolArray
  }
}
var foo = coolMoudle();
foo.doCool();
foo.doCoolArray();
//在控制台中显示:
//very cool
//44_38_56

var foo = (function coolMoudle(){
  var cool = "very cool";
  var coolArray = [44,34,56];
  function doCool(){
    console.log(cool);
  }
  function doCoolArray(){
    console.log(coolArray.join("!"));
  }
  return {
    doCool:doCool,
    doCoolArray:doCoolArray
  }
})();
foo.doCool();
foo.doCoolArray();
//在控制台中显示:
//very cool
//44_34_56

function coolMoudle(id){
  function identify(){
    console.log(id.toUpperCase());
  }
  return {
    identify:identify
  }
}
var moudleOne = coolMoudle("gary");
var moudleTwo = coolMoudle("simon");
moudleOne.identify();
moudleTwo.identify();
//在控制台中显示:
//GARY
//SIMON

function coolMoudle(){
  var cool = "very cool";
  var physical = {
    change:change,
    doCool:doCool
  };
  function doCool(){
    console.log(cool);
  }
  function change(){
    physical.doCool = doCoolAno;
  }
  function doCoolAno(){
    console.log(cool.toUpperCase());
  }
  return physical;
}
var foo = coolMoudle();
foo.doCool();
foo.change();
foo.doCool();
//在控制台中显示:
//very cool
//VERY COOL

//现代模块
var moudleCool = (function coolMoudle(){
  var moudle = {};
  function define(name, defs, imps){
    for(var i = 0; i < defs.length; i++){
      defs[i] = moudle[defs[i]];
    }
    moudle[name] = imps.apply(imps, defs);
  }
})();
moudleCool.define("bar", [], function moudleOne(){
  function hello(name){
    return "Commit changes:" + name;
  }
  return {
    hello:hello
  }
});
moudleCool.define("foo", ["bar"], function moudleTwo(bar){
  var hungry = "hippo";
  function awesome(){
    console.log(bar.hello(hungry.toUpperCase()));
  }
  return {
    awesome:awesome
  }
});
var bar = moudleCool.get("bar");
var foo = moudleCool.get("foo");
console.log(bar.hello("gary"));
foo.awesome();
//在控制台中显示:
//Commit changes:gary
//Commit changes:HIPPO

//未来模块
//bar.js
function hello(name){
  return "Commit changes:" + name;
}
export hello;
//foo.js
import hello from "bar";
function awesome(){
  var hungry = "hippo";
  console.log(hello(hungry.toUpperCase()));
}
export awesome;
//scripts.js
module bar from "bar";
module foo from "foo";
console.log(bar.hello("gary"));
foo.awesome();
//在控制台中显示:
//Commit changes:gary
//Commit changes:HIPPO

//动态作用域
//Javascript中并不支持动态作用域,但是this的原理和动态作用域互通
//词法作用域是在编写代码的时候,编译器就确定了的,也就是在声明和定义的时候生成的
//动态作用域则是在引擎执行代码的时候形成的,只在乎调用时候的情形,而不在意声明和定义
fucntion foo(){
  console.log(a);
}
function bar(){
  var a = 3;
  foo();
}
var a = 102;
bar();
//在控制台中显示:
//102

//块级作用域的替代方案
{
  let a = 249;
  console.log(a);
}
console.log(a);
//如果设想一下,ES6代码要在浏览器上运行,要转码成的形式:
try{
  throw 2;
} catch(a) {
  console.log(a);
}
console.log(a);
//在控制台中显示:
//249
//Reference Error:a is not defined
//ES6想要在浏览器上面运行现阶段还需要转码器
//谷歌公司开发的Traceur还有Babel
//转码成的形式:
{
  try{
    throw undefined;
  } catch(a) {
    a = 2;
    console.log(a);
  }
}
console.log(a);
//在控制台中显示:
//2
//Reference Error:a is not defined

//this
var bar = {
  name: "awesome",
  cool: function(){
    setTimeout(function timer(){
      console.log(this.name);
    }, 1000);
  }
};
var name = "not awesome";
bar.cool();
//在控制台中显示:
//not awesome

var bar = {
  name: "awesome",
  cool: function coolMoudle(){
    var self = this;
    setTimeout(function timer(){
      console.log(self.name);
    }, 1000);
  }
}
var name = "not awesome";
bar.cool();
//在控制台中隔1秒钟后显示:
//awesome

var bar = {
  name:"awesome",
  cool:function coolMoudle(){
    setTimeout(() => {
      console.log(this.awesome);
    }, 1000);
  }
}
var name = "not awesome";
bar.cool();
//ES6中的胖箭头会继承自己所在的作用域的this,所以此处的this指向的是cool方法
//在控制台中隔1秒钟后显示:
//awesome

var bar = {
  name:"awesome",
  cool:function coolMoudle(){
    setTimeout(function timer(){
      console.log(this.name);
    }.bind(this), 1000);
  }
}
var name = "not awesome";
bar.cool();
//在控制台中隔1秒钟后显示:
//awesome

//认识this
function bar(){
  console.log("name:" + this.name + ",age" + this.age);
}
function foo(){
  console.log("first name:" + this.firstName.toUpperCase() + ",last name:" + this.lastName.toUpperCase());
}
var barObj = {
  name:"Gary",
  age:23
}
var fooObj = {
  firstName:"Yin",
  lastName:"Gary"
}
bar.call(barObj);
foo.call(fooObj);
//在控制台中显示:
//name:Gary,age:23
//first name:YIN,last name:GARY

//this并不指向自身
function foo(i){
  console.log(i);
  this.count++;
}
foo.count = 0;
for(var i = 0; i <= 10; i++){
  if(i > 5){
    foo(i);
  }
}
console.log(foo.count);
//在控制台中显示:
//6
//7
//8
//9
//10
//0

//规避this用法是逃避的体现
function foo(i){
  console.log(i);
  data.count++;
}
var data = {
  count: 0
};
for(var i = 0; i <= 10; i++){
  if(i > 5){
    foo(i);
  }
}
console.log(data.count);
//在控制台中显示:
//6
//7
//8
//9
//10
//5

//正确的this用法
function foo(i){
  console.log(i);
  this.count++;
}
var data = {
  count: 0
};
for(var i = 0; i <= 10; i++){
  if(i > 5){
    foo.call(data, i);
  }
}
console.log(data.count);
//在控制台中显示:
//6
//7
//8
//9
//10
//5

//当然也可以不使用data对象
function foo(i){
  console.log(i);
  this.count++;
}
foo.count = 0;
for(var i = 0; i< = 10; i++){
  if(i > 5){
    foo.call(foo, i);
  }
}
console.log(foo.count);
//在控制台中显示:
//6
//7
//8
//9
//10
//5

//this也不指向作用域
function foo(){
  var a = "Hello World";
  this.bar();
}
function bar(){
  console.log(this.a);
}
foo();
//在控制台中显示:
//Hello World
//this跟函数的定义和声明是没有任何关系的,只跟函数的调用有关
//函数在哪儿调用、函数的调用方式以及传递的参数这才和this紧密相连

//this全面解析
//this调用栈
function baz(){
  console.log("baz");
  bar();
}
function bar(){
  console.log("bar");
  foo();
}
function foo(){
  console.log("foo");
}
baz();
//在控制台中显示:
//baz
//bar
//foo

//默认绑定
function foo(){
  console.log(this.name);
}
var name = "Hello World";
foo();
//在控制台中显示:
//Hello World
function foo(){
  "use strict";
  console.log(this.name);
}
var name = "Hello World";
foo();
//在控制台中显示:
//Referenct Error:a is not defined
function foo(){
  console.log(this.name);
}
var name = "Hello World";
(function zone(){
  "use strict";
  foo();
})();
//在控制台中显示:
//Hello World

//隐式绑定
function foo(){
  console.log(this.a);
}
var obj = {
  a: 1004,
  foo:foo
};
obj.foo();
//在控制台中显示:
//1004
function foo(){
  console.log(this.name);
}
var obj = {
  name:"Gary",
  foo:foo
};
var name = "Oops,global";
var baz = obj.foo();
baz();
//在控制台中显示:
//Oops,global
function foo(){
  console.log(this.name);
}
var obj = {
  name: "Gary",
  foo: foo
};
var objOne = {
  name:"Simon",
  obj:obj
};
objOne.obj.foo();
//在控制台中显示:
//Gary
function foo(){
  console.log(this.name);
}
var obj = {
  name:"Gary",
  foo:foo
};
var objOne = {
  name:"Simon",
  obj:obj
};
objOne.obj.foo();
//在控制台中显示:
//Simon
function foo(){
  console.log(this.name);
}
var obj = {
  name:"Gary",
  foo:foo
};
function define(fn){
  fn();
}
var name = "Oops,global";
define(obj.foo);
//在控制台中显示:
//Oops,global
function foo(){
  console.log(this.name);
}
var obj = {
  name:"Gary",
  foo:foo
};
var name = "Oops,global";
setTimeout(obj.foo, 1000);
//在控制台中隔一秒后显示:
//Oops,global
//相当于:
//function setTimeout(fn, timeout){
//  fn();
//}
function foo(){
  console.log(this.name);
}
var obj = {
  name:"Gary",
  foo:foo
};
var objOne = {
  name:"Simon",
  obj:obj
};
objOne.obj.foo();
//在控制台中显示:
//Gary

//显式绑定
function foo(){
  console.log(this.a);
}
var obj = {
  a: "clown laugh at you~"
};
foo.apply(obj);
//在控制台中显示:
//clown laugh at you~
function foo(num){
  console.log(this.a, num);
  return this.a + num;
}
var obj = {
  a: 2
};
function baz(){
  return foo.apply(obj, arguments);
}
var bar = baz(3);
console.log(bar);
//在控制台中显示:
//2 3
//5
function foo(num){
  console.log(this.a, num);
  return this.a + num;
}
var obj = {
  a: 2
};
function bind(func, obj){
  return function result(){
    return func.apply(obj, arguments);  
  };
}
var bar = bind(foo, obj);
var baz = bar(3);
console.log(baz);
//在控制台中显示:
//2 3
//5
function foo(num){
  console.log(this.a, num);
  return this.a + num;
}
var obj = {
  a: 2
};
var bar = foo.bind(obj);
var baz = bar(3);
console.log(baz);
//在控制台中显示:
//2 3
//5

//new绑定
function Foo(a){
  this.a = a;
}
var bar = new Foo(2);
console.log(bar.a);
//在控制台中显示:
//2
//new绑定:
//创建一个新对象
//将新对象绑定到函数调用的this上面

分为全局作用域、函数作用域和块作用域
在es6出现之前，是不存在块作用域的
var judge = true;
if(judge){
  var name = "CLAY"; 
}
console.log(name);
//在控制台中打印出"CLAY"
{
  var name = "CLAY";
}
console.log(name);
//在控制台中打印出"CLAY"
for(var i = 0; i < 5; i++){
  console.log(i);
}
console.log(i);
//在控制台中打印出:
//0
//1
//2
//3
//4
//5
var arr;
(function(){
  arr = [];
  arr.push(1);
  arr.push(2);
  arr.push(5);
})();
console.log(arr);
//在控制台中打印出:
//[1, 2, 5]
function foo(){
  console.log(a);
  a = 2;
}
foo();
//在控制台中打印出:
//undefined
function foo(){
  a = 2;
  var a;
  console.log(a);
}
foo();
//在控制台中打印出:
//2
在es6出现之后，引入了let，出现块作用域
{
  let name = "Clown";
}
console.log(name);
//在控制台中报出错误:
//ReferenceError:name is not defined
for(let j = 0; j < 5; j++){
  console.log(j);
}
console.log(j);
//在控制台中打印出并报出错误:
//0
//1
//2
//3
//4
//ReferenceError:j is not defined
let arr;
{
    arr = [];
    arr.push(1);
    arr.push(2);
    arr.push(5);
}
console.log(arr);
//在控制台中打印出:
//1
//2
//5
function foo(){
  console.log(a);
  let a = 2;
}
//在控制台中报出错误:
//ReferenceError
function foo(){
  a = 2;
  {
    let a;
    console.log(a);
  }
}
//在控制台中打印出:
//undefined
function foo(){
  a = 2;
  {
    let a;
  }
  console.log(a);
}
//在控制台中打印出:
//2
~~~
##闭包
~~~javascript
任何有回调函数的函数都是闭包，A函数包裹B函数，并返回B函数，B函数中可以对A函数中的变量进行使用，使得B函数访问的作用域扩大，这就是闭包
function A(){
  var name = "Gary";
  function B(){
    console.log(name);
  }
  return B;
}
A()();
//在控制台中打印出:
//Gary
var arr = [];
function foo(){
  for(var i = 0; i < 5; i++){
    arr.push(function(){
      console.log(i);
    });
  }
}
foo();
arr[0]();
arr[1]();
arr[4]();
//在控制台中打印出:
//5
//5
//5
var arr = [];
function foo(){
  for(var i = 0; i < 5; i++){
    arr.push((function(i){
      return function(){
        console.log(i);
      }
    })(i));
  }
}
foo();
arr[0]();
arr[1]();
arr[4]();
//在控制台中打印出:
//0
//1
//4
{
  let arr = [];
  function foo(){
    for(let i = 0; i < 5; i++){
        arr.push(function(){
          console.log(i);
        });
    }
  }
  foo();
  arr[0]();
  arr[1]();
  arr[4]();
}
//利用块作用域和闭包的结合完美解决
//在控制台中打印出:
//0
//1
//4
~~~
##模块
###旧时代
~~~javascript
function Modules(){
  var name = "Gary";
  var physical = {
    description,
    change
  }
  function description(){
    console.log("Introduce myself:" + name);
  }
  
  function change(){
    physical.description = descriptionAno;
  }
  
  function descriptionAno(){
    console.log(("Introduce myself:" + name).toUpperCase());
  }
  return physical;
}

var modules = Modules();
modules.description();
modules.change();
modules.description();
//在控制台中打印出:
//Introduce myself:Gary
//INTRODUCE MYSELF:GARY
~~~
###现代模块
~~~javascript
function Modules(){
  var modules = {};
  function define(name, dels, lmp){
    for(var i = 0; i < dels.length; i++){
      dels[i] = modules[dels[i]];
    }
    modules[name] = lmp.apply(lmp, dels);
  }
  function get(name){
    return modules[name];
  }
  return {
    define:define,
    get:get
  }
}

var modulesAno = Modules();
modulesAno.define("bar", [], function(){
  function hello(who){
    return "introduce myself:" + who;
  }
  return {
    hello
  }
});
modulesAno.define("foo", ["bar"], function(bar){
  function awsome(who){
    console.log(bar.hello(who).toUpperCase());
  }
  return {
    awsome
  }
});
var bar = modulesAno.get("bar");
var foo = modulesAno.get("foo");
console.log(bar.hello("hippo"));
foo.awsome("hippo");
//在控制台中打印出:
//introduce myself:hippo
//INTRODUCE MYSELF:HIPPO
~~~
###在未来
~~~javascript
//bar.js
function hello(who){
  return "introduce myself:" + who;
}
export hello;
//foo.js
import hello from 'bar';
function awsome(who){
  console.log(hello(who).toUpperCase());
}
export awsome;
//main.js
module bar from "bar";
module foo from "foo";
console.log(bar.hello("hippo"));
foo.awsome("hippo");
//在控制台中打印出:
//introduce myself:hippo
//INTRODUCE MYSELF:HIPPO
~~~
#数据结构
##数据结构定义
~~~javascript
相互之间存在一种或多种特定关系的数据元素的集合
~~~
##数据对象
~~~javascript
具有相同特定性质的数据元素的集合
~~~
##数据结构分类
~~~javascript
分为逻辑结构和物理结构
~~~
###逻辑结构分类
~~~javascript
分为集合结构，线性结构，树形结构和图形结构
~~~
###物理结构分类
~~~javascript
分为顺序存储结构和链式存储结构
~~~
##数据顺序
~~~javascript
数据-->数据对象-->数据元素-->数据项
~~~
##数据结构-队列
###特点
~~~javascript
先进先出(FIFO)
~~~
###分类
~~~
普通队列和环形队列
~~~
####普通队列
~~~javascript
存在队头和队尾，当队列中存在一个元素时，这个元素既是对头，也是队尾。
普通队列两种形式:
1.队列中的内存不断被CPU处理，其中的队列内存元素往前移动，等待CPU处理。
优点:不会造成资源浪费，内存不会空缺
缺点:队列内存元素不断往前移动，CPU处理效率低
2.队列内存元素不移动，CPU移动从队头到队尾依次进行处理
优点:CPU移动，CPU处理效率高
缺点:CPU处理后的队列内存元素会空缺，造成资源浪费
~~~
#算法
##算法定义
~~~javascript
针对某种或者某类问题，将指令转化为操作序列，操作序列中含有多组操作，每个组里面的操作针对某个特定的功能，这就是算法
~~~
##算法特性
~~~javascript
1.输入
2.输出
3.有穷性
4.确定性
5.可行性
~~~
##好算法特性
~~~javascript
1.正确性
2.可读性
3.健壮性
4.高效率
5.低存储含量
~~~
##算法效率的度量方法
~~~
1.事后统计估计(不科学，不正确)
2.事前统计估计
~~~
##大O阶
~~~javascript
1.用常数1取代运行时间中所有加法常数
2.在修改后的运行次数函数，只保留最高阶项
3.如果最高阶项存在且不是1，则去除与这个项相乘的常数
必须自己估计
1.算法最坏时间复杂度
2.算法平均时间复杂度
~~~
###大O阶算法时间复杂度从简略到复杂排序
~~~javascript
O(1) < O(logn) < O(n) < O(nlogn) < O(n的2次方) < O(n的3次方) < O(2的n次方) < O(n!) < O(n的n次方)
~~~
#网络基础
##OSI七层模型
~~~javascript
1.物理层，最底层，包括对双绞线(传输距离最短，适用于家庭，最高限度100米)，多模光纤(传输距离较短)，单模光纤(传输距离较长)，RJ45接口(水晶头)的研究
2.数据链路层，主要包括对MAC地址和交换机的研究
3.网络层，主要包括对IP编址和路由功能(即路由器)的研究
4.传输层，主要包括对TCP、UDP协议传输的研究
5.会话层，主要针对会话与会话之间的联系区分表示的研究
6.表示层，对声音、图像、视频等多媒体媒介的传输的研究
7.应用层，就是对现在界面上的软件、网站和App的研究
数据进行传递到传输层，叫做段;传输到网络层，叫做包;传输到数据链路层，叫做帧;传输到物理层，叫做比特流
~~~
##物理层
###双绞线
~~~javascript
RJ45接口，又叫做水晶头
双绞线分为568A和568B绕线方式
568B绕线方式:橙白，橙，绿白，蓝，蓝白，绿，棕白，棕。一般国内采用这种绕线的方式居多
568A绕线方式:将568B绕线的1,3和2,6进行替换。也就是绿白，绿，橙白，蓝，蓝白，橙，棕白，棕
连接时:相同类型设备用交叉线相连，不同类型设备用平行线相连
比如交换机和电脑之间用平行线相连，交换机和交换机之间用交叉线相连
注意:hub不属于任何一类设备，交换机和hub相当于相同类型设备，用交叉线相连
~~~
##数据链路层
###以太网
~~~javascript
数据链路层的分类:交换机、无线网卡以及无线网.
交换机里面用的协议是:Ethernet，也就是以太网技术，速度已经实现家居1000Mbps级别电缆，而电缆类型被命名为802.3a...
在实验室中已经实现电缆类型被命名为802.3ae，也就是10Gbps.
一条以太网电缆上会链接多个主机，或者一个交换机上面会链接多台电脑，为了进行识别，每台电脑和主机都有一个本地唯一(之前是全球唯一)的物理地址，也就是MAC地址.
~~~
###MAC地址
~~~javascript
MAC地址一共有48位，前24位名叫OUI，后24位名叫Vendor Assign
OUI是每个生产此电子产品的厂商的标识，比如Intel，HUAWEI，DELL等等厂商标识;
而Vendor Assign是此类电子产品的类型的标识;
OUI和Vendor Assign共同组成了MAC地址，MAC地址最初是全球唯一的，后来因为电子产品过多48位16进制数根本表示不过来，所以改变为本地唯一
~~~
###无线网WLAN
~~~javascript
无线网WLAN类型分为多种:802.11a,802.11b,802.11g,802.11n
无线网WLAM速度:
802.11a，802.11g:54Mbps
802.11b:11Mbps
802.11n:78Mbps,150Mbps,300Mbps,500Mbps
实验室里面的无线网WLAN类型为802.11n的速度已经达到700Mbps,800Mbps
~~~
###冲突域
~~~javascript
以太网电缆解决冲突:被动监听(CSMA/CD)
无线WLAN解决冲突:主动避免(CSMA/CA)
以太网电缆解决冲突一般会先检查一下我的这条电缆上或者交换机上是否有信息发出或者信息收入，如果没有就进行发送信息，如果有就进行等待，等待以太网电缆上或者交换机上没有信息发出或者信息收入的时候，再进行发送信息，也就是所谓的被动监听(CSMA/CD detect)
无线网WLAN解决冲突一般会主动的去避免冲突的发生，不让多方发送或者收入信息时发生冲突，也就是所谓的主动避免(CSMA/CA avoid)
~~~
###HTTP请求过程
~~~javascript
1.先寻找Chrome浏览器自身的DNS缓存
2.如果Chrome浏览器自身不存在DNS缓存或者DNS缓存过期,则去寻找操作系统自身的DNS缓存
3.如果操作系统自身不存在DNS缓存或者DNS缓存过期,则去寻找本地HOST文件
4.如果本地HOST文件也不存在,浏览器会发送给运营商服务器一个解析域名的DNS请求
5.经过DNS请求之后,会进行TCP/IP链接,并进行三次握手
6.TCP/IP链接成功,则会向服务器发送一个HTTP请求,协议为http 1.0/1.1
7.服务器接受到请求头和参数之后,根据请求头和参数返回响应头和主体响应信息
8.浏览器根据响应头和主体响应信息,作出html、css、js和图片渲染或者异常处理
~~~
###获取元素的固定位置
~~~javascript
let absoluteTop = this.refs["mainInformation"].getBoundingClientRect().top + this.refs["mainInformation"].scrollTop;
console.log(absoluteTop);
~~~
###获取元素的高度
~~~javascript
let titleHeight = this.refs["mainInformationTitle"].clientHeight();
let contentHeight = this.refs["mainInformationContent"].clientHeight();
let totalHeight = titleHeight + contentHeight;
console.log(totalHeight);
~~~
###获取元素的样式表
~~~javascript
let marginTop = window.getComputedStyle(this.refs["mainInformation"]) ? window.getComputedStyle(this.refs["mainInformation"]).marginTop ? this.refs["mainInformation"].currentStyle;
console.log(parseInt(marginTop.slice(0, -2)));
~~~
###linux安装nginx
~~~javascript
先检验一下是否安装有openssl,pcre和lizb
用rpm -qa | grep "openssl"
rpm -qa | grep "pcre"
rpm -qa | grep "lizb"
查找openssl,pcre和lizb所在目录
rpm -ql openssl
rpm -ql lizb
rpm -ql pcre
去查找是否安装
对于安装nginx来说,这三项软件是必须的
然后下载nginx安装包
wget https://nginx.org/download/nginx-1.12.2.tar.gz
接着进行压缩,复制到指定路径,再将原文件删除
tar -zxvf nginx-1.12.2.tar.gz
cp nginx-1.12.2 nginxTarGz
rm -rf nginx-1.12.2
随后进行安装
进入nginxTarGz目录底下的nginx-1.12.2目录下
--prefix nginx安装的路径
--with-pcre指向的是pcre-8.23.0的源文件目录
--with-lizb指向的是lizb-1.2.7的源文件目录
--with-openssl指向的是openssl的源文件目录
执行./configure --prefix=/root/nginx-1.12.2 --with-pcre=/source/pcre/pcre-8.23.0 --with-lizb=/source/lizb/lizb-1.2.7 --with-openssl=/source/openssl/openssl-1.0.2k
最后执行make && make install进行安装
启动nginx
/root/nginx-1.12.2/sbin/nginx
~~~
