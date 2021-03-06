###Welcome to My Html Little Knowledge
####块级元素  
+ 没有设置宽度时，块级元素的宽度是其容器的100%  
+ 可以给块级元素设置宽高、内边距、外边距等盒模型属性  
+ 常见的块级元素有 `<div>`、`<h1>~<h6>`、`<p>`、`<ul>`、`<ol>`、`<dl>`、`<table>`、`<address>`、`<form>`等  
####行内元素  
+ 行内元素不会独占一行，只会占领自身宽高所需要的
+ 给行内元素设置宽高不会起作用，`margin`和`padding`只对左右起作用
+ 行内元素一般不可以包含块级元素，只能包含行内元素和文本
+ 常见的行内元素有`<a>`、`<b>`、`<lable>`、`<span>`、`<img>`、`<em>`、`<strong>`、`<i>`、`<input>`等  

设置为**inline-block**的元素，既有块级元素可以设置宽高的特性，又有行内元素不换行的特性

####*position*的常用属性值
`relative`：相对定位，相对于元素的正常位置进行定位  
`absolute`：绝对定位，相对于出`static`定位意外的以外进行定位  
`fixed`：固定定位，相对于浏览器窗口进行定位，网站中固定的`header`和`footer`就是用固定定位来实现的  
`static`：默认值，没有定位属性，元素正常出现在文档流中
`inherit`：继承父元素的`position`的属性值  

####清除浮动
`clear`：用来定义哪一例不允许其他元素浮动，常见的值有`left`、`right`、`both`，分别表示`左侧不允许浮动元素`、`右侧不允许浮动元素`、`左右两侧不允许浮动元素`  
`overflow`：给父元素设置  
`after伪元素`：该方法的本质也是在末尾添加一个看不见的块元素来清除浮动，这个方法也不存在语义化的问题，是目前主流的清除浮动的方法

#### flex布局  
`flex-direction`：定义了主轴方向，即项目的排列方向  
+ `row(默认值)`：主轴在水平方向，起点在左侧，也就是我们常见的从左到右  
+ `row-reverse`：主轴在水平方向，起点在右侧  
+ `column`：主轴在垂直方向，起点在上沿  
+ `column-reverse`：主轴在垂直方向，起点在下沿  

默认情况下，项目是排成一行显示的，`flex-warp`用来定义当一行放不下时，项目如何换行  
+ `nowrap（默认）`：不换行  ，即使设置了项目的宽度，项目也会根据屏幕的大小被压缩  
+ `wrap`：换行，第一行在上面
+ `wrap-reserve`：换行，第一行在下面  

####居中问题

 `text-align：center`：让子元素水平居中，但只对图片、按钮、文字等行内元素起作用  
 `margin:auto`：适用于块级元素，其实就是把要居中的子元素的`margin-right`、`margin-right`都设置为`auto`，该方法能让子元素水平居中，但是对浮动元素和绝对定位的元素无效。  
 `line-height:父元素的高度`：适用于只有一行文字的情况

####文字太长显示省略号  
```

overflow-x:hidden;//超出隐藏
white-space:nowrap;//溢出不换行
text-overflow:ellipsis;//溢出省略号显示

```  

####css伪元素   

* `:before`  在每个被选元素前插入内容，使用`content`属性来指定要插入的内容  
* `:after`  在每个被选元素之后插入内容，使用`content`属性来指定要插入的内容  
* `:first-line`  向文本的首行设置特殊样式，只用于块级元素
* `:first-letter`  向文本的首字母设置特殊样式

#### css伪类  
* `:link`  向未被访问的链接添加样式
* `:visited`  已被访问的链接
* `:hover`  鼠标悬停样式
* `:active`  点击之后（激活）的样式
* `:first-child` 匹配的第一个元素添加样式

**a使用伪类的时候顺序必须为：link ,visited,hover,active**

#### meta  

`<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">`  
阻止网页自己放大或缩小  
