### 1.CSS 盒子模型(Box Model)
所有HTML元素可以看作盒子，在CSS中，"box model"这一术语是用来设计和布局时使用。
CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。
盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。
* Margin(外边距) - 清除边框外的区域，外边距是透明的。
* Border(边框) - 围绕在内边距和内容外的边框。
* Padding(内边距) - 清除内容周围的区域，内边距是透明的。
* Content(内容) - 盒子的内容，显示文本和图像。
### 2. box-sizing的应用场景
标准盒子（W3C标准）与IE盒子之间的切换
* content-box:此值为其默认值，其让元素维持W3C的标准Box Model，也就是说元素的宽度/高度（width/height）等于元素边框宽度（border）加上元素内边距（padding）加上元素内容宽度/高度（content width/height）即：Element Width/Height = border+padding+content width/height
* border-box:此值让元素维持IE传统的Box Model（IE6以下版本），也就是说元素的宽度/高度等于元素内容的宽度/高度。（从上面Box Model介绍可知，我们这里的content width/height包含了元素的border,padding,内容的width/height【此处的内容宽度/高度=width/height-border-padding】）。
### 3.textarea标签有默认文字的情况下，点击输入文字，然后删掉输入的文字，正常情况下应该显示的是默认文字，但是在某些手机的一些浏览器，特别是Safari浏览器中，显示的默认文字不全，有缺失的情况。
解决办法：height=line-height*rows
```
<textarea class="remark" rows="3">
在w3school，你可以找到你所需要的所有的网站建设教程。
</textarea>
.remark::-webkit-input-placeholder{
   line-height=12px;
   height=36px;
}
 ```
### 4.flex布局
Flex是Flexible Box的缩写，意为”弹性布局”。Flex可以简便、完整、响应式地实现多种页面布局。
<br>采用 Flex 布局的元素，称为 Flex 容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目"。</br>
容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；交叉轴的开始位置叫做cross start，结束位置叫做cross end。  
Flex项目默认沿主轴排列。单个项目占据的主轴空间叫做main size，占据的交叉轴空间叫做cross size。
Flex属性分为两部分，一部分作用于容器称容器属性，另一部分作用于项目称为项目属性
### 4.1 容器属性
* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content
### 4.2 项目属性
- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- align-self


### 6. 未知宽高的div元素垂直水平居中
方法1：通过定位和transform属性来实现
```
<style>
    .parent{
        width:100%;
        height:400px;
        background:#666;
        position:relative;
    }
    .children{
        position:absolute;
        top:50%;
        left:50%;
        background:red;
        transform:translate(-50%,-50%);
    }
</style>
```
方法2：通过利用flex布局
```
<style>
    .parent{
        width:100%;
        height:400px;
        background:#666;
        display:flex;
        align-items:center;
        justify-content:center;
    }
    .children{
        background:red;
    }
</style>
```
方法3：通过table属性:将父元素设置为table，子元素设置为table-cell，利用table属性
```
<style>
    .parent{
        display:table;
        width:100%;
        height:400px;
        background:#666;
    }
    .children{
        display:table-cell;
        vertical-align:middle;
        text-align:center;
        background:red;
    }
</style>
```
### 7. 原型，原型链，对象，构造函数之间的联系
* 对象：无序属性的集合，其属性可以包含基本值，对象和函数；严格来说，对象就是一组没有特定顺序的值。
### 8. Dom事件的几种绑定方式
### 9. https,http2.0,websocket

### 10. webpack的入口文件怎么配置，多个入口怎么分割

### 11. transform-runtime和stage
