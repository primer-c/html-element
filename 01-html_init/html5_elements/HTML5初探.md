---
title: 1.1 HTML5简介
date: 2020-03-10
tags: HTML5
---

### HTML 的发展简史

1. HTML(Hypertext Markup Language,超文本标记语言)： 诞生于 20 世纪 90 年代初期，是由网景公司拥有，并成为其旗下 Netscape Navigator 的开发语言;

2. 后来 Microsoft 也开始利用这种技术开发自己的浏览器；

3. HTML 从诞生到 HTML5 版本，共经历以下版本号和发展时期：

   表一： HTML各版本发布时间

   | 版本号  | 发布时间                            |
   | ------- | ----------------------------------- |
   | HTML2.0 | 1995 年 11 月                       |
   | HTML3.2 | 1996 年 1 月 14 日，W3C 推荐标准；  |
   | HTML4.0 | 1997 年 12 月 18 日，W3C 推荐标准； |
   | HTML4.1 | 1999 年 12 月 24 日，W3C 推荐标准； |
   | HTML5   | 2008 年 1 月 22 日，W3C 推荐标准；  |


### JavaScript 的发明

1. JavaScript 是网景公司(Netscape)的工程师，Brendan Eich 于 1995 年用十天时间，编写的一个公司内部脚本语言，很快就在 Web 开发领域得到广泛的应用，由于 Brendan 的轻率，致使这种语言很多地方都存在 BUG，因此，W3C 和 ECMA(欧洲计算机制造商协会)不得不多次对这种语言进行规范化，因此，后期出现了 ECMA-2015，ECMA-2016，ECMA-2017 等不同的规范；


### 第一次浏览器大战

1. 1994 年开始，Netscape 和 Microsoft 为了 争夺市场份额，掀起了第一次浏览器大战；
2. 97 年 Microsoft 将 IE 于 Window95 操作系统捆绑销售，网景最终宣布破产；
3. 1998 年网景公开了它的浏览器源码，并重新命名为 Mozilla，全部程序进行了重写；

### 第二次浏览器大战

1. 网景公司虽然破产，但是，这帮骨干最终成立了 Firefox 基金，2002 年发布了第一个版本；
2. 2004 年基于 Mozilla 源码的 Firefox 首次登台，拉开了第二次浏览器大战的序幕；
3. 第二次大战并不像第一次那么简单，除了火狐狸外，还有挪威的 Opera，Google 也以他的 Chrome 投入了大战；
4. 2009 年 Apple 的 Safari 也投入到这场残酷的大战；
5. 浏览器大战造成的结果，就是各个厂家之间的浏览器互不兼容。无论是 HTML，还是 CSS，或者是 JavaScript 都是这样。这就给开发工作带来很大的工作量，需要写很多不必要的代码；
6. 在这种情况下，行业内部要求统一规范和标准呼声越来越高，HTML 最终发布了 HTML5；
7. CSS 最终制定了 CSS3 标准
8. JavaScript 则一直在不断制定新的标准，目前，还在使用的有 ES4，ES5，ES6，ES7，ES8，ES9，以及 Microsoft 发布的 TypeScrip；
9. Google 采用了兼容所厂家的策略，最终，成为了最大赢家；

### HTML5 新增内容

1. HTML5 定义的许多元素 HTML4 中也存在，但是，元素的含义已经发生了很大的变化，或者，其使用方式已经不同；
2. HTML5 本身还新增了许多新的元素；
3. 需要指出的是 HTML5 规范不是简单地删除或新增了一些元素，而且新增了以下内容：

- Canvas： 2D 和 3D
- Cross-Document
- Geolocation
- Audio and Video
- Forms
- MathML
- Microdata
- File System API
- Server-Sent Events
- Scalable Vector Graphics(SVG)
- WebSocket API
- Web Workers API
- Web RTC API
- Web Origin Concept
- Web Storage
- XMLHttpRequest Level 2
- Web 离线缓存应用
- 拖放

顾名思义， HTML 是一种标记语言，以其标记为文档内容的元素文档的结构；

### 元素

1. 元素不区分大小写；
2. 内容与呈现分离

#### 1. 基本元

1. 表二： 基本元素

   | **元素 (element)** | **说明（description)**    |
   | ------------------ | ------------------------- |
   | !DOCTYPE           | 声明当前文档为 HTML5 文档 |
   | html               | 文档根目录                |
   | head               | 文档头部标签              |
   | title              | 文档标题标签              |
   | mate               | 文档元数据标签            |
   | link               | 文档外链接标签            |
   | script             | 文档外部资源标签          |
   | style              | 文档内联样式标签          |
   | body               | 文档主题标签              |


#### 2 常用元素

1. 表三： 常用元素

   - 表三： 常用元素

   | **元素 (element)** | **说明（description)** | 元素类型         |
   | ------------------ | ---------------------- | ---------------- |
   | div                | 定义文档中的节(容器)   | 块级元素(block)  |
   | p                  | 段落                   | block            |
   | ul                 | 无序列表               | block            |
   | ol                 | 有序列表               | block            |
   | li                 | 定义列表的项目         | block            |
   | span               | 定义文档中的节(容器)   | 行级元素(inline) |
   | b                  | 粗体文本               | inline           |
   | i                  | 斜体文本               | inline           |
   | table              | 表格                   | block            |
   | tr                 | 表格的行元素           | block            |
   | th                 | 头部单元格             | block            |
   | td                 | 体部单元格             | block            |
   | br                 | 折行                   | inline           |
   | hr                 | 水平线                 | block            |
   | label              | input说明              | inline           |
   | input              | 输入框                 | block            |
   | textarea           | 多行输入框             | block            |
   | a                  | 链接                   | inline           |
   | img                | 图片                   | inline-block     |


#### 3. 空元素

1. 没有内容的元素

   ```html
   I like
   <div></div>
   apples and oranges
   ```

#### 4. 自闭合元素

1.  对于空元素，可以用一个标签代替，以简洁标签；

   ```html
   I like
   <div />
   apples and oranges
   ```

#### 5. 虚元素（void element）

1. 有些元素只能使用一个标签，并且在其中不能插入任何内容的元素；

   ```html
   I like apples and oranges
   <hr />
   Today was warm and sunny <br />
   I would like go fishing;
   ```

#### 6. 元素属性(attribute)

1. 一个元素可以有多个属性

   ```html
   I like <a class="link" href="/apple.html" id="firstlink">apples</a> and oranges
   ```

2. 使用布尔属性

   ```html
   Enter your name <input disabled />
   ```

3. 自定义属性

   ```html
   Enter your name
   <input disabled="true" data-creator="adam" data-purpose="collection" />
   ```

###### 7. 创建 HTML 文档

1. 元数据标签： 向浏览器提供文档的相关信息；

2. 父元素、子元素、后代元素、兄弟元素

3. 元素分类：元数据元素(metadata element)、流元素 (flow element)、短语元素(phrasing element)

   a) 元数据元素(metadata element)

   - 构建 HTML 文档的基本结构，向浏览器提高文档信息；

   b) 流元素 (flow element)

   - 规定这些元素可以成为父元素；
   - 是短语元素的超级；
   - 短语元素都是流元素；
   - 但是，流元素并不一定是短语元素；

   c) 短语元素(phrasing element)

   - 和流元素呼应，规定这些元素可以成为子元素

   d) 无法归入上述三种类型的元素；

   - 例如： `<li></li>`元素，只能用在非常有限的情况，只能有三种父元素；
   - `<ul></ul>`无序列表，`<ol></ol>`有序列表，`<menu></menu>`菜单；

   ```html
   <!DOCTYPE html>
   <html lang="zh">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta http-equiv="X-UA-Compatible" content="ie=edge" />
       <title></title>
       <link rel="stylesheet" href="css/index.css" />
     </head>
     <body>
       <div class="container">
         <ul>
           <li>I like<a href="/apple.html">apples</a> and oranges</li>
           <li>Today was warm and sunny.</li>
           <li>I would like go fishing;</li>
         </ul>
       </div>
     </body>
   </html>
   ```

#### 8. 使用 HTML 实体

1. HTML 的实体(entity):

   - 表四： 特殊字符

   | 字符  | 实体名称 | 实体编码 |
   | ----- | -------- | -------- |
   | `' '` | `&nbsp;` | `&#160;` |
   | <     | &lt;     | &#60;    |
   | >     | &gt;     | &#62;    |
   | &     | &amp;    | &#38;    |
   | "     | &quot;   | &#34;    |
   | '     | &apos;   | &#39;    |
   | €     | &euro;   | &#8364;  |
   | £     | &pound;  | &#163;   |
   | ¥     | &yen;    | &#165;   |
   | ©     | &copy;   | &#169;   |
   | ®     | &reg;    | &#174;   |
   | ™     | &trade;  | &#8482;  |
   | ×     | &times;  | &#215;   |
   | ÷     | &divide; | &#247;   |

#### 9. HTML5 全局属性

1. 全局属性： global attribute；

2. 局部属性：local attribute；

   - 表五： HTML5全局属性

   | **属性()**      | **元素(element)** | **说明(description)**           |
   | --------------- | ----------------- | ------------------------------- |
   | style           | 短语元素          | css行内属性                     |
   | lang            | 短语元素          | 说明元素内容使用的语言          |
   | id              | 短语元素          | css id                          |
   | class           | 短语元素          | css 类                          |
   | accesskey       | input             | 设定一个或几个页面元素的快捷键  |
   | dir             | 短语元素          | 规定了文字的方向                |
   | contenteditable | 短语元素          | 规定内容是可编辑的              |
   | draggable       | 短语元素          | 规定了元素可以拖放              |
   | dropzone        | 短语元素          | 与draggable配套                 |
   | hidden          | 短语元素          | 隐藏元素                        |
   | spellcheck      | 短语元素          | 是否对元素内容做拼写检查        |
   | tabindex        | 短语元素          | 键盘`Tab`在HTML页面元素之间切换 |
   | title           | 短语元素          | 提供元素的额外信息              |

3. example1: accesskey

   ```html
   <!DOCTYPE html>
   <html lang="zh">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta http-equiv="X-UA-Compatible" content="ie=edge" />
       <title>Demo for accesskey</title>
     </head>
     <body>
       <form action="http://localhost:5000/user">
         <label for="username">用户名</label>
         <!-- Alt + n -->
         <input type="text" name="username" id="username" accesskey="n" /><br />
         <label for="password">密码</label>
         <!-- Alt + p -->
         <input type="text" name="password" id="password" accesskey="p" /><br />
         <label for="confirm">确认</label>
         <!-- Alt + c -->
         <input type="text" name="confirm" id="confirm" accesskey="c" /><br />
         <!-- Alt + s -->
         <input type="submit" value="Login" accesskey="s" />
       </form>
     </body>
   </html>
   ```

4. example2: class

   ```html
   <!DOCTYPE html>
   <html lang="zh">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta http-equiv="X-UA-Compatible" content="ie=edge" />
       <title>Demo for class</title>
       <style>
         .apress {
           padding: 5px;
           margin: 2px;
           color: white;
           background: #aaa;
         }
         .apple {
           font-size: x-large;
           display: block;
           margin-top: 20px;
         }
       </style>
     </head>
     <body>
       <a href="https://apress.com" class="apress">Apress web site</a>
       <a href="https://apple.com" class="apple add">Apple web site</a>
       <script>
         let add = document.querySelector('.add')
         add.style.border = 'thin solid black'
         add.style.background = 'red'
         add.style.color = 'white'
       </script>
     </body>
   </html>
   ```

5. example 3: contenteditable 属性

   - 文本可编辑

   ```html
   <!DOCTYPE html>
   <html lang="zh">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta http-equiv="X-UA-Compatible" content="ie=edge" />
       <title>Demo for contenteditable</title>
     </head>
     <body>
       <p contenteditable="true">It is raining right now.</p>
     </body>
   </html>
   ```

6. example 4: dir 属性

   - 规定了文字的方向： ltr 或者 rtl

   ```html
   <!DOCTYPE html>
   <html lang="zh">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta http-equiv="X-UA-Compatible" content="ie=edge" />
       <title>Demo for dir</title>
     </head>
     <body>
       <p dir="ltr">This is left-to-right</p>
       <p dir="rtl">This is right-to-left</p>
     </body>
   </html>
   ```

7. example 5: draggable and dropzone 属性

   - 详见拖放

   ```html
   <img src="imgs/timg.jpg" draggle="true" />
   ```

8. example 6: lang 属性

   - 说明元素内容使用的语言

   ```html
   <p lang="en">Hello -Tomas How are you?</p>
   ```

9. example 7: spellcheck 属性

   ```html
   <!DOCTYPE html>
   <html lang="zh">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <meta http-equiv="X-UA-Compatible" content="ie=edge" />
       <title>Demo for dir</title>
     </head>
     <body>
       <textarea spellcheck="true" cols="50px" rows="10px">
   This is some mispelled text</textarea
       >
     </body>
   </html>
   ```

10. example 8: tabindex 属性

    - 按下 Tab 键时，按数字的从小到大一次选取元素内容

    - 数值为负值时，不被选中

    ```html
    <!DOCTYPE html>
    <html lang="zh">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <meta http-equiv="X-UA-Compatible" content="ie=edge" />
        <title>Demo for tabindex</title>
      </head>
      <body>
        <form action="http://localhost:5000/user">
          <label for="username">用户名</label>
          <!-- Tab -->
          <input type="text" name="username" id="username" tabindex="2" /><br />
          <label for="password">密码</label>
          <!-- Tab -->
          <input type="text" name="password" id="password" tabindex="1" /><br />
          <label for="confirm">确认</label>
          <!-- Tab 不被选中-->
          <input type="text" name="confirm" id="confirm" tabindex="-1" /><br />
          <input type="submit" value="Login" />
        </form>
      </body>
    </html>
    ```

11. example 9: title 属性

    - 提供元素的额外信息： 鼠标悬停时，显示工具提示

      ```html
      <!DOCTYPE html>
      <html lang="zh">
        <head>
          <meta charset="UTF-8" />
          <meta name="viewport" content="width=device-width, initial-scale=1.0" />
          <meta http-equiv="X-UA-Compatible" content="ie=edge" />
          <title>Demo for title</title>
        </head>
        <body>
          <a href="https://apress.com" title="Apress Publishing"
            >Visit the apress site
          </a>
        </body>
      </html>
      ```

#### 10. 新的 DOCTYPE 和字符集

- DOCYTYPE

  浏览器的显示模式有多种：

  1. Strandards: 标准模式
  2. DOCTYPE 会告诉浏览器采用：Standards 模式显示

  ```html
  <!DOCTYPE html>
  ```

- 字符集

  字符集也简化很多了

  ```html
  <meta charset="UTF-8" />
  ```
