# 第四章 初探 CSS

## 1. 定义和应用样式

1. CSS样式： 一条或多条以分号分隔的样式声明组成；

### 1.1 初始CSS样式

| 样式(style)         | 说明(description)                         |
| ------------------- | ----------------------------------------- |
| **width**           | 设置元素宽度                              |
| **height**          | 设置元素高度                              |
| **margin**          | 设置元素外边距： 元素与元素之间的距离     |
| **padding**         | 设置元素内边距： 元素内容与边框之间的距离 |
| **text-align**      | 设置元素水平居中对齐                      |
| **line-height**     | 设置元素垂直对齐方式                      |
| **background**      | 设置元素背景颜色                          |
| **color**           | 设置元素文本颜色                          |
| **border**          | 设置元素边框                              |
| **text-decoration** | 设置元素文字的装饰效果                    |

### 1.2 元素的内嵌样式

1. 又称为元素行内样式
2. 用全局属性style定义样式

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>元素的行内样式</title>
</head>
<body>
	<a href="http://apress.com" style="background-color: grey;color: white;">
		Visit the Apress websit
	</a>
	<p>I like <span>apples</span> and oranges</p>
	<a href="https:/baidu.com">Visit the Baidu Website</a>
</body>
</html>
```

### 1.3 文档的内嵌样式

1. 又称为文档内联样式

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>文档内联样式</title>
	<style>
		a {
			background-color: grey;
			color: white;
		}
        span {
			border: thin solid black;
			padding: 10px;
		}
	</style>
</head>
<body>
	<a href="http://apress.com">
		Visit the Apress websit
	</a>
	<p>I like <span>apples</span> and oranges</p>
	<a href="https:/baidu.com">Visit the Baidu Website</a>
</body>
</html>
```

### 1.4 外联样式表

- 03-外联样式.html

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>文档内联样式</title>
	<link rel="stylesheet" href="css/index.css">
</head>
<body>
	<a href="http://apress.com">
		Visit the Apress websit
	</a>
	<p>I like <span>apples</span> and oranges</p>
	<a href="https:/baidu.com">Visit the Baidu Website</a>
</body>
</html>
```

- index.css

```css
a {
	background-color: grey;
	color: white;
}
span {
	border: thin solid black;
	padding: 10px;
}
```

## 2. 样式的层叠和继承

### 2.1 浏览器样式

1. 浏览器样式，就是默认样式，根据浏览器的不同，展现的样式了有不同；

2. ul默认样式

   ```html
   <!DOCTYPE html>
   <html lang="zh">
   <head>
   	<meta charset="UTF-8">
   	<meta name="viewport" content="width=device-width, initial-scale=1.0">
   	<meta http-equiv="X-UA-Compatible" content="ie=edge">
   	<title>ul的默认样式</title>
   </head>
   <body>
   	<ul>
   		<li>落霞与孤鹜齐飞 秋水共长天一色</li>
   		<li>渔舟晚唱 响穷彭蠡之滨 雁阵惊寒 声断衡阳之浦</li>
   		<li>海内存知己 天涯若比邻个</li>
   		<li>大漠孤烟直 长河落日圆</li>
   		<li>飞流直下三千尺 凝是银河落九天</li>
   		<li>桃花潭水深千尺 不及汪伦送我情</li>
   		<li>疏影横斜水清浅 暗香浮动月黄昏</li>
   		<li>幽独空林色 朱蕤冒紫茎</li>
   		<li>晴川历历汉阳树 芳草萋萋鹦鹉洲</li>
   	</ul>
   </body>
   </html>
   ```

3. ol默认样式

   ```html
   <!DOCTYPE html>
   <html lang="zh">
   <head>
   	<meta charset="UTF-8">
   	<meta name="viewport" content="width=device-width, initial-scale=1.0">
   	<meta http-equiv="X-UA-Compatible" content="ie=edge">
   	<title>ol默认样式</title>
   </head>
   <body>
   	<ol>
   		<li>落霞与孤鹜齐飞 秋水共长天一色</li>
   		<li>渔舟晚唱 响穷彭蠡之滨 雁阵惊寒 声断衡阳之浦</li>
   		<li>海内存知己 天涯若比邻个</li>
   		<li>大漠孤烟直 长河落日圆</li>
   		<li>飞流直下三千尺 凝是银河落九天</li>
   		<li>桃花潭水深千尺 不及汪伦送我情</li>
   		<li>疏影横斜水清浅 暗香浮动月黄昏</li>
   		<li>幽独空林色 朱蕤冒紫茎</li>
   		<li>晴川历历汉阳树 芳草萋萋鹦鹉洲</li>
   	</ol>
   </body>
   </html>
   ```

### 2.2 用户样式

1. a 用户样式

   ```html
   <!DOCTYPE html>
   <html lang="zh">
   <head>
   	<meta charset="UTF-8">
   	<meta name="viewport" content="width=device-width, initial-scale=1.0">
   	<meta http-equiv="X-UA-Compatible" content="ie=edge">
   	<title>用户样式</title>
   	<style>
   		/* 默认样式 */
   		/* a {
   			color: blue;
   			text-decoration: underline;
   		} */
   		/* 用户样式 */
   		a {
   			color: white;
   			background: grey;
   			text-decoration: none;
   			padding: 2px;
   		}
   	</style>
   </head>
   <body>
   	<a href="http://apress.com" style="background-color: grey;color: white;">
   		Visit the Apress websit
   	</a>
   	<p>I like <span>apples</span> and oranges</p>
   	<a href="https:/baidu.com">Visit the Baidu Website</a>
   </body>
   </html>
   ```

2. ol用户样式

   ```html
   <!DOCTYPE html>
   <html lang="zh">
   <head>
   	<meta charset="UTF-8">
   	<meta name="viewport" content="width=device-width, initial-scale=1.0">
   	<meta http-equiv="X-UA-Compatible" content="ie=edge">
   	<title>ol默认样式</title>
   	<style>
   		ol {
   			padding: 0;
   			margin: 0;
   		}
   	</style>
   </head>
   <body>
   	<ol>
   		<li>落霞与孤鹜齐飞 秋水共长天一色</li>
   		<li>渔舟晚唱 响穷彭蠡之滨 雁阵惊寒 声断衡阳之浦</li>
   		<li>海内存知己 天涯若比邻个</li>
   		<li>大漠孤烟直 长河落日圆</li>
   		<li>飞流直下三千尺 凝是银河落九天</li>
   		<li>桃花潭水深千尺 不及汪伦送我情</li>
   		<li>疏影横斜水清浅 暗香浮动月黄昏</li>
   		<li>幽独空林色 朱蕤冒紫茎</li>
   		<li>晴川历历汉阳树 芳草萋萋鹦鹉洲</li>
   	</ol>
   </body>
   </html>
   ```

3. ul用户样式

   ```html
   <!DOCTYPE html>
   <html lang="zh">
   <head>
   	<meta charset="UTF-8">
   	<meta name="viewport" content="width=device-width, initial-scale=1.0">
   	<meta http-equiv="X-UA-Compatible" content="ie=edge">
   	<title>ul的默认样式</title>
   	<style>
   		ul {
   			display: block;
   			list-style: none;
   			margin: 0;
   			padding: 0;
   		}
   	</style>
   </head>
   <body>
   	<ul>
   		<li>落霞与孤鹜齐飞 秋水共长天一色</li>
   		<li>渔舟晚唱 响穷彭蠡之滨 雁阵惊寒 声断衡阳之浦</li>
   		<li>海内存知己 天涯若比邻个</li>
   		<li>大漠孤烟直 长河落日圆</li>
   		<li>飞流直下三千尺 凝是银河落九天</li>
   		<li>桃花潭水深千尺 不及汪伦送我情</li>
   		<li>疏影横斜水清浅 暗香浮动月黄昏</li>
   		<li>幽独空林色 朱蕤冒紫茎</li>
   		<li>晴川历历汉阳树 芳草萋萋鹦鹉洲</li>
   	</ul>
   </body>
   </html>
   ```

### 2.3 样式的层叠

#### 2.3.1 浏览器显示样式的优先顺序

1. 元素的内嵌样式： 行内样式
2. 文档的内联样式
3. 外部样式
4. 用户样式
5. 浏览器样式

#### example

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>样式的优先级顺序</title>
	<link rel="stylesheet" href="css/04-index.css">
	<style>
		.post {
			color: green;
		}
	</style>
</head>
<body>
	<ul>
		<li class="post first" style="color: red">落霞与孤鹜齐飞 秋水共长天一色</li>
		<li class="post second" style="color: red">渔舟晚唱 响穷彭蠡之滨 雁阵惊寒 声断衡阳之浦</li>
		<li class="post third" style="color: red">海内存知己 天涯若比邻个</li>
		<li class="post fourth">大漠孤烟直 长河落日圆</li>
		<li class="post fifth">飞流直下三千尺 凝是银河落九天</li>
		<li class="post sixth">桃花潭水深千尺 不及汪伦送我情</li>
		<li class="post seventh">疏影横斜水清浅 暗香浮动月黄昏</li>
		<li class="post eighth">幽独空林色 朱蕤冒紫茎</li>
		<li class="post ninth">晴川历历汉阳树 芳草萋萋鹦鹉洲</li>
	</ul>
</body>
</html>
```

#### 04-index.css

```css
.first {
	color: yellow;
}
.post {
	color: yellow;
}
.second {
	color: yellow !important;
}
.third {
	color: yellow;
}
```

#### 2.3.2 用重要样式调整层叠顺序

1. 通过在样式中添加!important改变层叠次序，贵高优先级；

```css
.second {
	color: yellow !important;
}
```

#### 2.3.3 同级样式冲突的解决

当同级样式发生冲突时，样式的呈现要根据以下原则解决冲突：

1. 选择器中的id值得数目；
2. 选择器中其他属性和伪类的数目；
3. 选择器中元素名和伪元素的数目；
4. 这些规则将选择器样式分为三个级别，根据三个级别形成类似“a-b-c"的层级关系：
   - 优先比较a层级中id的样式数量，哪种样式的数量多，就呈现该样式；
   - 当a层级样式数目相同时，就开始比较b层级的样式数量；
   - 根据b级别的其他属性和伪类的数量，哪种样式的数量多，就呈现该样式；
   - 如果b层级样式数量相同时，就开始比较层级的样式数量，以此类推；
5.  

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>样式的优先级顺序</title>
	<style>
		#second, #post {
			color: yellow;
		}
		li#post {
			color: darkcyan;
		}
		.post {
			color: green;
		} 
		.first, .second,.forth,.one, .two,.four{
			color: red;
		}
		li:nth-child(6){
			color: blue;
		}
		/* 层叠 post的样式 */
		.fifth,.sixth,.seventh {
			color: purple;
		}
		li.seven {
			color: green;
		}
	</style>
</head>
<body>
	<ul>
		<li class="post first one">落霞与孤鹜齐飞 秋水共长天一色</li>
		<li class="post second two" id="second">渔舟晚唱 响穷彭蠡之滨 雁阵惊寒 声断衡阳之浦</li>
		<li class="post third" id="post">海内存知己 天涯若比邻个</li>
		<li class="post fourth four">大漠孤烟直 长河落日圆</li>
		<li class="post fifth">飞流直下三千尺 凝是银河落九天</li>
		<li class="post sixth">桃花潭水深千尺 不及汪伦送我情</li>
		<li class="post seventh seven">疏影横斜水清浅 暗香浮动月黄昏</li>
		<li>幽独空林色 朱蕤冒紫茎</li>
		<li>晴川历历汉阳树 芳草萋萋鹦鹉洲</li>
	</ul>
</body>
</html>
```

### 2.4 样式的继承

1. 什么继承： 浏览器在直接样式中找不到某个属性值，就会求助继承机制，使用父元素的样式属性值；
2. 并不是所有样式都会被继承；
3. 与文字相关的属性： 文字颜色、字体等将被继承；
4. 与元素在布局相关的样式不会被继承；
5. 若要对样式使用强制继承，请使用`inherit`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS 样式的继承</title>
    <style>
      p {
        color: red;
        background: #aaa;
        font-size: 28px;
        border: 1px solid black;
      }
        span {
           border: inherit;
        }
    </style>
  </head>
  <body>
    <a href="http://apress.com" style="background-color: grey; color: white;">
      Visit the Apress websit
    </a>
    <p>I like <span>apples</span> and oranges</p>
    <a href="https:/baidu.com">Visit the Baidu Website</a>
  </body>
</html>
```

## 3. CSS中的颜色

1. CSS中颜色的表示方法有四种

   - 英文单词表示颜色
   - 十六进制表示颜色
     - 十六进制颜色的组成部分是：＃RRGGBB，其中RR（红色），GG（绿色）和BB（蓝色），所有值都必须介于00和FF之间；
   - RGB表示颜色： 十进制表示法
     - RGB写法：rgb（0,0,0），它的取值范围都在0-255之间，值越大越颜色越深；
     - RGB除了可以用数值以外，它还可以用百分百，取值在0%到100%之间；
     - 比如：RGB（0,0,255）和RGB（0％，0％，100％）表示的是同一种颜色；
     - RGBA： 是RGB外加了一个透明度之α值；取值范围： 0-1之间
   - HSL表示颜色： 
     - HSL颜色值分别代表：色相(**hue**)，饱和度(**saturation**)，亮度(lightness)；
     - 色相是在色轮上的程度（从0到360）；
     - -0（或360）是红色的，120是绿色的，240是蓝色的；
     - 饱和度是一个百分比值，0％意味着灰色和100％的阴影是全彩；
     - 亮度也是一个百分比，0％是黑色的，100％是白色的；
     - HSLA： 是HSL外加了一个透明度之α值；

   | 颜色名称  | 十六进制表示 | RGB         | HSL  |
   | --------- | ------------ | ----------- | ---- |
   | black     | #000000      | 0,0,0       |      |
   | white     | #FFFFFF      | 255,255,255 |      |
   | silver    | #C0C0C0      | 192,192,192 |      |
   | gray      | #808080      | 128,128,128 |      |
   | maroon    | #800000      | 128,0,0     |      |
   | red       | #FF0000      | 255,0,0     |      |
   | purple    | #80080       | 128,0,128   |      |
   | fushia    | #FF00FF      | 255,0,255   |      |
   | green     | #008000      | 0,128,0     |      |
   | lime      | #00FF00      | 0,255,0     |      |
   | olive     | #808000      | 128,128,0   |      |
   | yellow    | #FFFF00      | 255,255,0   |      |
   | navy      | #000080      | 0,0,128     |      |
   | blue      | #0000FF      | 0,0,128     |      |
   | teal      | #008080      | 0,128,128   |      |
   | aqua      | #00FFFF      | 0,255,255   |      |
   | darkgray  | #A9A9A9      | 169,169,169 |      |
   | gray      | #808080      | 128,128,128 |      |
   | dimgray   | #696969      | 105,105,105 |      |
   | lightgray | #D3D3D3      | 211,211,211 |      |

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS 的颜色</title>
    <style>
      div {
        width: 200px;
        height: 200px;
        margin: 10px;
        float: left;
      }
      .one {
        background: red;
      }
      .two {
        background: #00ff00;
      }
      .three {
        background: rgba(0, 0, 0, 0.5);
      }
      .four {
        background: hsla(120, 100%, 50%, 0.8);
      }
    </style>
  </head>
  <body>
    <div class="one"></div>
    <div class="two"></div>
    <div class="three"></div>
    <div class="four"></div>
  </body>
</html>
```

## 4. CSS中的长度

1. 绝对长度： cm（厘米），pt （磅）
2. 相对单位： 
   - 与元素字号挂钩的单位： em;
   - 与元素字体x高度挂钩的单位： ex， 即字体基线到中线之间的距离，通常 1 ex = 0.5em;
   - 与根元素(html元素)挂钩的单位： rem;
   - 与像素挂钩的单位： px；
   - 与元素属性的值得百分比挂钩的单位： %;

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS 的颜色</title>
    <style>
      body {
        height: 100vh;
      }
      .container {
        width: 80%;
        height: 80%;
        background: #690;
      }
      div {
        margin: 10px;
        float: left;
      }
      .one {
        width: 200px;
        height: 200px;
        background: red;
      }
      .two {
        width: 10em;
        height: 10em;
        font-size: 2rem;
        background: #00ff00;
      }
      .three {
        width: 10rem;
        height: 10rem;
        background: rgba(0, 0, 0, 0.5);
      }
      .four {
        background: hsla(120, 100%, 50%, 0.8);
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="one"></div>
      <div class="two">Hello</div>
      <div class="three"></div>
      <div class="four"></div>
    </div>
  </body>
</html>
```

## 5. 其他CSS单位

### 5.1  计算单位：

```css
p { width: calc(80% -20px)}
```

### 5. 2 角度

| 单位标识符 | 说明                       |
| ---------- | -------------------------- |
| deg        | 角度： 取值 0 ~ 360 deg    |
| grad       | 百分度： 取值 0 ~  400grad |
| rag        | 弧度： 取值 0rad ~ 6.28rad |
| turn       | 圆周： 1turn = 360 deg     |

### 5.3 时间

| 单位标识符 | 说明               |
| ---------- | ------------------ |
| s          | 秒： 1s = 1000ms   |
| ms         | 毫秒： 1000ms = 1s |

## 6. 测试CSS特性的支持情况

1. 测试工具一： https://caniuse.com/
2. 测试工具二：https://modernizr.com/

## 7. 有用的CSS工具

1. chrome开发工具
2. SelectorGadget生成选择器： https://selectorgadget.com/
3. CSS预编译工具： Sass、 Less、 Stylus
