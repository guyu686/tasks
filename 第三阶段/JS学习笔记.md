# JS学习笔记

一、JS基础语法与数据类型

1. 变量声明

* var：函数作用域，存在变量提升（不推荐）
* let：块级作用域，无变量提升
* const：块级作用域，声明常量

2. 数据类型

* 原始类型：Undefined、Null、Boolean、Number、String、Symbol
* 引用类型：Object（普通对象、数组、函数等）
* 类型判断：
    typeof：检测原始类型
    instanceof：检测引用类型
    Object.prototype.toString.call()：精准判断类型

二、流程控制与函数

1. 流程控制语句

* 条件判断：if...else、switch
* 循环：
    for：常规循环
    for...of：遍历可迭代对象
    for...in：遍历对象属性（需配合hasOwnProperty过滤）

2. 函数

* 定义方式：
    函数声明：function fn() {}（提升至作用域顶部）
    函数表达式：const fn = function() {}（无提升）
    箭头函数：const fn = () => {}（无this绑定）
* 参数与作用域：
    默认参数：function fn(a = 1, b = 2) {}
    剩余参数：...rest
    作用域链：函数内可访问外层作用域变量

3. 闭包

* 定义：函数内部嵌套函数，内部函数引用外层函数变量
* 应用：封装变量、实现初始化、缓存数据
* 注意：可能导致内存泄漏

三、对象与数组

1. 对象（Object）

* 创建方式：
    字面量：const obj = {name: 'Alice', age: 20}
    Object.create()：基于原型创建对象
* 属性操作：
    增/删：obj.key = value、delete obj.key
    遍历：for...in、Object.keys(obj)
    合并：Object.assign()、扩展运算符{...obj1, ...obj2}

2. 数组（Array）

* 常用方法：
    新增/删除：push()、pop()、shift()、unshift()
    遍历：forEach()、map()、filter()、reduce()
    查找：find()、includes()