# css中各种单位

## px

* 绝对单位，按照像素值来显示相应的大小。

## em

* 相对单位，基准点为父节点字体的大小，如果自身定义了`font-size`按自身来计算（浏览器默认字体是16px），整个页面内`1em`不是一个固定的值。
* `em`是指字体高度 浏览器默认`1em=16px`,所以`0.75em=12px`;我们经常会在页面上看到根元素写的`font-size:62.5%`; 这样`em`就成了`16px*62.5=10em`;这是显示在页面的字体大小是`10px`; 这样`12px=1.2em`,`10px=1em`,也就是说只需要将你的原来的`px`数值除以10，然后换上`em`作为单位就行了。
* `em`是个相对值 他会根据父级元素的大小而变化 但是如果嵌套了多个元素 要计算它的大小,是件很头疼的事情。这样的情况下,就出现了`rem`,`rem`的区别在于它是相对于根基元素的,因此不会被它的父类影响到。

## rem

* 相对单位，可理解为`root em`, 相对根节点`html`的字体大小来计算，`CSS3`新加属性，`chrome/firefox/IE9+`支持。

## vw

* viewpoint width，视窗宽度，1vw等于视窗宽度的1%。

## vh

* viewpoint height，视窗高度，1vh等于视窗高度的1%。

## vmin

* vw和vh中较小的那个。

## vmax

* vw和vh中较大的那个。

## vw,vh,vmin,vmax,IE9+局部支持，chrome/firefox/safari/opera支持，ios safari 8+支持，android browser4.4+支持，chrome for android39支持