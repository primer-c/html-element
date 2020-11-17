# input元素属性

## input属性

| 属性            | 说明                                |
| --------------- | ----------------------------------- |
| **type**        | input类型                           |
| **placeholder** | input初始值，或者相关数据的提示信息 |
| **disabled**    | 提示input禁用                       |
| **readonly**    | 提示input只读                       |
| **maxlength**   | input容量                           |
| **size**        | input元素的大小                     |
| **name**        | 提示input名称                       |
| **value**       | input的初始值                       |
| **enctype**     | 指定input元素的编码                 |

## Type属性

| 属性值             | 说明               |
| ------------------ | ------------------ |
| **text**           | type为文本         |
| **password**       | type为密码         |
| **submit**         | type为提交按钮     |
| **reset**          | type为重置按钮     |
| **button**         | type为普通按钮     |
| **number**         | type为数字         |
| **email**          | type为邮件         |
| **tel**            | type为电话         |
| **url**            | type为URL          |
| **radio**          | type为单选框       |
| **checkbox**       | type为多选框       |
| **search**         | type为搜索框       |
| **color**          | type为颜色         |
| **range**          | type为范围         |
| **hidden**         | type为隐藏         |
| **image**          | type为图像         |
| **file**           | type为文件         |
| **datetime**       | type限定为时间     |
| **datatime-local** | type限定为当地时间 |
| **time**           | type限定为时间     |
| **date**           | type限定为时间     |
| **month**          | type限定为月       |
| **week**           | type限定为星期     |

## 用input元素输入文字

#### text型input元素可用的额外其它属性

| 属性            | 说明                                                         |
| --------------- | ------------------------------------------------------------ |
| **dirname**     | 指定元素内容文字方向的名字                                   |
| **list**        | 指定为文本框提供建议值的datalist元素，其值为datalist元素的id值 |
| **maxlength**   | 指定文本框中输入的字符最大数                                 |
| **pattern**     | 指定一个用于输入验证的正则表达式                             |
| **placeholder** | 指定关于所需数据信息的提示                                   |
| **readonly**    | 用于将文本框设置为只读，禁止用户编辑内容                     |
| **required**    | 表示用户必须输入一个值，否者无法通过验证                     |
| **size**        | 指定文本框中可见的字符数目                                   |
| **value**       | 设置文本框的初始值                                           |

### 1. size: 设定文本框显示的字符数目

### 2. maxlength 设置用户能够输入字符串的最大数目

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type size</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input type="text" name="name" id="name" size="10" maxlength="10" /><br />
      <label for="city">City:</label>
      <input type="text" name="cite" id="city" size="10" /><br />
      <label for="fave">Fruit:</label>
      <input type="text" maxlength="10" size="10" name="fave" id="fave" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 3. value： 设定元素的初始值

```html
<input type="password" value="password" name="password"/>
```

### 4. placeholder： 占位符，提示用户输入的数据类型

```html
<input type="username" value="username" name="username" placeholder="andy@gmail.com"/>
```

### 4. list: datalist元素的id属性值

#### 4.1 datalist元素： 

1. 提供一批值，以便用户输入需要的数据
2. 允许具有的父级元素： 任何可以包含短语元素的元素
3. 子元素： option

#### 4.2 option

1. 允许具有的父级元素： datalist，select，optgroup
2. 局部属性： disabled，selected，label， value

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of datalist and option</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form method="post" action="http://titan.com/form">
      <label for="name">Name:</label>
      <input
        type="text"
        name="name"
        value="name"
        id="name"
        placeholder="Your name"
      /><br />
      <label for="city">City:</label>
      <input
        type="text"
        name="city"
        value="city"
        id="city"
        placeholder="Where you live"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" list="fruitlist" id="fave" name="fave" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
    <datalist id="fruitlist">
      <option value="Apples" label="Lovely Apples" />
      <option value="Oranges">Refreshing Oranges</option>
      <option value="Cherries" />
    </datalist>
  </body>
</html>
```

### 5. readonly: 表示只读文本框

### 6. disabled： 表示不可编辑文本框

##### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of datalist and option</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form method="post" action="http://titan.com/form">
      <label for="name">Name:</label>
      <input type="text" name="name" value="Andy" id="name" disabled /><br />
      <label for="city">City:</label>
      <input type="text" name="city" value="Boston" id="city" readonly /><br />
      <label for="fave">Fruit:</label>
      <input type="text" id="fave" name="fave" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 7. dirname: 将用户输入文字的方向数据发送给服务器

## 用input元素输入密码

#### password型input元素可以使用的额外属性

| 属性            | 说明                                     |
| --------------- | ---------------------------------------- |
| **maxlength**   | 指定文本框中输入的字符最大数             |
| **pattern**     | 指定一个用于输入验证的正则表达式         |
| **placeholder** | 指定关于所需数据信息的提示               |
| **readonly**    | 用于将文本框设置为只读，禁止用户编辑内容 |
| **required**    | 表示用户必须输入一个值，否者无法通过验证 |
| **size**        | 指定文本框中可见的字符数目               |
| **value**       | 设置文本框的初始值                       |

#### example 

略

## 用input元素生成按钮

### submit类型的按钮： 提交按钮

### reset类型按钮： 重置按钮

### button类型按钮： 普通按钮

## 用input元素输入数据把关

| 属性值             | 说明               |
| ------------------ | ------------------ |
| **number**         | type为数字         |
| **email**          | type为邮件         |
| **tel**            | type为电话         |
| **url**            | type为URL          |
| **radio**          | type为单选框       |
| **checkbox**       | type为多选框       |
| **color**          | type为颜色         |
| **range**          | type为范围         |
| **datetime**       | type限定为时间     |
| **datatime-local** | type限定为当地时间 |
| **time**           | type限定为时间     |
| **date**           | type限定为时间     |
| **month**          | type限定为月       |
| **week**           | type限定为星期     |

### 1. number属性值： 获取数值

#### number属性值元素可用的额外属性

| 属性         | 说明                                                         |
| ------------ | ------------------------------------------------------------ |
| **list**     | 指定为文本框提供建议值的datalist元素，其值为datalist元素的id值 |
| **min**      | 指定一个用于输入验证的正则表达式                             |
| **max**      | 指定关于所需数据信息的提示                                   |
| **readonly** | 用于将文本框设置为只读，禁止用户编辑内容                     |
| **required** | 表示用户必须输入一个值，否者无法通过验证                     |
| **step**     | 指定上下调节数值的步长                                       |
| **value**    | 设置文本框的初始值                                           |

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type size</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input type="text" name="Andy" id="name" /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="Apples" /><br />
      <label for="price">$ per unit in your area:</label>
      <input
        type="number"
        name="price"
        id="price"
        min="0"
        max="100"
        step="1"
        value="1"
      /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 2. range属性值： 获取指定范围的数值

### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type range</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input type="text" name="Andy" id="name" /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="Apples" /><br />
      <label for="price">$ per unit in your area:</label>
      <input
        type="range"
        name="price"
        id="price"
        min="0"
        max="100"
        step="1"
        value="1"
      /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 3. checkbox属性值： 多选布尔型输入

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type checkbox</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input type="text" name="Andy" id="name" /><br />
      <h4>My Favorite Fruit</h4>
      <label for="apple">Apple:</label>
      <input type="checkbox" name="apple" id="apple" value="apple" /><br />
      <label for="orange">Orange:</label>
      <input type="checkbox" name="orange" id="orange" value="orange" /><br />
      <label for="cherry">Cherry:</label>
      <input type="checkbox" name="cherry" id="cherry" value="cherry" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 4. radio属性值： 单选项布尔型输入

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type checkbox</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input type="text" name="Andy" id="name" /><br />
      <fieldset>
        <legend>Your Gender</legend>
        <label for="male">Male:</label>
        <input type="radio" checked name="male" id="male" value="male" /><br />
        <label for="female">Female:</label>
        <input type="radio" name="female" id="female" value="female" /><br />
      </fieldset>
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 5.用input元素获取有规定格式的字符串

| 属性            | 说明                                                         |
| --------------- | ------------------------------------------------------------ |
| **list**        | 指定为文本框提供建议值的datalist元素，其值为datalist元素的id值 |
| **maxlength**   | 指定文本框中输入的字符最大数                                 |
| **pattern**     | 指定一个用于输入验证的正则表达式                             |
| **placeholder** | 指定关于所需数据信息的提示                                   |
| **readonly**    | 用于将文本框设置为只读，禁止用户编辑内容                     |
| **required**    | 表示用户必须输入一个值，否者无法通过验证                     |
| **size**        | 指定文本框中可见的字符数目                                   |
| **value**       | 设置文本框的初始值                                           |

#### 5.1 email属性值: 输入邮箱

#### 5.2 tel属性值： 输入电话

#### 5.3 url属性值：输入URL

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type checkbox</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="email">Email:</label>
      <input
        type="email"
        name="email"
        id="email"
        value="email"
        placeholder="user@gmail.com"
      /><br />
      <label for="tel">Telephone:</label>
      <input
        type="tel"
        name="tel"
        id="tel"
        placeholder="(086)-010-8868"
      /><br />
      <label for="url">URL:</label>
      <input type="url" id="url" name="url" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 6. 用input元素获取时间和日期

| 属性         | 说明                                                         |
| ------------ | ------------------------------------------------------------ |
| **list**     | 指定为文本框提供建议值的datalist元素，其值为datalist元素的id值 |
| **min**      | 指定一个用于输入验证的正则表达式                             |
| **max**      | 指定关于所需数据信息的提示                                   |
| **readonly** | 用于将文本框设置为只读，禁止用户编辑内容                     |
| **required** | 表示用户必须输入一个值，否者无法通过验证                     |
| **step**     | 指定上下调节数值的步长                                       |
| **value**    | 设置文本框的初始值                                           |

#### 6.1 datetime属性值： 获取世界时日期，时间

#### 6.2 datetime-local属性值： 获取本地日期，时间

#### 6.3 date属性值：获取本地日期

#### 6.4 month属性值： 获取本地年月信息

#### 6.5 time属性值： 获取本地时间

#### 6.6 week属性值： 获取本地星期

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type checkbox</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="apples" /><br />
      <label for="lastby">When did you last buy:</label>
      <input type="date" name="lastby" id="lastby" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 7. 用input元素获取颜色

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type color</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="apples" /><br />
      <label for="color">Color:</label>
      <input type="color" name="color" id="color" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 8. search： 获取搜索关键词

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type search</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="apples" /><br />
      <label for="search">Search:</label>
      <input type="search" name="search" id="search" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 9. hidden： 生成隐藏数据项

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type hidden</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <input type="hidden" name="recodeID" value="123456" />
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="apples" /><br />
      <label for="search">Search:</label>
      <input type="search" name="search" id="search" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

### 10. image: 生成图像按钮和分区相应图

| 属性               | 说明                                                         |
| ------------------ | ------------------------------------------------------------ |
| **alt**            | 指定元素的说明文字                                           |
| **formaction**     | 覆盖**form****元素的**action**属性，另行指定表单的URL        |
| **formenctype**    | 覆盖**form****元素的**enctype**属性，另行指定表单的编码方式  |
| **formmethod**     | 覆盖**form****元素的**method**属性，另行指定表单的提交方式   |
| **formtarget**     | 覆盖**form****元素的**target**属性，另行指定表单的**target** |
| **formnovalidate** | 覆盖**form****元素的**novalidateaction**属性，另行指定表单的**novalidate** |
| **height**         | 以像素为单位设置图像高度                                     |
| **width**          | 以像素为单位设置图像宽度                                     |
| **src**            | 指定要显示图像的URL                                          |

#### example 

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type image</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <input type="hidden" name="recodeID" value="123456" />
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="apples" /><br />
      <input
        type="image"
        name="submit"
        src="imgs/flower.gif"
        width="60px"
        height="60px"
      />
    </form>
  </body>
</html>
```

### 11. file： 上传文件

| 属性         | 说明                 |
| ------------ | -------------------- |
| **accept**   | 指定接受的MINE类型   |
| **multiple** | 指定可以上传多个文件 |
| **required** | 表示为必选项         |

#### example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Demo of input type file</title>
    <link rel="shortcut icon" href="imgs/favicon.ico" type="image/x-icon" />
  </head>
  <body>
    <form action="http://titan.com/form">
      <input type="hidden" name="recodeID" value="123456" />
      <label for="name">Name:</label>
      <input
        type="text"
        name="Andy"
        id="name"
        placeholder="Please insert your name"
      /><br />
      <label for="password">Password:</label>
      <input
        type="password"
        checked
        name="password"
        id="password"
        value="password"
        placeholder="Min 6 character"
      /><br />
      <label for="fave">Fruit:</label>
      <input type="text" name="fave" id="fave" value="apples" /><br />
      <label for="file">File:</label>
      <input type="file" name="filedata" id="file" /><br />
      <input type="submit" value="Submit Vote" />
    </form>
  </body>
</html>
```

