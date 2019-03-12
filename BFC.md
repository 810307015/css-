# BFC(Block Fromatting Context) --- 块级格式上下文

## 基本概念

* 浮动元素和绝对定位元素，非块级盒子的块级容器（例如 inline-blocks, table-cells, 和 table-captions），以及overflow值不为“visiable”的块级盒子，都会为他们的内容创建新的BFC（块级格式上下文）。
* BFC是一个独立的布局环境，其中的元素布局是不受外界的影响，并且在一个BFC中，块盒与行盒（行盒由一行中所有的内联元素所组成）都会垂直的沿着其父元素的边框排列。

## 区分（满足以下的条件的就会自动创建BFC模型）

1. float的值不是none。
2. position的值不是static或者relative。
3. display的值是inline-block、table-cell、flex、table-caption或者inline-flex。
4. overflow的值不是visible。

## 对比

* 常规流布局时，盒子都是垂直排列，两者之间的间距由各自的外边距所决定，但不是二者外边距之和。
* BFC可能造成外边距折叠，也可以利用它来避免这种情况。BFC产生外边距折叠要满足一个条件：两个相邻元素要处于同一个BFC中。所以，若两个相邻元素在不同的BFC中，就能避免外边距折叠。

## 具体参考

* 地址：`https://www.cnblogs.com/libin-1/p/7098468.html`.