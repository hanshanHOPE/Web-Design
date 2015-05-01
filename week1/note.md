##使用Emmet
section.hero>(header>img+ul>li*3)+h1+h2+(form>input[type="text"]+imput[type="button"])
真是键动如飞

##HTML
img标签
alt特性(attribute)：文件加载错误或文件加载过程中用以显示内容。


##CSS
<pre><code>
body {
	font-size: 62.5%;
	text-align: center;
}</code></pre>

设置文档字体大小很流行的一种做法是在body中将font-size设为62.5%。也就是设为默认值16px的62.5%，即为10px，或0.625em。之后就可以很方便地使用em单位，1em = 10px。
text-align 描述了inline 内容 在其 parent block 中的对齐方式，text-align不控制 block 元素本身的对齐方式，
只控制 inline content

####inline与block
html元素通常为 inline 或是 block-level 元素。一个inline元素通常只占据定义该inline元素的标签的空间大小，比如p中定义的span. 常见的inlime element：img、script、button、input、label、select、textarea。
block-level, 它通常占据其父元素的全部空间。
inline 与 block 的比较：
1.格式。一般而言，block-level 元素会另起一行。
2.内容。block-level 可以包含 inline 或是 block-level 元素。

####float
导航条列表
<pre><code>
ul {
    float: right;
	li {
		float: left;
		margin: 0.5em;
		padding: 1em;
	}
}</code></pre>
<p>@include clearfix;
使用float调整元素位置
float将元素从文档流中分离，置于所包含其容器的左侧或右侧。同时，文本和inline元素将环绕它。
一个浮动中的元素(floating element)是指float值不为none。</p>

####clear


####dispaly与visibility
关于display property。
display property 。初始值为inline
none很特殊，可以用来禁止指定元素的显示，以及从属于它的元素。为了不显示指定元素，通常有两种方法，
设置display 和 visibility。
visibility会隐藏某一元素，同时保留它原来的位置，初始值为visible；隐藏某一元素可以使用hidden，hidden会让元素区域完全透明，但依旧存在与布局中。如果从属元素的visibility 被设为visible，它依旧会被显示。
display设为none，将该元素从文档流中分离。


至此，可以总结一下将元素脱离文档流的方法：
1.position 中 absolute及fixde
2.display: none
3.float

####list-style
list-style是list-style-type、list-style-image和list-style-position的简写。
list-style-type:none，无项目符号。


####background
background-image指定背景图片的相对路径，相对于CSS文件所在路径。
background-size 指定background-image的尺寸，CSS3特性。如果选区为矩形，图片为正方形，cover图片会被放大至长的那条边，一部分会不可见；contain会将图片放大至较短的那条边。详见w3school。

####盒子模型
box-sizing指明元素width和height的计算方式，包含content-box、padding-box和border-box。
content-box，默认值。width和height的计算只包含content。padding、border和margin将在盒子之外。
padding-box，width和height的计算将包含padding的尺寸，不包含border和margin。
border-box, width和height的计算将包含padding、border，不含margin。
一般会指定border、padding的值，如果选用border-box,content的值是计算出来的。


####伪类(Pseudo-classes)
将伪类添加至CSS选择器来指明被选元素的状态，如:hover。

####伪元素(Pseudo-elements)
与伪类相似，伪元素也被添加至CSS选择器中，但不是用来描述某一特殊状态，而是用来指定文档中某一部分的样式，比如::after。常见的伪元素有::after,::before,::first-letter, ::first-line等。为了区别于伪类，CSS3使用::
