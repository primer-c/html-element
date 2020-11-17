---
title: 第五章：5.2 HTML常用块级元素汇总表
date: October 14 2020
tags: HTML5
---

### 1. 块级元素(Block)的定义

1. 总是在新行上开始
2. 高度，行高以及外边距和内边距都可控制；
3. 宽度缺省是它的容器的100%，除非设定一个宽度；
4. 它可以容纳内联元素和其他块元素；
5. 多个块状元素标签写在一起，默认排列方式为从上至下；

### 2.块级元素汇总表

1. 常用块级元素

   | 元素名称(element name) | 说明(discription)                | 参考文档                                                     |
   | ---------------------- | -------------------------------- | ------------------------------------------------------------ |
   | **body**               | 文档内容                         | [参考文档]()                                                 |
   | **h1~h6**              | 定义标题标签(heading)            | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/H%20Element/) |
   | **div**                | 布局元素，不表示任何其他内容分组 | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/DIV%20Element/) |
   | **p**                  | 表示段落                         | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/P%20Element/) |
   | **hr**                 | 段落级别的主题变换               | [略]                                                         |
   | **table**              | 表格元素                         | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Table%20Element/) |
   | **form**               | 表单元素                         | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Form%20Element/) |
   | **ul**                 | 无序列表                         | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/UL%20Element/) |
   | **li**                 | 列表象                           | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/LI%20Element/) |
   | **ol**                 | 有序列表                         | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/OL%20Element/) |
   | **dl**                 | 生成术语及其定义的列表           | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/DL%20Element/) |
   | **dt**                 | 列表项                           | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/DT%20Element/) |
   | **dd**                 | 列表项                           | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/DD%20Element/) |
   | **pre**                | 预定义元素                       | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Pr%20Element/) |
   | **caption**            | 标题                             | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Caption%20Element/) |
   | **figure**             | 插图                             | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Firgure%20Element/) |
   | **figcaption**         | 插图标题                         | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Figcaption%20Element/) |
   | **blockquote**         | 引自他处的内容                   | [参考文档](https://yuanmin650304.github.io/2020/10/14/HTML/Elements%20Description/Blockquote%20Element/) |


### 3. HTML5新增块级元素汇总表

1. HTML5元素主要变化： 将元素语义与其内容呈现结果的影响分开；

2. HTML元素负责文档内容的结构和含义，而内容的呈现则由CSS样式控制；

3. HTML5中新增的大多数元素都具有含义；

   | 元素名称(element name) | 说明(discription)                    | 元素类型(type) |
   | ---------------------- | ------------------------------------ | -------------- |
   | **section**            | 文档节                               |                |
   | **nav**                | 导航                                 |                |
   | **header**             | 页眉                                 |                |
   | **article**            | 文章                                 |                |
   | **aside**              | 文章侧栏                             |                |
   | **footer**             | 页脚                                 |                |
   | **details**            | 元素的细节                           |                |
   | **summary / details**  | 元素可见的标题                       |                |
   | **dialog**             | 对话框窗口                           |                |
   | **h1,h2,h3,h4,h5,h6**  | 标题                                 |                |
   | **p**                  | 段落                                 |                |
   | **ul**                 | 无序列表                             |                |
   | **ol**                 | 有序列表                             |                |
   | **dir**                | 目录列表                             |                |
   | **li**                 | 项目                                 |                |
   | **dl**                 | 列表                                 |                |
   | **dt**                 | 列表项目                             |                |
   | **dd**                 | 项目描述                             |                |
   | **menu**               | 命令的菜单,列表                      |                |
   | **menuitem**           | 菜单项目                             |                |
   | **command**            | 命令按钮                             |                |
   | **form**               | 表单                                 |                |
   | **fieldset**           | 围绕元素的边框(可用于表单内元素分组) |                |
   | **legend**             | 在边框上的标题                       |                |
   | **select**             | 选择列表(内联元素)                   |                |
   | **optgroup**           | 组合选择列表选项                     |                |
   | **option**             | 选择列表选项(也可做datalist选项)     |                |
   | **table**              | 表格                                 |                |
   | **caption**            | 格标题                               |                |
   | **thead**              | 组合表头内容(th)                     |                |
   | **tbody**              | 组合主体内容(td)                     |                |
   | **tfoot**              | 组合表注内容(td)                     |                |
   | **tr**                 | 表格行                               |                |
   | **th**                 | 表头单元格                           |                |
   | **td**                 | 表格单元                             |                |
   | **col**                | 表格列属性;(空标签)                  |                |
   | **colgroup**           | 表格格式化列组                       |                |
   | **iframe**             | 内联框架(不推荐)                     |                |
   | **figure**             | 媒介内容分组                         |                |
   | **figcaption:figure**  | 标题                                 |                |
   | **map**                | 图像映射                             |                |
   | **area**               | 图像区域                             |                |
   | **canvas**             | 图形容器(脚本来绘制图形)             |                |
   | **video**              | 视频                                 |                |
   | **source**             | 媒介源                               |                |
   | **track**              | 文本轨道                             |                |
   | **audio**              | 声音内容                             |                |
   | **br**                 | 换行(空标签)                         |                |
   | **hr**                 | 平分割线(空标签)                     |                |
   | **pre**                | 格式文本                             |                |
   | **blockquote**         | 块引用                               |                |
   | **address**            | 文档联系信息                         |                |
   | **center**             | 居中文本(不赞成使用)                 |                |
   | **spacer**             | 在水平和垂直方向插入空间(空元素)     |                |


[[<--Previous]](https://yuanmin650304.github.io/2020/10/14/HTML/%E7%AC%AC%E4%B8%80%E9%83%A8%E5%88%86%20HTML/05-HTML5%E5%85%83%E7%B4%A0/HTML5%E5%85%83%E7%B4%A0%E6%96%B0%E5%A2%9E%E7%9A%84%E5%8A%9F%E8%83%BD/)                                                
[[Next-->]](https://yuanmin650304.github.io/2020/10/14/HTML/%E7%AC%AC%E4%B8%80%E9%83%A8%E5%88%86%20HTML/05-HTML5%E5%85%83%E7%B4%A0/HTML5%20%E8%A1%8C%E7%BA%A7%E5%85%83%E7%B4%A0%E6%B1%87%E6%80%BB%E8%A1%A8/)


