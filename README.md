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
  <section></section>:表示网页模块部分标签
  <aside></aside>:表示网页边栏部分标签
  <article></article>:表示网页内容文章部分标签
  <nav></nav>:表示导航栏部分标签
  <figure></figure>:表示承载图片部分标签
  <figcaption></figcaption>:表示对图片进行注解部分标签,在figure标签中
  <hgroup></hgroup>:表示承载标题部分标签
  <footer></footer>:表示网页结尾部分标签
  <ul></ul>:表示无序列表标签
  <ol></ol>:表示有序列表标签
  <li></li>:表示有序和无序列表子标签
  <abbr></abbr>:表示对文字缩写与简称的描述
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
~~~
  contentEditable:表示标签可编辑
  designModel:表示页面可编辑
  hidden:表示属性隐藏
  spellcheck:表示检查单词是否正确
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
  
~~~
#JavaScript
##方法
~~~Javascript
  Array数组的方法:
~~~
