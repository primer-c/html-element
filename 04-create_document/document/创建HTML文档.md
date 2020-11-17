# 创建HTML文档

本章介绍HTML5的基本元素：文档元素和元数据元素；

1. 元素

   | 元素(element) | 说明(description)                        | 父元素     | 子元素     | 局部属性                              | 类型(type)   |
   | ------------- | ---------------------------------------- | ---------- | ---------- | ------------------------------------- | ------------ |
   | **DOCTYPE**   | HTML版本号，HTML5                        | 无         | 无         |                                       | 无           |
   | **html**      | HTML文档根元素                           | 无         | head、body | manifest                              | 无           |
   | **head**      | HTML文档的头部信息                       | html       | title      |                                       | 无           |
   | **body**      | HTML文档的主题内容                       | html       | 短语、流   |                                       | 无           |
   | **meta**      | 提供文档信息                             | head       | 无         | name， content， chartset，http-equiv | 元数据       |
   | **link**      | 定义与外部资源(样式表和网站图标)         | head       | 无         |                                       | 元数据       |
   | **base**      | 设置相对URL                              | head       | 无         | href，garget                          | 元数据       |
   | **script**    | 定义脚本程序： 文档内嵌或者外部文件      | body、head | 无         |                                       | 元数据，短语 |
   | **noscript**  | 浏览器禁用脚部或者不支持脚本时显示的内容 | body       | 无         |                                       | 元数据，短语 |
   | **style**     | 定义文档内联CSS样式                      | head       | 无         |                                       | 元数据       |
   | **title**     | 设置文档标题                             | head       | 无         |                                       | 元数据       |

2. 属性

   | **属性**         | **说明**                                             |
   | ---------------- | ---------------------------------------------------- |
   | **charset**      | **声明HTML文档的字符编码**(meta)                     |
   | **http-equiv**   | 设置HTML文档的默认样式表或周期性地刷新页面内容(meta) |
   | **rel=prefetch** | 预先加载可能马上会用到的资源(link)                   |
   | **src**          | 加载外部脚本文件(script)                             |
   | **async**        | 控制脚本的执行时机和执行方式：异步执行方式           |
   | **defer**        | 控制脚本的执行时机和执行方式：                       |

   ## 构筑基本文档结构

   ### 1. DOCTYPE

   1. 声明处理的是HTML
   2. 标记文档的版本号： HTML5;

   ### 2. html元素

   1. html根元素；

   2. manifest属性： 详见离线缓存Web应用程序

   3. 默认样式： 

      ```css
      html {
        display: block;
      }
      html:focus {
        outline: none;
      }
      ```

   ### 3. head元素

   1. 默认样式： 无

   ### 4. body元素

   1. 默认样式： 

      ```css
      body {
        display: block;
          margin: 8px;
      }
      body:focus {
        outline: none;
      }
      ```

   ## 元数据元素说明文档

   ### 1. 设置文档标题

   1. 默认样式： 

      ```css
      title { display: none; }
      ```

   ### 2. 用元数据说明文档

   1. meta元素，指定名/值定义元数据，为此要用到name和content属性

      ```html
   <!DOCTYPE html>
      <html lang="en">
     <head>
          <meta charset="UTF-8" />
          <meta name="viewport" content="width=device-width, initial-scale=1.0" />
          <title>Demo of meta</title>
          <base href="https://www.apple.com.cn/" />
          <meta name="author" content="Adam Freeman">
          <meta name="description" content="A simple example">
     </head>
        <body>
          <p>I like <code id="applecode">apples</code> and oranges.</p>
          <a href="ipad/" target="_top">IPad</a>
        </body>
      </html>
      ```
   
   2. 预定义元素类型
   
      | 元数据名称       | 说明                             |
      | ---------------- | -------------------------------- |
      | application name | 当前页所属Web应用系统的名称      |
      | author           | 当前页的作者名                   |
      | description      | 当前页的说明                     |
      | generation       | 用来生成HTML的软件名称           |
   | keywords         | 用来描述页面的字符串，以逗号分隔 |
   
3. 三个元数据类型值： 
   
      - noindex：表示不要搜索本页
      - noarchive：表示不要将本页存档或缓存
      - nofollow：表示不要继续顺着本页中的链接继续搜索下去
   
      ```html
      <meta name="robots" content="noindex">
      <meta name="robots" content="noarchive">
      <meta name="robots" content="noarchive">
      ```
   
   4. charset属性： 声明HTML文档内容所用的字符编码；
   
   5. UTF-8字符： 能以最少的字节数表示Unicode字符；
   
   ```html 
      <meta name="charset" content="utf-8">
   <meta http-equiv="content-type" content="text/html charset=UTF-8">
      ```
   
   6. 模拟HTTP表头字段： 改写HTTP(超文本传输协议)标头字段的值，服务器和浏览器之间传输HTML数据时，一般都用的就是HTTP
   
      ```html
      <meta http-equiv="refresh" content="5">
      <meta http-equiv="refresh" content="5; http://www.apress.com">
      ```
   
   7. meta元素的http-equiv属性允许使用的值
   
      | 属性值        | 说明                                                         |
      | ------------- | ------------------------------------------------------------ |
      | refresh       | 以秒为单位指定一个时间间隔，在此时间过去后将重新从服务器加载该页面 |
      | default-style | 指定页面优先使用的样式表，对应的content属性，应该与同一文档中的某个style元素或者link元素的style属性值相同 |
   | content-type  | 另一种声明HTML页面所使用字符编码的方法，详见charset          |
   
### 3. 定义CSS样式
   
   1. style元素：用来定义HTML文档内嵌样式；
   
   2. 允许具有的父元素： 任何包含元数据元素的元素，head，div，noscript，section，article，aside，type，media，scoped
   
   3. 可以出现在html文档的任何部分
   
   4. 一个文档可以有多个style
   
   5. type属性： 规定了所定义的样式类型，其值为 text/css；
   
   6. scoped属性： 规定CSS样式的作用范围；
   
   7. media属性： 指定样式的适用媒体
   
   ```html
      <!DOCTYPE html>
   <html lang="en">
        <head>
       <meta charset="UTF-8" />
          <meta name="viewport" content="width=device-width, initial-scale=1.0" />
          <title>Demo of style</title>
          <style media="screen" type="text/css">
            a {
              background: gray;
              color: white;
              padding: 0.5em;
              text-decoration: none; 
            }
          </style>
            
         <style media="print">
            a {
              color: red;
              font-weight: bold;
              font-style: italic;
            }
       </style>
        </head>
     <body>
          <p>I like <code id="applecode">apples</code> and oranges.</p>
          <a href="ipad/" target="_top">IPad I love</a>
        </body>
      </html>
      ```
   
   ### 4. 指定外部资源

   1. link元素： 元素类型，元数据；

   2. 允许具有的父级元素： head，noscript
   
   3. 局部属性： href，rel，hreflang，media，type，sizes

      | 属性         | 说明                                                   |
      | ------------ | ------------------------------------------------------ |
      | **href**     | 指定link元素指向资源的URL                              |
      | **hreflang** | 说明所关联的资源的语言                                 |
      | **media**    | 说明所关联的内容用于哪种设备, 参见type和http-equiv属性 |
   | **rel**      | 说明文档与所关联资源的关系类型,                        |
      | **sizes**    | 指定图标的大小                                         |
   | **type**     | 指定所关联资源的MIME类型，如： text/css ，image/x-ico  |
   
#### 4.1 用于载入外部样式表
   
   #### 4.2 用于定义网页标志: favicon.ico
   
   #### 4.3 预先获取资源

   ```html
<!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of rel</title>
       <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
    <link rel="stylesheet" href="css/indec.css" />
       <link rel="prefetch" href="/products.html" />
     </head>
     <body>
       <p>I like <code id="applecode">apples</code> and oranges.</p>
       <a href="products.html" target="_blank">Products Page</a>
  </body>
   </html>
```
   
## 使用脚本元素
   
### 1. script元素
   
1. 数据类型： 元数据、短语
   
2. 允许具有的父级元素： 任何包含元数据元素或者短语元素的元素
   
3. 局部属性： type，src，defer，async，charset
   
   | 属性        | 说明                                                         |
      | ----------- | ------------------------------------------------------------ |
   | **type**    | 表示所引用或定义的脚本类型，对于JavaScript脚本可以省略       |
      | **src**     | 指定外部脚本的URL                                            |
      | **defer**   | 指定脚本执行方式，必须在文档，Image及link全部加载，并且解析后再加载本脚本 |
      | **async**   | 指定脚本执行方式，异步执行方式                               |
      | **charset** | 说明外部脚本文件所使用的字符编码                             |
   
   #### 1.1 文档内嵌脚本
   
   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Demo of script</title>
       <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
     </head>
     <body>
       <p>I like <code id="applecode">apples</code> and oranges.</p>
       <a href="ipad/" target="_self">IPad</a>
       <script>
         let p = document.querySelector("p");
         p.style.width = "400px";
         p.style.height = "20px";
         p.style.background = "green";
         p.style.color = "white";
         p.style.padding = "10px";
       </script>
     </body>
   </html>
   ```

   #### 1.2 文档外部脚本

   ```html
<!DOCTYPE html>
   <html lang="en">
  <head>
       <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Demo of rel</title>
       <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
     </head>
     <body>
       <p>I like <code id="applecode">apples</code> and oranges.</p>
       <a href="ipad/" target="_self">IPad</a>
       <script src="js/05-index.js"></script>
     </body>
</html>
   ```

   #### 1.3 脚本的defer属性

   ```html
<!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Demo of rel</title>
       <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
       <script src="js/05-index.js" defer></script>
     </head>
     <body>
       <p>I like <code id="applecode">apples</code> and oranges.</p>
       <a href="ipad/" target="_self">IPad</a>
     </body>
   </html>
   ```
   
   #### 1.4 异步执行脚本
   
```html
   <!DOCTYPE html>
<html lang="en">
     <head>
    <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of rel</title>
       <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
    <script src="js/05-index.js" async></script>
     </head>
  <body>
       <p>I like <code id="applecode">apples</code> and oranges.</p>
       <a href="ipad/" target="_self">IPad</a>
     </body>
   </html>
   ```
   
   ### 2. noscript元素

   1. 用来向禁用了的JavaScript脚本或者浏览器不支持JavaScript的用户显示一些内容

    ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Demo of rel</title>
       <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
     </head>
     <body>
       <noscript>
         <h1>JavaScript is Required</h1>
         <p>You can not use this page without JavaScript</p>
       </noscript>
       <p>I like <code id="applecode">apples</code> and oranges.</p>
       <a href="ipad/" target="_self">IPad</a>
     </body>
   </html>
    ```
   
   