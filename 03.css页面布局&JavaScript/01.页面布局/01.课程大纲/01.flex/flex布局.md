### 一.flex概述

> 全称为 “`Flexible Box Layout`”，即 **“弹性盒布局”**，旨在提供一种更有效的方式来**布局、对齐和分配容器中项目之间的空间，即使它们的大小未知或动态变化**。
>
> Flex是Flexible Box的缩写，意为”弹性布局”，用来为盒状模型提供最大的灵活性。

### 二.flex基本概念

##### 2.1 容器与项目

> 采用Flex布局的元素，称为Flex容器（flex container），简称”容器”。它的所有直接子元素自动成为容器成员，称为Flex项目（flex item），简称”项目”。

<img src="https://www.runoob.com/wp-content/uploads/2015/07/3791e575c48b3698be6a94ae1dbff79d.png" alt="img" style="zoom:200%;" />

> 容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；交叉轴的开始位置叫做cross start，结束位置叫做cross end。
>
> 项目默认沿主轴排列。单个项目占据的主轴空间叫做main size，占据的交叉轴空间叫做cross size。

##### 2.2 容器属性 -  flex-direction属性

flex-direction属性决定主轴的方向（即项目的排列方向）。

```css
.box {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

![img](https://www.runoob.com/wp-content/uploads/2015/07/0cbe5f8268121114e87d0546e53cda6e.png)

- row（默认值）：主轴为水平方向，起点在左端。
- row-reverse：主轴为水平方向，起点在右端。
- column：主轴为垂直方向，起点在上沿。
- column-reverse：主轴为垂直方向，起点在下沿。

##### 2.3 容器属性 -  flex-wrap属性

默认情况下，项目都排在一条线（又称”轴线”）上。flex-wrap属性定义，如果一条轴线排不下，如何换行。

![img](https://www.runoob.com/wp-content/uploads/2015/07/903d5b7df55779c03f2687a7d4d6bcea.png)

```css
.box{
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

它可能取三个值。

（1）nowrap（默认）：不换行。

![img](https://www.runoob.com/wp-content/uploads/2015/07/9da1f23965756568b4c6ea7124db7b9a.png)

（2）wrap：换行，第一行在上方。

![img](https://www.runoob.com/wp-content/uploads/2015/07/3c6b3c8b8fe5e26bca6fb57538cf72d9.jpg)

（3）wrap-reverse：换行，第一行在下方。

![img](https://www.runoob.com/wp-content/uploads/2015/07/fb4cf2bab8b6b744b64f6d7a99cd577c.jpg)

##### 2.4 容器属性 -  justify-content属性

justify-content属性定义了项目在主轴上的对齐方式。

```
.box {
  justify-content: flex-start | flex-end | center | space-between | space-around;
}
```

![img](https://www.runoob.com/wp-content/uploads/2015/07/c55dfe8e3422458b50e985552ef13ba5.png)

它可能取5个值，具体对齐方式与轴的方向有关。下面假设主轴为从左到右。

- flex-start（默认值）：左对齐
- flex-end：右对齐
- center： 居中
- space-between：两端对齐，项目之间的间隔都相等。
- space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。