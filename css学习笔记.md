# css学习笔记

## 语法

一、CSS基础语法

1. 选择器

* 类型：
* 标签选择器：p
* 类选择器：.container
* ID选择器：#header
* 属性选择器：[type="button"]
* 优先级：!important > 行内样式 > ID > 类 > 标签

2. 盒模型

* 构成：content → padding → border → margin

* 尺寸计算：

    标准盒模型：总宽度 = width + padding + border + margin

    怪异盒模型：box-sizing: border-box，总宽度 = width + margin

二、布局系统

1. 传统布局

* 浮动：float（需配合clearfix清除浮动）
* 定位：
    static：默认文档流
    relative：相对自身偏移
    absolute：相对已定位祖先元素
    fixed：固定于视口
    sticky：滚动时固定

2. Flex布局（一维）

* 父容器属性：
    display: flex
    flex-direction：主轴方向
    justify-content：主轴对齐
    align-items：交叉轴对齐
* 子元素属性：
    flex：分配剩余空间
    order：排列顺序

三、视觉样式

1. 文本样式

* font-family：字体类型
* font-size：字体大小
* color：文字颜色
* text-align：文本对齐
* line-height：行高

2. 背景与边框

* 背景：background-color、background-image、background-size
* 边框：border、border-radius、box-shadow

3. 颜色表示

* 关键字：red、transparent
* RGB：rgb(255, 0, 0)
* HEX：#FF0000
* RGBA：rgba(255, 0, 0, 0.5)（含透明度）