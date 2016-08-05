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
  <rp></rp>:表示特殊字符的父级,比如难写的中文字,要进行标注拼音,这就表示的是中文字部分
  <rt></rt>:表示特殊字符的子级,如上,表示的时标注拼音部分
  <pre></pre>:表示内容会按照原来有换行和空格形式显示，适合写入程序
  <p></p>:段落标签
  <blockquote></blockquote>:段落模块儿标签
##属性
~~~
  contentEditable:表示标签可编辑
  designModel:表示页面可编辑
  hidden:表示属性隐藏
  spellcheck:表示检查单词是否正确
~~~
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
