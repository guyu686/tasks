# html学习笔记

## 语法

1. HTML 基础结构

* 文档声明：<!DOCTYPE html>
* 根元素：<html>
*  头部：<head>（存放元数据）
*  主体：<body>（可见内容区域）
*  标题：<title>（浏览器标签页标题）

2. 文本与排版标签

* 标题：<h1>-<h6>（重要性递减）
*  段落：<p>
*  换行：<br>
*  加粗：<strong>（语义化）
*  斜体：<em>（语义化）
*  删除线：<del>
*  下划线：<ins>

3. 列表标签

*  无序列表：<ul> + <li>
*  有序列表：<ol> + <li>
*  定义列表：<dl> + <dt> + <dd>

4. 链接与图片

* 超链接：<a href="URL">
* target="_blank"（新窗口打开）
* rel="noopener noreferrer"（安全属性）
* 图片：< img src="路径" alt="描述">
* width/height（尺寸）
* loading="lazy"（懒加载）
* 图片格式：JPG（照片）、PNG（透明图）、SVG（矢量图）

5. 表单标签

* 表单容器：<form action="提交地址" method="get/post">
* 输入框：<input>
* 类型：text、password、email、checkbox、radio
* 文本域：<textarea rows="行数" cols="列数">
* 下拉菜单：<select> + <option>
* 按钮：<button type="submit">
* 必填项：required属性
* 分组：<fieldset> + <legend>

6. 多媒体与嵌入内容

* 视频：<video src="路径" controls autoplay muted>
* 音频：<audio src="路径" controls loop>
* 嵌入网页：<iframe src="网页地址">
* 嵌入文件：<embed src="文件路径">

7. 元数据

* 字符集：<meta charset="UTF-8">
* 视口适配：<meta name="viewport" content="width=device-width, initial-scale=1.0">