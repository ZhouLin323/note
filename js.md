js
===
1.js类型
js5种基本类型： string,boolean,number,null,undefined
js7种数据类型：string,boolean,number,null,undefined,array,object
typeof6种返回格式：'string','number','object','function','boolean','undefined'

2. 获取数组中最大值或最小值的方法：
最大值：Math.min.apply(null,arr);
最小值：Math.min(...[v1,v2……])

3.this:
this的值要等到代码真正执行时才能确定
this的值具体有以下几种情况：
(1)new调用时指的是被构造的对象
(2)call,apply调用，指向我们指定的对象
(3)对象调用，如执行obj.b()，this指向obj
(4)默认的，指向全局变量window（相当于执行window.fun()）

4.Boolean返回值：
Boolean（[]） //true
Boolean(undefined) //false
boolean(null) //false
boolean(0) //false
boolean(NaN) //false
boolean(' ') //false

5.Number转化为0：
Number()
Number(0)
Number(' ')
Number('0')
Number(false)
Number(null)
Number([])
Number([0])

6.form表单的enctype属性：规定在发送到服务器之前应如何对表单数据进行编码
属性值：
application/x-www-form-urlencoded----在发送前编码所有字符（默认）
multlpart/form-data----不对字符编码（注：在使用包含文件上传控件的表单时，必须使用该值）
text/plain----空格转换为“+”加号，但不对特殊字符编码

7.设置弹出层居中： 
设置： position:absolute;
left: 50%;
top: 50%;
transform: translate(-50%, -50%);

8.外边距塌陷解决方法：
a:给父盒子设置border值
b:给父盒子设置overflow:hidden; 

9. 深入理解BFC和margin collapse
BFC(block formatting contexts)：浮动元素和绝对定位元素，非块级盒子的块级容器 ，以及overflow值不为“visiable”的块级盒子，都会为他们的内容创建新的BFC（块级格式上下文）
在BFC中，盒子从顶端开始垂直地一个一个排列，两个盒子之间的垂直地间隙是由他们的margin值所决定的。在一个BFC中，两个相邻的块级盒子的垂直外边距会产生折叠。
BFC的通俗理解：是一个独立的布局环境，BFC中的元素的布局不受外界影响并且在一个BFC中块盒与行盒都会垂直地沿着其父元素的边框排列。
合并外边距与BFC：
*折叠结果：
两个相邻的外边距都是正数时，折叠结果是他们两者之间较大的值。
两个相邻的外边距都是负数时，折叠结果是两者绝对值的较大值。
两个外边距一正一负时，折叠结果是两者的相加的和。
*产生折叠的必要条件：margin必须是邻接的。
两个margin是邻接的必须满足以下条件：
(1)必须是处于常规文档流的块级盒子并处于同一个BFC当中。
(2)没有线盒，没有空隙，没有padding和border将他们分隔开。
(3)都属于垂直方向上相邻的外边距，可以是下面任意一种情况
(4)元素的margin-top与其第一个常规文档流的子元素的margin-top
(5)元素的margin-bottom与其下一个常规文档流的兄弟元素的margin-top
(6)height为auto的元素的margin-bottom与其最后一个常规文档流的子元素的margin-bottom
(7)高度为0并且最小高度也为0，不包含常规文档流的子元素，并且自身没有建立新的BFC元素的margin-top和margin-bottom

10.iframe适用以下的场景：
(1)典型系统结构，左侧是功能树，右侧是一些常见的表单之类的
(2)ajax上传文件
(3)加载别的网站内容，如Google广告，网站流量分析
(4)在上传图片时，不用flash实现刷新
(5)跨域访问时可用iframe

11.html5新增标签：
article:标签定义外部的内容
aside:标签定义article以外的内容
audio：h5新增音频标签，没有宽高属性
canvas：h5新增画布标签
command：定义命令按钮
datalist：标签定义选项列表
details：用于描述文档或文档某个部分的细节
figure：用于对元素进行组合
figcaption:定义figure元素的标题
footer:定义section或document的页脚
header:定义section或document的页眉
hgroup:用于对网页或区段的标题进行组合
keygen：用于表单的密钥对生成器字段
mark：标签定义带有记号的文本
meter：通过min="0",max="20"的方式定义度量衡，仅用于已知最大和最小值得度量
nav：定义document或section或article的导航
output：定义不同的输出类型
progress：定义任何类型的任务的进度
rp:定义若浏览器不支持ruby元素显示的内容
rt:定义ruby的注释
section：标签定义文档中的节、区段
source:audio和video的属性之一
summary：为details定义标签
time：定义日期或时间
video：h5新增视频标签，具有宽高属性

12.css中可继承和不可继承的属性：
（一）无继承性的属性
1、display
2、文本属性：vertical-align,text-decoration,text-shadow,white-space,unicode-bidi
3、盒子模型的属性：width,height,margin,border,padding
4、背景属性：background一系列
5、定位属性：float,clear,position,top,right,bottom,left,overflow,clip,z-index
6、生成内容属性：content，counter-reset，counter-incrememt
7、轮廓样式属性：outline-style，outline-width，outline-color，outline
8、页面样式属性：size,page-break-before,page-break-after
9、声音样式属性：pause-before，pause-after，pause，cue-before，cue-after，cue，play-during
（二）有继承性的属性
1、字体系列属性：font系列，
font-variant：设置所有小写字母转换为大写
font-stretch：对当前的font-family进行伸缩变形，所有主流浏览器都不支持
font-size-adjust：为某个元素规定一个aspect值
2、文本系列属性：text-indent，text-align，line-height，word-spacing，letter-spacing，text-transform，direction，color
3、元素可见性：visibility
4、表格布局属性：caption-side,border-collapse,border-spacing,empty-cells,table-layout
5、列表布局属性：list-style-type,list-style-image,list-style-position,list-style
6、生成内容属性：quotes
7、光标属性：cursor
8、页面样式属性：page,page-break-inside,windows,orphans
9、声音样式属性：speak,speak-punctuation,speak-numeral,speak-header,speech-rate,volume,voice-family,pitch,pitch-range,stress,richness,azimuth,elevation
(三)所有元素可以继承的属性：
1、元素可见性：visibility
2、光标属性：cursor
(四)内联元素可以继承的属性：
1、字体系列属性
2、除text-indent，text-align之外的文本系列属性
(五)块级元素可以继承的属性
1，text-indent，text-align

13、ajax与flash的优势与劣势：
ajax优势：可搜索性；开放性；费用；易用性；易于开发
ajax劣势：可能破坏浏览器的后退功能；使用动态页面更新使得用户难于将某个特定的状态保存到收藏夹中，不过这些都有相关方法解决
flash的优势：多媒体处理；兼容性；矢量图形；客户端资源调度
flash劣势：二进制格式；格式私有；flash文件经常会很大，第一次使用需要等待较长时间；性能问题

