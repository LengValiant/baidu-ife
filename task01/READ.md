# task 1_1

**表单标签label**
label元素及其重要，因为它可以帮助添加结构和增加表单的可用性和可访问性。
这个元素用来在每个表单元素中添加有意义的描述性标签。在许多浏览器中，单击元素标签将导致相关联的表单元素获得焦点。
```
/*隐式绑定*/
<label>email<input name="email" type="text"></lable>
```
或者
```
/*显式绑定*/
<lable for="author">Name:</lable>
<input name="author" id="author" type="text">
/*<label>标签的for属性应当与相关元素的id属性相同。*/
```

# task 1_2

表单的基线对齐还不清楚。(╯▽╰ )

# task 1_3
布局方法有三种

1. 按左中右方式盒子，然后全体`float: left;`，设置好中间盒子的外边距。

2. 使用flex属性布局，注意设置中间盒子`flex：1；`，不然很可能压缩其他盒子的宽度。

3. 负边距布局，双飞翼或者圣杯布局

# task_1_4
## 1.1 水平居中
### 1.1.1 行内元素
只需要把行内元素包裹在一个属性display为block的父层元素中，再给父元素设置 `text-align:center`
> 适用元素：文字，链接，及其其它inline或者inline-*类型元素（inline-block，inline-table，inline-flex）

### 1.1.2 块状元素
- 定宽块状元素
设置“左右margin”值为“auto”来实现居中
- 不定宽块状元素
1. 加入 table 标签：左右margin:auto
2. 设置 `display;inline` ，然后使用 `text-align: center`
3. 设置 `position:relative` 和 `left:50%`：给父元素设置float和 `position:relative` 和` left:50%`，子元素设置 `position:relative` 和 `left:-50%`
4. 使用flexbox布局，只需要把待处理的块状元素的父元素添加属性`display:flex`及`justify-content:center`即可

## 1.2 垂直居中
###1.2.1 父元素高度确定的单行文本
设置父元素的 height 和 line-height 高度一致。

###1.2.2 父元素高度确定的多行文本
1.插入 table (包括tbody、tr、td)标签，同时设置 vertical-align：middle
2.在 chrome、firefox 及 IE8 以上的浏览器下可以设置块级元素的 display 为 table-cell，激活 vertical-align 属性
###1.2.3 已知高度的块状元素解决方案
```
.item{
  top: 50%;
  margin-top: -50px;
  position: absolute;
  padding:0;
}
```
> 由于是div左上角与页面定位，所以要上移半个div大小


##1.3 水平垂直居中
###1.3.1  已知高度和宽度的元素解决方案
设置元素定位为absolute，并且设置top, left绝对值为50%，margin-top和margin-left为元素高度一半的负值即可。
```
.item{
   position: absolute;
   top: 50%;
   left: 50%;
   margin-top: -75px;
   margin-left: -75px;
  }
```
###1.3.2 未知高度和宽度元素解决方案
使用类似的transform属性来定义，即可实现。
```
.item{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

###1.3.3 使用flex布局实现
```
.parent{
  display: flex;
  justify-content:center;
  align-items: center;
  /* 注意这里需要设置高度来查看垂直居中效果 */
  background: #AAA;
  height: 300px;
}
```

## 1.4 隐性改变display类型
有一个有趣的现象就是当为元素（不论之前是什么类型元素，display:none 除外）设置以下 2 个句之一：
1. `position : absolute`
2. `float : left` 或 `float:right`
元素会自动变为以 `display:inline-block` 的方式显示，当然就可以设置元素的 width 和 height 了且默认宽度不占满父元素。

## 补充
1. 又一种使用绝对定位居中的方法
适用于已知道宽度或高度的元素
![](http://images.cnitblog.com/blog/130623/201310/28171709-bbe4bd7ad1af4171b4be67d452743748.png)

2. 使用浮动配合相对定位来进行水平居中
此方法也是关于浮动元素怎么水平居中的解决方法，并且我们不需要知道需要居中的元素的宽度。见1.1.2的第3点
