# JavaEE

## 基础



## GUI编程入门到游戏实战

## 一小时开发贪吃蛇游戏

## 网络编程实战讲解

## 多线程详解

## 注解与反射

## JavaSE阶段回顾总结

## JVM快速入门

## JUC并发编程

# 前端

## HTML5

## CSS

## JavaScript和jQuery

# 数据库

## MySQL

# JavaWeb

## HTML+CSS

#### 参考网站

W3school：https://www.w3school.com.cn/

MDN：https://developer.mozilla.org/zh-CN/

第一个html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

</body>
</html>
```

标签：

- 字符标签

  ```html
  <font color="red" face="宋体" size="3">我是字体标签</font><br/>
  ```

  ​	color：颜色	face：字体	size：大小

- 特殊字符

  &nbsp：空格

  &gt、&lt：大于号、小于号

  &copy：版权符号

- 标题标签

  ```html
  <h1 align="left">标题1</h1>
  ```

  align：对齐方式（left\center\right）

- 超链接标签

  ```html
  <a href="http://www.baidu.com" target="_blank">百度</a>
  ```

  href：跳转的目标地址

  target：跳转方式[_self（默认方式，当前页面跳转）	_blank（新窗口中打开）]

- 列表标签

  ```html
  <ul type="none">	<!--无序列表-->
      <li>张三</li>
      <li>赵四</li>
      <li>王五</li>
      <li>孙六</li>
  </ul>
  <ol>	<!--无有序列表-->
      <li>张三</li>
      <li>赵四</li>
      <li>王五</li>
      <li>孙六</li>
  </ol>
  <dl>	<!--自定义列表-->
  	<dt></dt>
  	<dd></dd>
  </dl>
  ```

  type：列表项前的符号（none：空白）

- 图片标签

  ```html
  <img src="img/yurisa.jpg" width="" height="" border="" alt="找不到">
  ```

  src：图片地址	width\height：宽高	border：边框宽度	alt：图片找不到时显示的内容

  JavaSE

  ​	相对路径：从工程名开始

  ​	绝对路径：盘符/目录/文件名

  web

  ​	相对路径：

  ​			.				当前文件所在的目录

  ​			..				当前文件所在的上一级目录

  ​			文件名		当前文件所在目录的文件，相当于./文件名

  ​	绝对路径：

  ​			http://ip:port/工程名/资源路径/文件名

- 表格标签

  ```html
  <table border="10" width="300" height="300" cellspacing="10">
      <tr>
          <td align="center"><b>1.1</b></td>
          <th>1.2</th>
          <td>1.3</td>
      </tr>
      <tr>
          <td>2.1</td>
          <td>2.2</td>
          <td>2.3</td>
      </tr>
      <tr>
          <td>3.1</td>
          <td>3.2</td>
          <td>3.3</td>
      </tr>
  </table>
  ```

  table：表格标签	tr：行标签	th：表头标签	td：单元格标签	b：加粗标签

  使用th，自动居中

  border：边框宽度	width\height：宽高	cellspacing：设置单元格间距

  align：在td中，单元格文本对齐方式；table中，表格在页面中的位置

  跨单元格应用

  ```html
  <table border="1" width="300" height="300" cellspacing="0">
      <tr>
          <td colspan="2">1.1</td>
          <td>1.3</td>
          <td>1.4</td>
          <td>1.5</td>
      </tr>
      <tr>
          <td rowspan="2">2.1</td>
          <td>2.2</td>
          <td>2.3</td>
          <td>2.4</td>
          <td>2.5</td>
      </tr>
      <tr>
          <td>3.2</td>
          <td>3.3</td>
          <td>3.4</td>
          <td>3.5</td>
      </tr>
      <tr>
          <td>4.1</td>
          <td>4.2</td>
          <td>4.3</td>
          <td colspan="2" rowspan="2">4.4</td>
      </tr>
      <tr>
          <td>5.1</td>
          <td>5.2</td>
          <td>5.3</td>
      </tr>
  </table>
  ```

  colspan：设置跨列		rowspan：设置跨行

  idea中快捷键，ctrl+x，（设置好需要跨行列之后，删除原本存在的多余的单元格）

- 框架标签

  ```html
  <iframe name="iframe" src="7.表格跨行跨列.html" width="400" height="300">
      <ul>
          <li>猜猜我是谁</li>
      </ul>
  </iframe>
  <a href="1.font.html" target="iframe">font标签</a>
  <a href="5.img.html" target="iframe">img标签</a>
  ```

  iframe和a两标签相结合使用

  ![image-20210113175802507](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210113175802507.png)

- 表单标签

  ```html
  <form>
      <table align="center">
          <tr>
              <td>用户名称：</td>
              <td><input type="text" value="用户名称"></td>
          </tr>
          <tr>
              <td>用户密码：</td>
              <td><input type="password" value="用户密码"><br></td>
          </tr>
          <tr>
              <td>用户邮箱：</td>
              <td><input type="text" value="用户邮箱"><br></td>
          </tr>
          <tr>
              <td>性别：</td>
              <td>男<input type="radio" name="sex" checked="checked"> 女<input type="radio" name="sex"><br></td>
          </tr>
          <tr>
              <td>兴趣爱好：</td>
              <td>java<input type="checkbox" checked="checked">C<input type="checkbox">C++<input type="checkbox"><br></td>
          </tr>
          <tr>
              <td>国籍：</td>
              <td>
                  <select>
                      <option>--请选择国籍--</option>
                      <option>漂亮国</option>
                      <option selected="selected">中国</option>
                      <option>韩国</option>
                      <option>日本</option>
                  </select><br>
              </td>
          </tr>
          <tr>
              <td>自我评价：</td>
              <td>
                  <textarea rows="10" cols="20">标签内才是默认值，不在属性中添加</textarea><br>
              </td>
          </tr>
          <tr>
              <td>
                  <input type="reset" value="按钮上的字"><br>
              </td>
              <td align="center">
                  <input  type="reset">
              </td>
          </tr>
  <!--        <tr>-->
  <!--            <td rowspan="2">-->
  <!--                <input type="file">-->
  <!--            </td>-->
  <!--            <td></td>-->
  <!--        </tr>-->
      </table>
  ```

  input标签，（value为默认值）

  type：

  ​	text单行文本	password密码

  ​	radio单选（需要使用相同的name属性表示同一组，checked属性值为”checked“表默认选中）

  ​	checkbox多选

  ​	reset重置	submit提交	button按钮	file文件上传域

  ​	hidden隐藏域（当需要发送些信息，但不需要给用户看到，如参数时使用）

  select、option标签实现复选

  textarea	（rows、cols行数、列数）

  ==将table和form标签一些使用，可以规范美观==

  form标签

  ​	action：设置提交的服务器地址

  ​	method：提交的方式，一般为get/post

  ​		get	不安全，会把值显示在地址栏中；当字符过多时，值不会全发过去

  ​		post	解决上述问题

  ​	需要在input标签中设置name、value属性，以便获取到正确的input中的值，和所选的值（需要将所选的选项值放在value中传递过去）

- div、span、p

  div	默认独占一行

  span	所占长度为数据本身的长度

  p	默认在段落的上方或下方各空出一行，如果有就不再空

- 

- CSS语法规则

  ```
  p{
  	font-size:20px;
  }
  ```

  p：选择器		font-size：属性		20px：值		一个选择器可有多个属性

- css + html使用方式一：在div中添加style属性

  ```html
  <body>
  <div style="border: 1px solid red;width: 100px;height: 100px;background-color: green;text-align: center">div标签</div>
  <span style="border: 1px solid red">span标签</span>
  <p style="border: 1px solid red">p标签</p>
  </body>
  ```

- css + html使用方式二：在head标签中添加style标签，定义

  ```html
  <!DOCTYPE html>
  <html lang="cn">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <!--style标签专门用来定义css样式-->
      <style type="text/css">
          div{
              border: 1px solid red;
          }
          span{
              border: 1px solid red;
          }
      </style>
  </head>
  <body>
  <div>div标签</div>
  <div>div标签</div>
  <div>div标签</div>
  <span>span标签</span>
  <p>p标签</p>
  </body>
  </html>
  ```

- css + html使用方式三：外部编写css文件，html文件中使用link导入使用（标签选择器）

  ```css
  div{
      border: 1px solid red;
  }
  span{
      border: 1px solid red;
  }
  ```

  

  ```html
  <!DOCTYPE html>
  <html lang="cn">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <!--link标签专门用来引入css样式-->
      <link rel="stylesheet" type="text/css" href="1.css"/>
  </head>
  <body>
  <div>div标签</div>
  <div>div标签</div>
  <div>div标签</div>
  <span>span标签</span>
  <p>p标签</p>
  </body>
  </html>
  ```

- css + html使用方式四，（id选择器）id属性使用

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>ID选择器</title>
      <style>
          #id001{
              color: blue;
              font-size: 20px;
              border: 1px solid yellow;
          }
          #id002{
              color: red;
              font-size: 30px;
              border: 5px blue dotted;
          }
      </style>
  </head>
  <body>
  <div id="id001">标签1</div>
  <div id="id002">标签2</div>
  </body>
  </html>
  ```

- css + html使用方式五（类型选择器），class属性使用

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>class类型选择器</title>
      <style type="text/css">
          .class01{
              color: blue;
              font-size: 30px;
              border: 1px solid yellow;
          }
          .class02{
              color: grey;
              font-size: 26px;
              border: 1px solid yellow;
          }
      </style>
  </head>
  <body>
  <div class="class01">div标签1</div>
  <div class="class02">div标签2</div>
  <div class="class03">div标签3</div>
  </body>
  </html>
  ```

- css + html使用方式六（组合选择器）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>组合选择器</title>
      <style type="text/css">
          .class01,#id01{
              color: blue;
              font-size: 20px;
              border: 1px solid yellow;
          }
      </style>
  </head>
  <body>
  <div class="class01">div标签1</div>
  <span id="id01">span标签</span>
  <div class="class02">div标签2</div>
  <div class="class03">div标签3</div>
  </body>
  </html>
  ```

- css属性

  color：字体颜色	border：边框的像素大小、颜色、虚实（solid）	width/height：div的大小

  background：背景颜色	font-size：字体大小	margin（-left/-right   + auto居中）

  text-decoration：none）超链接去下划线

  border-collapse：collapse边框合并

- 

- 



## JavaScript

- alert弹窗输出语句，直接在html文件中编写

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          //alert使javaScript语言提供得一个警告框函数
          //它可以接收任意类型得参数，这个参数就是警告框得提示信息
          alert("hello javaScript!")
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 在外部编写，html文件中导入使用

  ```js
  alert("hello javaScript!")
  ```

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <!--
          使用script引入外部的js文件来执行
          script标签可以定义js代码，也可以引入js文件，功能只能二选一
      -->
      <script type="text/javascript" src="1.js"></script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 变量

  数值类型：number		字符串类型：string		对象类型：object		布尔类型：boolean

  函数类型：function

  

  特殊值：

  ​	undefined：未定义，所有js变量为赋于初始值的时候的值

  ​	null：空值		NAN：非数字，非数值

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          var i;
          i = 12;
          alert(typeof (i));
          var j = "abc"
          alert(typeof (j));
          alert(i * j);
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 逻辑运算

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>逻辑运算</title>
      <script type="text/javascript">
          /**
           * JavaScript中，所有变量都可以作为一个boolean类型
           * 0,null,undefind,""（空串）都认为是false
           *
           * &&且运算（两种情况）
           * 第一种：当表达式全为真，返回最后一个表达式的值
           * 第二种：当表达式中，有一个为假的时候，返回第一个为假的表达式的值
           *
           * ||或运算
           * 第一种：当表达式全为假，返回最后一个表达式的值
           * 第二种：只要有一个表达式为真，返回第一个为真的表达式的值
           */
          var a = "abc";
          var b = true;
          var d = false;
          var c = null;
          // alert(a && b);  //true
          // alert(a && d);  //false
          // alert(a && c);  //null
  
          alert(d || c);    //null
          alert(c || d);    //false
          alert(b || c);  //true
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 数组（不定长，自动扩容）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>数组</title>
      <script type="text/javascript">
          var arr = [];
          alert(arr.length);
          arr[0] = 11;
          alert(arr[0]);
          arr[2] = 22;
          alert(arr[1]);
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 函数（第一种方式）

  ```html
  <!DOCTYPE html>
  <html lang="cn">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          /**
           * 第一种函数定义方式
           * function 函数名(参数名){
           *     函数体;
           * }
           */
          //无参函数
          function fun() {
              alert("无参函数fun()被调用了");
          }
  
          fun();
  
          //有参函数
          function fun2(a, b) {
              alert("有参函数被执行了，a=" + a + "，b=" + b);
          }
  
          fun2(22, 33);
  
          //有返回值的函数
          function fun3() {
              return 666;
          }
  
          alert("fun3函数返回值：" + fun3());
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 函数（第二种方式），==js中函数不能重载，将直接覆盖==

  ```html
  <!DOCTYPE html>
  <html lang="cn">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          /**
           * 第一种函数定义方式
           * var 函数名 = function (参数名){
           *     函数体;
           * }
           */
          var fun = function (a, b) {
              alert("有参函数被调用了，a=" + a + "，b=" + b);
          }
          fun(22, 33);
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- 隐形参数，arguments，所有参数的数组

  ```html
  <!DOCTYPE html>
  <html lang="cn">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          function fun() {
              alert(arguments.length);
              alert("无参函数fun()");
          }
  
          fun(a, "ab");
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

  应用，参数为一串数字，函数计算总和，定义的函数参数个数任意，在函数体类调用arguments，类似数组使用

- object形式的自定义对象，变量、函数

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          var obj = new Object();
          obj.name = "2233娘";
          obj.age = 18;
          obj.fun = function (){
              alert("姓名：" + this.name);
          }
          alert(obj.age);
          obj.fun();
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- {}花括号形式的自定义对象，最后一项后面不加逗号“，”

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          // var obj = {};
          // alert(typeof (obj));
          var obj = {
              name: "2233娘",
              age: 18,
              fun: function () {
                  alert("姓名：" + this.name + "，年龄：" + this.age);
              }
          };
          alert(obj.name);
          obj.fun();
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- js事件

  | 事件名                       | 使用时期                                     |
  | :--------------------------- | :------------------------------------------- |
  | onload()：加载完成事件       | 页面加载完成之后，常用于页面js代码初始化操作 |
  | onclick()：单击事件          | 常用于按钮的点击相应操作                     |
  | onblur()：失去焦点事件       | 常用于输入框失去焦点后验证输入内容是否合法   |
  | onchange()：内容发生改变事件 | 常用于下拉列表和输入框内容发生改变后操作     |
  | onsubmit()：表单提交事件     | 常用于表单提交前，验证所有表单项是否合法     |

- 事件注册（绑定）

  告诉浏览器，当事件响应后要执行哪些操作

  **静态注册**（通过html标签的事件属性直接赋于事件响应后的代码）

  ​	直接在标签中类似添加属性一样，添加：事件名 = "自己编写的函数名"

  **动态注册**（先通过js代码得到标签的dom对象，然后再通过dom对象.事件名 = function(){}的形式赋于事件响应后的代码+）

  ​	先在外部编写

  ```html
  window.onload = function (){
      alert('动态注册onload事件');
  }
  ```

  ​	除onload不需要额外添加外，别的需要在上述代码中获取到标签对象，再使用标签对象调用事件，再在事件体中编写需要执行的方法。如：

  onload事件（加载完成事件）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          function onloadFun(){
              alert('静态注册onload事件');
          }
          window.onload = function (){
              alert('动态注册onload事件');
          }
      </script>
  </head>
  <body onload="onloadFun()">
  
  </body>
  </html>
  ```

  静态注册的事件需要引用，如上述代码；

  动态注册的事件，使用window直接调用，

  onclick事件（按钮点击事件）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          function onclickFun() {
              alert("静态注册onclick事件");
          }
  
          //动态注册onclick事件
          window.onload = function () {
              /**
               * document JavaScript语言提供的一个对象（文档）
               * get  获取
               * Element  元素（标签）
               * By   通过，，由，，经，，
               * Id   id属性
               *
               * getElementById通过id属性获取标签对象
               */
              //1.获取标签对象
              var btnObj = document.getElementById("btn01");
              //2.通过标签对象.事件名 = function(){}
              btnObj.onclick = function (){
                  alert("动态注册的onclick事件");
              }
          }
      </script>
  </head>
  <body>
  <button onclick="onclickFun()">按钮1</button>
  <button id="btn01">按钮2</button>
  </body>
  </html>
  ```

  onblur事件（失去焦点事件）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          function onblurFun() {
              //console是控制台对象，室友javaScript语言提供，专门用来向浏览器的控制器打印输出，用于测试使用
              //log()打印的方法
              console.log("静态注册失去焦点事件");
          }
  
          window.onload = function () {
              //1.获取标签对象
              var passwordObj = document.getElementById("password");
              alert(passwordObj);
              //2.通过标签对象.事件名 = function(){}
              passwordObj.onblur = function () {
                  console.log("动态注册失去焦点事件");
              }
          }
      </script>
  </head>
  <body>
  用户名：<input type="text" onblur="onblurFun()"><br>
  密码：<input id="password" type="text"><br>
  </body>
  </html>
  ```

  onchange事件（内容发生改变事件）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          function onchangeFun() {
              alert("女神已经发生了改变！");
          }
  
          window.onload = function () {
              var selectObj = document.getElementById("sel01");
              selectObj.onchange = function () {
                  alert("男神已经发生了改变！");
              }
          }
      </script>
  </head>
  <body>
  请选出你心中的女神：
  <select onchange="onchangeFun()">
      <option>--女神--</option>
      <option>11</option>
      <option>22</option>
      <option>33</option>
  </select><br>
  请选出你心中的男神：
  <select id="sel01">
      <option>--男神--</option>
      <option>11</option>
      <option>22</option>
      <option>33</option>
  </select>
  </body>
  </html>
  ```

  onsubmit事件（表单提交事件）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          //静态注册表单提交事务
          function onsubmitFun() {
              //要验证所有表单是否合法，如果有一个不合法就阻止表单提交
              alert("静态注册表单提交事务");
              return false;
          }
          //动态注册表单提交事务
          window.onload = function (){
              var formObj = document.getElementById("form01");
              //alert(formObj);
              formObj.onsubmit = function (){
                  alert("动态态注册表单提交事务");
                  return false;
              }
          }
      </script>
  </head>
  <body>
  <!--return false可以阻止表单提交-->
  <form action="http://localhost:8080" method="get" onsubmit="return onsubmitFun()">
      <input type="submit" value="静态注册">
  </form>
  <form id="form01" action="http://localhost:8080">
      <input type="submit" value="动态注册">
  </form>
  </body>
  </html>
  ```

- DOM模型

  DOM对象就是文档对象模型，文档中的所有标签、属性、文本转换成为对象来管理

  1. Document管理所有的HTML文档内容
  2. 是一种树结构的文档，有层级关系
  3. 把所有的标签都对象化
  4. 可以通过document访问所有的标签对象

- 正则表达式（regexp）

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>正则表达式</title>
      <script type="text/javascript">
          //表示要求字符串中，是否包含字母
          //var patt = new RegExp("e");
          //var patt = /e/;//与上式等价
  
          //表示要求字符串中，是否包含字母a或b或c
          //var patt = /[abc]/;
          //var patt = /[a-zA-Z0-9]/;//是否包含任意字母、数字
          //var patt = /\w/;//是否包含字母、数字、下划线
          //var patt = /a+/;//至少包含1个
          //var patt = /a*/;//包含零个或多个
          //var patt = /a?/;//是否包含零个或一个a
          //var patt = /a{3}/;//是否包含连续三个a
          //var patt = /a{3,5}/;//是否包含至少3个a，至多5个a
          //var patt = /a{3,}/;//是否包含至少3个a，
          //var patt = /a$/;//是否必须以a结尾
          //var patt = /^a/;//字符串必须以a起头
          var patt = /^a{3,5}$/;//从头到尾必须完全匹配（^  $）
          var str = "aaaaaab";
          alert(patt.test(str));
      </script>
  </head>
  <body>
  
  </body>
  </html>
  ```

- getElementById（获取指定id的标签对象），返回的是dom对象

  使用的优先顺序：id > name > tag
  
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript">
          /**
           * 点击校验按钮，获取输入框中的内容，然后校验其内容是否合法
           * 必须由字符，数字，下划线组成，并且长度为5到12位
           */
          function onclickFun(){
              //1.当我们要操作一个标签时：需要先获取这个标签对象
              var usernameobj = document.getElementById("username");
              var usernameText = usernameobj.value;
              //如何验证字符串符合某个规则，需要使用正则表达式
              var patt = /^\w{5,12}$/;
              var usernameSpanObj = document.getElementById("usernameSpan");
              //innerHTML表示其实标签和结束标签中的内容
              //该属性可读可写
              //alert("innerHTML" + usernameSpanObj.innerHTML);
              if (patt.test(usernameText)){
                  //alert("用户名合法");
                  //usernameSpanObj.innerHTML = "用户名合法";
                  usernameSpanObj.innerHTML = "<img src=\"right.png\" width=\"12px\" height=\"12px\">"
              }else {
                  //alert("用户名不合法");
                  //usernameSpanObj.innerHTML = "用户名不合法";
                  usernameSpanObj.innerHTML = "<img src=\"wrong.png\" width=\"12px\" height=\"12px\">"
              }
          }
      </script>
  </head>
  <body>
  用户名：<input id="username" type="text">
  <span id="usernameSpan" style="color: red">
  
  </span>
  <button onclick="onclickFun()">校验</button>
  </body>
  </html>
  ```

    getElementsByName（指定的name属性查询返回多个标签属性集合）

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>
        <script type="text/javascript">
            //document.getElementsByName()是根据指定的name属性查询返回多个标签属性集合
            //与数组操作相同，集合中都是dom对象
            //checked表示复选框的选中状态，true：选中，false：未选中
            //选中全部复选框
            var hobbies = document.getElementsByName("hobby");
            function checkAll() {
                for (var i = 0;i<hobbies.length;i++){
                    hobbies[i].checked = true;
                }
            }

            function checkNo() {
                //取消选中全部复选框
                for (var i = 0;i<hobbies.length;i++){
                    hobbies[i].checked = false;
                }
            }

            function checkReverse() {
                //反转所有复选框
                for (var i = 0;i<hobbies.length;i++){
                    if (hobbies[i].checked){
                        hobbies[i].checked = false;
                    }else {
                        hobbies[i].checked = true;
                    }
                }
            }
        </script>
    </head>
    <body>
    兴趣爱好：
    <input type="checkbox" name="hobby" value="cpp">C++
    <input type="checkbox" name="hobby" value="java">Java
    <input type="checkbox" name="hobby" value="js">JavaScipt
    <br>
    <button onclick="checkAll()">全选</button>
    <button onclick="checkNo()">全不选</button>
    <button onclick="checkReverse()">反选</button>
    </body>
    </html>
    ```

    getElementsByTagName（是根据指定标签名来进行查询并返回集合）

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>
        <script type="text/javascript">
            //document.getElementsByTagName()是根据指定标签名来进行查询并返回集合
            //与数组操作相同，集合中都是dom对象
            //checked表示复选框的选中状态，true：选中，false：未选中
            //选中全部复选框
            //document三个查询方法，顺序为：id、name、标签名
            function checkAll(){
                var inputs = document.getElementsByTagName("input");
                for (var i = 0; i < inputs.length; i++){
                    inputs[i].checked = true;
                }
            }
        </script>
    </head>
    <body>
    兴趣爱好：
    <input type="checkbox" value="cpp">C++
    <input type="checkbox" value="java">Java
    <input type="checkbox" value="js">JavaScipt
    <br>
    <button onclick="checkAll()">全选</button>
    <button onclick="checkNo()">全不选</button>
    <button onclick="checkReverse()">反选</button>
    </body>
    </html>
    ```


- 节点的常用属性和方法
- 
- 

## jQuery

- helloworld jQuery 

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript" src="../script/jquery-1.7.2.js"></script>
      <script type="text/javascript">
          // window.onload = function (){
          //     var btnObj = document.getElementById("btnId");
          //     //alert(btnObj);
          //     btnObj.onclick = function (){
          //         alert("js 原生的单击事件");
          //     }
          // }
          $(function (){  //表示页面加载完成，等价于window.onload = function (){
              var $btnObj = $("#btnId1");    //根据id查询标签对象
              $btnObj.click(function (){
                  alert("jQuery的单击事件");
                  alert($("button").length);
              })
              var btndom = document.getElementById("btnId1");
              alert($("btnId1"));
          })
      </script>
  </head>
  <body>
  <button id="btnId1">按钮</button>
  <button id="btnId2">按钮</button>
  <button id="btnId3">按钮</button>
  </body>
  </html>
  ```

- jQuery核心函数$()

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>Title</title>
      <script type="text/javascript" src="../script/jquery-1.7.2.js"></script>
      <script type="text/javascript">
          //核心函数的4个作用
          //1.参数为函数时，再文档加载完成后执行这个函数
          $(function () {
              alert("页面加载完成之后，自动调用");
          })
          //2.参数为html字符串时，根据这个字符串创建元素节点对象
          $("<div>\n" +
              "        <span>div-span1</span>\n" +
              "        <span>div-span2</span>\n" +
              "    </div>").appendTo("body");
          //3.参数为选择器字符串时，根据这个字符串查找元素节点对象
          //      $("#id属性值");    id选择器，根据指定id查询标签对象
          //      $("标签名");   标签名选择器，根据指定的标签名查询标签
          //      $(".class属性值"); 类型选择器，可以根据class属性查询标签对象
          $(function (){
              alert($("button").length);
              //4.参数为dom对象时，将dom对象包装为jQuery对象返回
              var btn = $("#btn01");	//此处的代码应该写在方法里，否则下面的button还没执行，null
              var btn1 = document.getElementById("btn01");
              alert(btn1);
              alert(btn1 + " " + $(btn1));
          })
      </script>
  </head>
  <body>
  <div>
      <button id="btn01">标签1</button>
      <button>标签2</button>
  </div>
  </body>
  </html>
  ```

- jQuery对象和dom对象区别

  dom对象：

  ​	通过getElementById()、getElementsByName()、getElementsByTagName()查询，createElement()创建的对象都是dom对象，alert()方法出来的都是[object HTML标签名Element]的形式。

  ​	常见使用格式：document.getxxxx()		

  jQuery对象：（本质是dom对象数组）

  ​	通过jQuery提供的API创建的、包装的、所提供的API查询到的都是jQuery对象

  ​	常见使用格式：$("#btn1")（根据id查）	$("<h1></h1>")

- jQuery对象和dom对象使用区别

  两者无法相互使用对方的属性或方法

- jQuery对象和dom对象相互转换

  dom -> jQuery	：$(dom对象)

  jQuery -> dom	：jQuwey对象[下标]	取出dom对象

- jQuery选择器

  **基础选择器**

  $("") 直接在双引号中写id/标签名/name属性，可同时写多个，所得到的对象数组顺序按代码中实际顺序，与选择器中的顺序无关

  **层级选择器**

  $("标签名1 ？ 标签名2")	? 可选 [空格（1里面的**所有**（包括子孙）2标签）,>（1里面的**所有**（不包括孙）2标签）,+（紧跟着1标签的2标签）,~（与标签1同辈的所有2标签）]

  **基本过滤选择器**

  $("li:first")	获取第一个li标签

  | 选择器 | 效果                                | 选择器      | 效果                           |
  | ------ | ----------------------------------- | ----------- | ------------------------------ |
  | :first | 获取第一个元素                      | :odd        | 同even，奇数，从1开始          |
  | :last  | 获取最后一个元素                    | :eq/:gt/:lt | 等于/大于/小于给定索引值的元素 |
  | :not   | 去除所有与给定选择器匹配的元素      | :header     | 匹配如h1，h2之类的标题元素     |
  | :even  | 匹配所有索引值为偶数的元素，从0计数 | :animated   | 匹配所有正在执行动画效果的元素 |

  **内容过滤选择器**

  | 选择器          | 效果                           | 选择器         | 效果                         |
  | --------------- | ------------------------------ | -------------- | ---------------------------- |
  | :contains(text) | 匹配包含给定文本的元素         | :parent        | 含有子元素或者文本的元素     |
  | :empty          | 所有不包含子元素或文本的空元素 | :has(selector) | 含有选择器所匹配的元素的元素 |

  **过滤选择器**

  $("div[id]")	所有含有id属性的div元素

  | 选择器             | 效果                             | 选择器             | 效果           |
  | ------------------ | -------------------------------- | ------------------ | -------------- |
  | [attribute]        | 匹配包含给定属性的元素           | [attribute$=value] | 以某些值结尾的 |
  | [attribute=value]  | 匹配给定的属性是某个特定值的元素 | [attribute*=value] | 包含某些值的   |
  | [attribute!=value] | 不包含                           | [attrSel1]...      | 复合属性选择器 |
  | [attribute^=value] | 从某些值开始的                   |                    |                |

  **表单过滤器**

  

  给一个标签加入style="display:none"，即设置为不可见，成为隐藏域中的一个元素

  | 选择器    | 效果                                     | 选择器  | 效果     |
  | --------- | ---------------------------------------- | ------- | -------- |
  | :input    | 匹配所有input/textarea/select/button元素 | :image  |          |
  | :text     | 匹配所有文本输入框                       | :reset  | 重置按钮 |
  | :password | 密码输入框                               | :button | 所有按钮 |
  | :radio    | 单选框                                   | :file   | 文件域   |
  | :checkbox | 复选框                                   | :hidden | 隐藏域   |
  | :submit   | 提交按钮                                 |         |          |

  **表单对象属性**

  如：$("select option:selected")

  在标签中添加属性：disabled="disabled"，即成为不可用，运行结果中，该input无法使用

  | 选择器    | 效果                | 选择器    | 效果                                               |
  | --------- | ------------------- | --------- | -------------------------------------------------- |
  | :enabled  | 匹配所有可用的input | :checked  | 选中的元素（复选、单选等，不包括select中的option） |
  | :disabled | 不可用              | :selected | 所有选中的option元素                               |

  

- jQuery元素筛选，与上一节基本过滤选择器中相似，但是用在外部

  如：$("li").last()，获取最后一个匹配的元素

- jQuery属性操作

  

- 

- 

- 

- 

- 

- 

- 

- 

- 

## xml

可扩展的标记性语言

1. 用来保存数据，而且这些数据具有自我描述性
2. 作为项目的配置文件
3. 网路传输数据的格式（目前json为主）

- 第一个xml文件

  ```xml
  <?xml version="1.0" encoding="UTF-8" ?>
  <!--
      xml文件的声明
      version="1.0"   xml的版本
      encoding="UTF-8"    文件本身的编码
  -->
  <books>
      <book sn="SN123">
          <name>时间简史</name>
          <auther>霍金</auther>
          <price>75</price>
      </book>
      <book sn="SN456">
          <name>Java从入门到放弃</name>
          <auther>沙老师</auther>
          <price>108</price>
      </book>
  </books>
  ```

- xml语法

  注释：<!---->

  

- dom4j编程步骤

  1. 加载.xml文件创建document对象
  2. 通过document对象拿到根元素对象
  3. 通过根元素.elements（标签名）；可以返回一个集合（存放指定的标签名的元素对象）
  4. 找到你想要修改、删除的子元素，进行相应的操作
  5. 保存到硬盘

- 使用dom4j读取xml文件得到document对象

  创建一个lib目录，并添加dom4j的jar包，添加到类路径

  

- 

- 

- 

## Tomcat

**JavaWeb**：所有通过java语言编写可以通过浏览器访问的程序的总称，基于请求和响应来开发的。

**请求**：客户端给服务器发送数据		**响应**：服务器给客户端回传数据

**web资源的分类**

静态资源：html、css、js、txt、mp4、jpg等

动态资源：jsp页面、servlet程序

**常见WEB服务器**

Tomcat：Apache组织提供，提供jsp和servlet的支持，轻量级的javaweb容器（免费）

Jboss：遵从JavaEE规范的、开源代码的、纯java的EJB服务器，支持所有的JavaEE规范（免费）

GlassFish、Resin、WebLogic

**动态web工程目录**

![image-20210117122124477](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210117122124477.png)

## servlet

## 书城项目

## jsp

## AJAX

# JavaSE

## 基础

### Tomcat

1. 下载&安装

2. 配置环境变量

3. idea配置tomcat

   ![image-20201117111114693](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201117111114693.png)

   ![image-20201117111451503](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201117111451503.png)

   ![image-20201117111509986](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201117111509986.png)

## Spring系列

### Spring

#### 1、简介

##### 1.1、历史

- 2002年，首次推出Spring框架的雏形：interface21框架
- 2004年3月24日发布1.0正式版
- Rod Johnson，悉尼大学，音乐计算机双学位博士
- spring理念：是现有技术更加容易使用，本身是一个大杂烩

导入

```
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-webmvc</artifactId>
    <version>5.2.9.RELEASE</version>
</dependency>
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-jdbc</artifactId>
    <version>5.2.9.RELEASE</version>
</dependency>
```

##### 1.2、优点

- 一个开源的费框架
- 轻量级、非侵入式的框架
- ==控制反转（IOC），面向切面编程（AOP）==
- 支持事务的处理，对框架整合的支持

##### 1.3、组成

![image-20201125195045188](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201125195045188.png)

##### 1.4、扩展

现代化的java开发，基于Spring的开发

![image-20201125195215450](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201125195215450.png)

- Spring Boot
  - 一个快速开发的脚手架
  - 基于SpringBoot可以快速的开发单个微服务
  - 约定大于配置
- Spring Cloud
  - SpringCloud是基于SpringBoot实现的

弊端：发展太久之后，配置逐渐变得十分繁琐，人称“配置地狱”

#### 2、IOC理论推导

1. UserDao接口
2. UserDaoImpl实现类
3. UserService业务接口
4. UserServiceImpl业务实现类

之前业务实现中，用户需求可能影响源代码，可能需要修改大量的代码，代价十分昂贵

在service层实现类中（UserServiceImpl）设计一个set接口实现，

```
public void setUserDao(UserDao userDao) {
    this.userDao = userDao;
}
```

需要调用方法时传递一个dao层实现类的对象（需要调用哪个类里的方法，就传那个类的对象）

- 程序主动创建对象~控制权在程序员手中
- 使用set之后，程序不再具有主动性，而是被动的接收对象

从本质上解决了问题，程序员不用再去管理对象的创建了。系统的耦合性大大降低，可以更专注与业务的实现上，==IOC的原型==。

IOC本质：控制反转（Inversion of Control），是一种设计思想，DI（依赖注入）是实现IOC的一种方法。**一种通过描述（XML或注解）并通过第三方去生产或获取特定对象的方式，在spring中实现控制反转的时IOC容器，其实现方法是依赖注入（Dependancy Injection，DI）。**

IOC是Spring框架的核心内容，可使用多种方式实现（XML配置、注解、自动装配）

Spring容器在初始化时先读取配置文件，根据配置文件或元数据创建于组织对象存入容器中，程序使用时再从IOC容器中取出需要的对象。

#### 3、HelloSpring

创建实体类

```java
public class Hello {
    private String name;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    @Override
    public String toString() {
        return "Hello{" +
                "name='" + name + '\'' +
                '}';
    }
}java
```

创建xml文件

使用Spring来创建对象，在spring这些都成为bean
bean = 对象，一个bean类似于new一个对象
id：对象名  class：类的路径
property：给其属性设置值
等价于：Hello hello = new Hello()
使用时用该xml文件对象get这个bean对象，强转之后就可以调用其包含的方法

```xml
<?xml version="1.0" encoding="UTF-8"?>

<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd">

    <!--
        ref：引用Spring容器中创建好的对象
        value：具体的值，基本数据类型
    -->
    <bean id="hello" class="com.kuang.pojo.Hello">
        <property name="name" value="Hello World!"/>
    </bean>

</beans>
```

测试类

```java
public class HelloTest {
    public static void main(String[] args) {
        //获取spring的上下文对象！
        ApplicationContext context =
                new ClassPathXmlApplicationContext("beans.xml");
        //对象操作都在spring中，使用时，从里面取出来即可
        Hello hello = (Hello) context.getBean("hello");
        System.out.println(hello.toString());
        hello.toString();
    }
}
```

#### 4、IOC创建对象的方式

1. 使用无参构造创建对象，默认

2. 假设我们要使用有参构造创建对象

   1. 下标赋值

      ```xml
      <bean id="User" class="com.kuang.pojo.User">
          <constructor-arg index="0" value="铁柱404"/>
      </bean>
      ```

   2. 类型赋值

      ```xml
      <bean id="User" class="com.kuang.pojo.User">
          <constructor-arg type="java.lang.String" value="铁柱404"/>
      </bean>
      ```

   3. 参数名赋值

      ```xml
      <bean id="User" class="com.kuang.pojo.User">
          <constructor-arg name="name" value="铁柱404"/>
      </bean>
      ```

总结：在配置文件加载的时候，容器中管理的对象就已经被初始化了

#### 5、Spring配置

##### 5.1、别名

```xml
<alias name="User" alias="userNew"/>
```

##### 5.2、Bean配置

1. id：bean的唯一标识符，类似于对象名
2. class：bean对象所对应的全限定名：包名 + 类型
3. name：别名，同时取多个也行，也可用空格，分号进行分隔

```
<bean id="User" class="com.kuang.pojo.User" name="user2,u2">
    <constructor-arg name="name" value="铁柱404"/>
</bean>
```

##### 5.3、import

这个import，一般用于团队开发使用，可以将多个配置文件，导入合并为一个

指定一个使用的xml文件，import标签导入其他的xml文件，使用时获取该xml文件即可

#### 6、依赖注入

##### 6.1、构造器注入

上述介绍

##### 6.2、Set方式注入【重点】

- 依赖注入：set注入
  - 依赖：bean对象的创建依赖于容器
  - 注入：bean对象中的所有属性，由容器来注入

【环境搭建】

1. 复杂类型

   ```java
   public class Address {
       private String address;
       get()、set()...
   }
   ```

2. 真实测试对象

   ```java
   public class Student {
       private String name;
       private Address address;
       private String[] books;
       private List<String> hobbys;
       private Map<String,String> card;
       private Set<String> games;
       private String wife;
       private Properties info;
       get()、set()、toString()...
   }
   ```

3. beans.xml

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   
   <beans xmlns="http://www.springframework.org/schema/beans"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans-3.0.xsd">
   
       <bean id="student" class="com.kuang.pojo.Student">
           <property name="name" value="狂神"/>
   
       </bean>
   
   </beans>
   ```

4. 测试类

   ```java
   public class StudentTest {
       public static void main(String[] args) {
           ApplicationContext context =
                   new ClassPathXmlApplicationContext("beans.xml");
           Student student = (Student)context.getBean("student");
           System.out.println(student.toString());
       }
   }
   ```

5. 完善注入信息

   ```xml
   <bean id="address" class="com.kuang.pojo.Address">
       <property name="address" value="西安"/>
   </bean>
   
   <bean id="student" class="com.kuang.pojo.Student">
       <!--普通注入，value-->
       <property name="name" value="狂神"/>
       <!--Bean注入，ref-->
       <property name="address" ref="address"/>
       <property name="books">
           <array>
               <value>红楼梦</value>
               <value>西游记</value>
               <value>水浒传</value>
               <value>三国演义</value>
           </array>
       </property>
       <property name="hobbys">
           <list>
               <value>篮球</value>
               <value>排球</value>
           </list>
       </property>
       <property name="card">
           <map>
               <entry key="身份证" value="231321231"/>
               <entry key="银行卡" value="2341341234"/>
           </map>
       </property>
       <property name="games">
           <set>
               <value>王者荣耀</value>
               <value>绝地求生</value>
           </set>
       </property>
       <property name="wife">
           <null/>
       </property>
       <property name="info">
           <props>
               <prop key="学号">2020123123</prop>
               <prop key="班级">计算机</prop>
           </props>
       </property>
   </bean>
   ```


##### 6.3、扩展方式注入

我们可以使用p命名空间和c命名空间进行注入

使用：

```xml
<?xml version="1.0" encoding="UTF-8"?>

<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:p="http://www.springframework.org/schema/p"
       xmlns:c="http://www.springframework.org/schema/c"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-3.0.xsd">

    <!--p命名控件注入，可以直接注入属性的值-->
    <bean id="User" class="com.kuang.pojo.User" p:name="铁柱404" p:age="18"/>

    <!--c命名空间注入，-->
    <bean id="User2" class="com.kuang.pojo.User" c:age="20" c:name="翠花"/>
</beans>
```

##### 6.4、bean的作用域

1. 单例模式（Spring默认机制）

   ```xml
   <bean id="User" class="com.kuang.pojo.User" p:name="铁柱404" p:age="18" scope="singleton"/>
   ```

2. 原型模式

   ```xml
   <bean id="User" class="com.kuang.pojo.User" p:name="铁柱404" p:age="18" scope="prototype"/>
   ```

3. 其余的request、session、application，只能在web开发中使用到

#### 7、Bean的自动装配

- 自动装配是Spring满足bean依赖的一种方式
- Spring会在上下文中自动寻找，并自动给bean装配属性

Spring有三种装配方式

1. xml中显示的配置
2. java中显示配置
3. 隐式自动装配【重点】

##### 7.1、测试

##### 7.2、ByName自动装配

```xml
<bean id="Cat" class="com.kuang.pojo.Cat"/>
<bean id="Dog" class="com.kuang.pojo.Dog"/>

<!--
    byName：会自动在容器上下文中查找，和自己对象set方法后面的值对应的beanid
    如People类中有setdog()，就会查找id为cat的bean，然后装配在bean中，效果同注释掉的代码
-->
<bean id="People" class="com.kuang.pojo.People" autowire="byName">
<!--        <property name="dog" ref="Dog"/>-->
<!--        <property name="cat" ref="Cat"/>-->
<property name="name" value="铁柱404"/>
</bean>
```

##### 7.3、ByType自动装配

```xml
<bean class="com.kuang.pojo.Cat"/>
<bean class="com.kuang.pojo.Dog"/>
<!--
    byType：会自动在容器上下文中查找，和自己对象属性类型相同的bean
-->
<bean id="People" class="com.kuang.pojo.People" autowire="byType">
<property name="name" value="铁柱404"/>
</bean>
```

==使用byType时，查找类型相同的bean，故bean可以没有id==

小结：

- byName的时候，需要保证所有bean的id唯一，并且这个bean需要和自动注入的属性的set方法的值一致
- byType的时候，需要保证所有class唯一，并且这个bean需要和自动注入的属性的类型一致

##### 7.4、使用注解实现自动装配

jdk1.5支持的注解，spring2.5支持

使用注解须知：

1. 导入约束

2. 配置注解的支持：==<context:annotation-config/>==

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   
   <beans xmlns="http://www.springframework.org/schema/beans"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:context="http://www.springframework.org/schema/context"
          xsi:schemaLocation="http://www.springframework.org/schema/beans
       http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
       http://www.springframework.org/schema/context 
           http://www.springframework.org/schema/context/spring-context-3.0.xsd">
       
       <context:annotation-config/>
   
   </beans>
   ```

   **@Autowired**

   直接在属性上使用即可，也可在set方式上使用

   使用Autowired，我们可以不用编写set方法了，前提是自动装配的属性在IOC（Spring）容器中存在，且符合名字byname

   科普：

   ```xml
   @Nullable	字段标记了这个注解，说明这个字段可以为null
   ```

   ```java
   public @interface Autowired{
       boolean required() default true;
   }
   ```

   测试代码

   ```java
   public class People {
       //如果显示定义required = false，则该对象可以为null，否则不允许为空（但不是可以不定义）
       @Autowired(required = false)
       private Cat cat;
       @Autowired
       private Dog dog;
       private String name;
   }
   ```

   @Autowired自动装配的环境比较复杂时，自动装配无法通过一个注解【@Autowired】完成时，可以使用@Qualifier(value="xxx")去配置@Autowired的使用，指定一个唯一的bean对象注入

   @Qualifier可以指定某个bean（可能存在多个id相类似的的bean）

   ```java
   public class People {
       //如果显示定义required = false，则该对象可以为null，否则不允许为空（但不是可以不定义）
       @Autowired
       private Cat cat;
       @Autowired
       @Qualifier(value = "Dog")
       private Dog dog;
       private String name;
   }
   ```

   **@Resource注解**

   ```java
   public class People {
       //如果显示定义required = false，则该对象可以为null，否则不允许为空（但不是可以不定义）
       @Resource(name="Cat")
       private Cat cat;
       private Dog dog;
       private String name;
   }
   ```

   小结：

   @Autowired和@Resource

   - 都是用来自动装配，都可以放在属性字段上
   - @Autowired通过byType的方式实现，而且必须要求这个对象存在【常用】
   - @Resource默认通过byName的方式实现，如果过找不到名字，则通过byType，两个都找不到就报错。
   - 执行顺序不同
     - @Autowired通过byType的方式实现
     - @Resource默认通过byName的方式实现，失败则用byType

#### 8、使用注解开发

需要保证aop的包导入了

![image-20201127111006709](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201127111006709.png)

使用注解需要导入context约束，增加注解的支持

1. bean   @Component

2. 属性如何注入   @Value

   ```java
   //等价于<bean id="user" class="com.kuang.pojo.User"/>
   @Component
   public class User {
       @Value("铁柱")
       public String name;
   }
   ```

3. 衍生的注解

   @Component有几个衍生注解，在web开发中，会按照mvc三层架构分层（功能其实一样）

   - dao【@Repository】
   - service【@Service】
   - controller【@Controller】

   四个注解功能都是一样的，都是代表将某个类注册到Spring中，装配bean

4. 自动装配置

   ```
   @Autowired:自动装配通过类型。名字
   	如果Autowired不能唯一自动装配上属性，则要通过@Qualifier(value="xxx")
   @Nullable	字段标记了这个注解，说明这个字段可以为null
   @Resource	自动装配通过名字。类型
   ```

5. 作用域

   ```
   @Scope("xxx")
   	singleton：单例
   	prototype：原型
   ```

6. 小结

   xml与注解：

   - xml更加万能，适用于任何场合！维护简单方便
   - 注解不是自己类使用不了，维护相对复杂

   xml与注解最佳实践：

   - xml用来管理bean

   - 注解只负责完成属性的注入

   - 使用的过程中，只需要注意一个问题，必须让注解生效，就需要开启注解支持

     ```xml
     <!--指定要扫描的包，这个包下的注解就会生效-->
     <context:component-scan base-package="com.kuang"/>
     <context:annotation-config/>
     ```

#### 9、使用java的方式配置spring

完全不使用spring的xml配置，全权交给java来做

#### 10、代理模式

SpringAOP的底层

代理模式分类：

- 静态代理
- 动态代理

![image-20201127152044992](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201127152044992.png)

##### 10.1、静态代理

角色分析：

- 抽象角色：一般会使用接口或者抽象类解决
   ```java
   public interface Rent {
       public void rent();
   }
   ```
- 真实角色：被代理的角色
   ```java
   public class Host implements Rent {
       @Override
       public void rent() {
           System.out.println("我要出组房子");java
       }
   }
   ```
- 代理角色：代理真实角色，代理真实角色后，我们一般会做附属操作
   ```java
   public class Proxy implements Rent{
       private Host host;
   
       public Proxy() {
       }
   
       public Proxy(Host host){
           this.host = host;
       }
   
       @Override
       public void rent() {
           seeHouse();
           host.rent();
           fare();
       }
   
       //看房
       public void seeHouse(){
           System.out.println("中介带你看房");
       }
   
       //收中介费
       public void fare(){
           System.out.println("收中介费");java
       }
   }
   ```
- 客户：访问代理对象的人
   ```java
   public class Client {    
       public static void main(String[] args) {
           Host host = new Host();
           Proxy proxy = new Proxy(host);
           proxy.rent();
       }
   }
   ```

代理模式的好处：

- 可以使真实角色的操作更加纯粹，不用关注一些公共的业务
- 公共也就交给了代理角色，实现了业务的分工
- 公共业务发生扩展时，方便集中管理

缺点：

- 一个真实角色就会产生一个代理角色；代码量会翻倍，开发效率会变低

##### 10.3、动态代理

- 和静态代理角色一样
- 代理类时动态生成的，不像静态代理是写好的
- 动态代理分为两打类：基于接口的动态代理
  - 基于接口--JDK动态代理【目前使用】
  - 基于类：cglib
  - java字节码实现：javasist

了解两个类：

- Proxy：生成动态代理实例
- InvocationHandler：调用处理程序，并返回一个结果（调用客户端调用的真实对象的方法，同时还有代理类加入的方法）

动态代理的好处：

- 可以使真实角色的操作更加纯粹，不用关注一些公共的业务
- 公共也就交给了代理角色，实现了业务的分工
- 公共业务发生扩展时，方便集中管理
- 一个动态代理类代理的是一个接口，一般就是对应一个接口
- 一个动态代理类可以代理多个类，只要是实现了同一个接口

抽象对象

```java
package com.kuang.demo04;

public interface UserService {
    public void add();
    public void update();
    public void delete();
    public void select();
}
```

真实对象

```java
package com.kuang.demo04;

public class UserServiceImpl implements UserService{
    @Override
    public void add() {
        System.out.println("添加");
    }

    @Override
    public void update() {
        System.out.println("修改");
    }

    @Override
    public void delete() {
        System.out.println("删除");
    }

    @Override
    public void select() {
        System.out.println("查询");
    }
}
```

代理对象

```java
package com.kuang.demo04;

import com.kuang.demo03.Rent;

import java.lang.reflect.InvocationHandler;
import java.lang.reflect.Method;
import java.lang.reflect.Proxy;

//自动生成代理类
public class ProxyInvocationHandler implements InvocationHandler {

    //被代理的接口
    private Object target;

    public void setTarget(Object target){
        this.target = target;
    }

    //生成得到代理类
    public Object getProxy(){
        return Proxy.newProxyInstance(this.getClass().getClassLoader(),target.getClass().getInterfaces(),this);
    }

    //处理代理实例，并返回结果
    @Override
    public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
        log(method.getName());
        Object result = method.invoke(target, args);
        return result;
    }

    public void log(String msg){
        System.out.println("执行了" + msg + "方法");
    }
}
```

客户

```java
package com.kuang.demo04;

import com.kuang.demo02.UserService;
import com.kuang.demo02.UserServiceImpl;

import java.util.Properties;

public class Client {
    public static void main(String[] args) {
        //真实角色
        UserServiceImpl userService = new UserServiceImpl();
        //代理角色，不存在
        ProxyInvocationHandler pih = new ProxyInvocationHandler();
        pih.setTarget(userService); //设置要代理的对象
        //动态生成代理类
        UserService proxy = (UserService)pih.getProxy();
        proxy.add();
    }
}
```

#### 11、AOP

##### 11.1、什么是AOP

![image-20201127200325169](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201127200325169.png)

![image-20201127200346358](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201127200346358.png)



##### 11.2、AOP在Spring中的作用

![image-20201127200511901](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201127200511901.png)

![image-20201127200654143](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201127200654143.png)



##### 11.3、使用Spring实现Aop

导入依赖包

```
<dependency>
    <groupId>org.aspectj</groupId>
    <artifactId>aspectjweaver</artifactId>
    <version>1.9.6</version>
</dependency>
```

方式一：使用Spring的API接口【主要SpringAPI】

方式二：自定义来实现AOP【主要是切面定义】

方式三：使用注解实现

#### 12、整合Mybatis

步骤：

1. 导入相关jar包
   - junit
   - mybatis
   - mysql数据库
   - spring相关的
   - aop织入
   - mybatis-spring
2. 编写配置文件
3. 测试

##### 12.1、回忆mybatis

1. 编写实体类
2. 编写核心配置文件
3. 编写接口
4. 编写Mapper.xml
5. 测试

##### 12.2、Mybatis-spring

1. 编写数据源配置
2. sqlSessionFactory
3. sqlSessionTemplate
4. 需要给接口加实现类
5. 将自己写的实现类，注入到spring中，测试

#### 13、声明式事务

##### 13.1、回顾事务

- 把一组业务当作一个业务，要么都成功，要么都失败
- 涉及数据的一致性
- 确保完整性和一致性

事务ACID原则

- 原主性
- 一致性
- 隔离性
  - 多个业务可能操作同一个资源，防止数据损坏
- 持久性
  - 事务一旦提交，无论系统发生什么问题，结果都不再被影响，被持久的写在存储器中

1. 引入依赖
2. pojo包实体类、mapper包实体接口（定义对实体数据的操作方法）
3. 编写mybatis配置类
4. 编写spring mybatis整合配置文件（整合mybatis中的，数据库连接信息、sqlsessionFactory、sqlsession）
5. mapper包xml文件（具体操作数据库的SQL语句）、mapper包接口实现类（实现接口中的方法）
6. applicationContext.xml文件，将配置文件.xml整合在一起，（import标签），配置bean（接口实现类）
7. 测试类编写

##### 13.2、spring中的事务管理

- 声明式事务：AOP
- 编程式事务：需要在代码中，进行事务管理

思考：

为什么需要事务

- 如果不配置事务，可能存在数据提交不一致的情况，无法保证ACID原则；
- 在spring中配置，就需要手动在代码中配置，会修改源代码
- 事务在项目的开发中十分重要，涉及到数据的一致性和完整性

### SpringMVC

Spring：IOC和AOP

SpringMVC：SSM框架整合

Spring

MVC：

- 模型（dao，service）、视图（jsp）、控制器（Servlet）的简写，是一种软件设计规范
- 将业务逻辑、数据、显示分离的方法来组织代码
- MVC主要作用是降低视图与业务逻辑间的双向耦合
- MVC不是一种设计模式，是一种架构模式，不同的MVC间存在差异

MVC框架的任务

- 将url映射到java类或java类的方法
- 封装用户提交的数据
- 处理请求--调用相关的业务处理--封装响应数据
- 将相应的数据进行渲染.jsp/html等表示层数据

Spring MVC的特点

1. 轻量级、简单易学
2. 高效，基于请求相应的MVC框架
3. 与spring兼容性好，无缝结合
4. 约定优于配置
5. 功能强大：RESTful、数据验证、格式化、本地化、主体等
6. 简洁灵活

模型Model：

​	数据模型，提供要展示的数据，因此包含数据和行为，可以认为是领域模型或JavaBean组件，一般分为一下两层：

​	dao：联系数据库
​	service：调用dao层执行业务
视图View：

​	负责进行模型的展示，一般就是我们见到的用户界面，客户想看到的东西

​	jsp
控制器Controller：

​	接收用户请求，委托给模型进行处理（状态改变），处理完毕后把返回的模型数据返回给视图，由视图负责展示，也就是说控制器做了个调度员的工作。

​	servlet：接收前端数据，交给service层处理，然后根据处理返回的结果进行页面跳转
​	转发、重定向，两者的区别



pojo:User(id,name,pwd,sex,hobby...)可能有很多参数，可以细分，将关键的划分出来

vo:Uservo(id,name,pwd)

dto:(数据传输时对象)

**JSP：本质就是一个Servlet**

==项目的架构一定是演进的，不可能是设计好的==

#### 1、回顾Servlet

1. 新建Maven工程，导入pom依赖

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <project xmlns="http://maven.apache.org/POM/4.0.0"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
       <parent>
           <artifactId>SpringMVC</artifactId>
           <groupId>com.kuang</groupId>
           <version>1.0-SNAPSHOT</version>
       </parent>
       <modelVersion>4.0.0</modelVersion>
   
       <artifactId>springmvc-01-servlet</artifactId>
   
       <dependencies>
           <dependency>
               <groupId>junit</groupId>
               <artifactId>junit</artifactId>
               <version>4.13</version>
               <scope>test</scope>
           </dependency>
           <dependency>
               <groupId>javax.servlet</groupId>
               <artifactId>jstl</artifactId>
               <version>1.2</version>
           </dependency>
           <dependency>
               <groupId>org.springframework</groupId>
               <artifactId>spring-webmvc</artifactId>
               <version>5.2.9.RELEASE</version>
           </dependency>
       </dependencies>
   </project>
   ```

2. 创建module，添加框架支持，变成web项目

   ![image-20201129214257289](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201129214257289.png)

   ![image-20201129214334369](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201129214334369.png)

3. 导入依赖

   ```xml
   <dependency>
               <groupId>javax.servlet</groupId>
               <artifactId>servlet-api</artifactId>
               <version>2.5</version>
           </dependency>
           <dependency>
               <groupId>javax.servlet.jsp</groupId>
               <artifactId>jsp-api</artifactId>
               <version>2.2</version>
           </dependency>
   ```

4. 编写一个类继承servlet，（继承了servlet的就叫servlet），重写servlet方法

   ```java
   package com.kuang.servlet;
   
   import javax.servlet.ServletException;
   import javax.servlet.http.HttpServlet;
   import javax.servlet.http.HttpServletRequest;
   import javax.servlet.http.HttpServletResponse;
   import java.io.IOException;
   
   public class HelloServlet extends HttpServlet {
       @Override
       protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
           //1.获取前端参数
           String method = req.getParameter("method");
           if (method.equals("add")){
               req.getSession().setAttribute("msg","执行了add方法");
           }
           if (method.equals("delete")){
               req.getSession().setAttribute("msg","执行了delete方法");
           }
           //2.调用业务层
           //3.视图转发或者重定向
           req.getRequestDispatcher("/WEB-INF/jsp/test.jsp").forward(req,resp);
       }
   
       @Override
       protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
           doGet(req,resp);
       }
   }
   ```

5. 编写页面

   ```jsp
   <%--
     Created by IntelliJ IDEA.
     User: 江尚奇
     Date: 2020/11/17
     Time: 10:14
     To change this template use File | Settings | File Templates.
   --%>
   <%@ page contentType="text/html;charset=UTF-8" language="java" %>
   <html>
   <head>
       <title>Title</title>
   </head>
   <body>
   ${msg}
   </body>
   </html>
   ```

6. web.xml注册servlet

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <web-app xmlns="http://xmlns.jcp.org/xml/ns/javaee"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_4_0.xsd"
            version="4.0">
       <servlet>
           <servlet-name>hello</servlet-name>
           <servlet-class>com.kuang.servlet.HelloServlet</servlet-class>
       </servlet>
       <servlet-mapping>
           <servlet-name>hello</servlet-name>
           <url-pattern>/hello</url-pattern>
       </servlet-mapping>
       <!--设置欢迎页面，默认为index.jsp-->
       <welcome-file-list>
           <welcome-file>index.jsp</welcome-file>
       </welcome-file-list>
   </web-app>
   ```

7. 

#### 2、编写第一个SpringMVC项目

1. 新建一个Moudle，添加web的支持

2. 确定导入SpringMVC的依赖

3. 配置web.xml，注册DispatchServlet，配置servlet-mapping，来匹配所有的请求

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <web-app xmlns="http://xmlns.jcp.org/xml/ns/javaee"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_4_0.xsd"
            version="4.0">
       <!--配置DispatchServlet：这个是SpringMVC的核心；请求分发器，前端控制器-->
       <servlet>
           <servlet-name>springmvc</servlet-name>
           <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
           <!--DispatcherServlet要绑定Spring-MVC的配置文件-->
           <init-param>
               <param-name>contextConfigLocation</param-name>
               <param-value>classpath:springmvc-servlet.xml</param-value>
           </init-param>
           <!--启动级别：1（随着服务器启动而启动）-->
           <load-on-startup>1</load-on-startup>
       </servlet>
       <!--is
       在SpringMVC中 /  /*
       /:只匹配所有请求，不会去匹配jsp
       /*：匹配所有请求，包含jsp，可能会进入死循环，无尽的jsp
       -->
       <servlet-mapping>
           <servlet-name>springmvc</servlet-name>
           <url-pattern>/</url-pattern>
       </servlet-mapping>
   </web-app>
   ```

4. 编写SpringMVC的配置文件，名称：springmvc-servlet.xml

   ```xml
   <?xml version="1.0" encoding="UTF-8" ?>
   <beans xmlns="http://www.springframework.org/schema/beans"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="
      http://www.springframework.org/schema/beans
      http://www.springframework.org/schema/beans/spring-beans.xsd">
           <!--前缀-->
           <property name="prefix" value="/WEB-INF/jsp/"/>
           <!--后缀-->
           <property name="suffix" value=".jsp"/>
       </bean>
   </beans>
   ```

5. 添加处理映射器(springmvc-servlet.xml)

   ```xml
   <!--处理器映射器-->
       <bean class="org.springframework.web.servlet.handler.BeanNameUrlHandlerMapping"/>
   ```

6. 添加处理适配器(springmvc-servlet.xml)

   ```xml
   <!--处理器适配器-->
       <bean class="org.springframework.web.servlet.mvc.SimpleControllerHandlerAdapter"/>
   ```

7. 添加视图解析器(springmvc-servlet.xml)

   ```xml
   <!--视图解析器-->
       <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver" id="internalResourceViewResolver">
   ```

8. 编写操作业务Controller，要么实现Controller接口，要么增加注解，需要返回一个ModelAndView，装数据，封视图

   ```java
   package com.kuang.controller;
   
   import org.springframework.web.servlet.ModelAndView;
   import org.springframework.web.servlet.mvc.Controller;
   
   import javax.servlet.http.HttpServletRequest;
   import javax.servlet.http.HttpServletResponse;
   
   public class HelloController implements Controller {
       @Override
       public ModelAndView handleRequest(HttpServletRequest httpServletRequest, HttpServletResponse httpServletResponse) throws Exception {
           ModelAndView mv = new ModelAndView();
           //业务代码
           String result = "HelloSpringMVC";
           mv.addObject("msg",result);
           //视图跳转
           mv.setViewName("test");
           return mv;
       }
   }
   ```

9. 将自己的类交给SpringIOC容器，注册bean(springmvc-servlet.xml)

   ```xml
   <bean id="/hello" class="com.kuang.controller.HelloController"/>
   ```

10. 写要跳转的jsp页面，显示ModelandView存放的数据，以及正常页面

    test.jsp

    ```jsp
    <%--
      Created by IntelliJ IDEA.
      User: 江尚奇
      Date: 2020/11/17
      Time: 15:44
      To change this template use File | Settings | File Templates.
    --%>
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <html>
    <head>
        <title>Title</title>
    </head>
    <body>
    ${msg}
    </body>
    </html>
    ```

    index.jsp

    ```jsp
    <%--
      Created by IntelliJ IDEA.
      User: 江尚奇
      Date: 2020/11/17
      Time: 14:45
      To change this template use File | Settings | File Templates.
    --%>
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <html>
      <head>
        <title>$Title$</title>
      </head>
      <body>
      $END$
      </body>
    </html>
    ```

11. 启动tomcat服务器，自动来到index（http://localhost:8080）欢迎页面，http://localhost:8080/hello测试

可能遇到的问题：访问404，配查步骤

1. 查看控制台输出，看一下缺少什么jar
2. 如果jar包存在，显示无法输出，就在IDEA的项目中添加lib依赖（添加一个lib包，然后导入包）
3. 重启tomcat

![image-20201130111249226](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201130111249226.png)

![image-20201130160432704](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201130160432704.png)

![image-20201130160355323](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201130160355323.png)

springMVC核心三要素：

- 处理器映射器：HandlerMapping（找到要用的servlet）
- 处理器适配器：HandlerAdapter（使用servlet处理，返回数据与要跳转的页面）
- 视图解析器：ViewResolver（前缀，后缀）

```xml
@Component	组件
@Service	service
@Controller	controller
@Repository	dao
```

#### 3、注解开发

1. 新建一个Moudle，添加web的支持

2. 确定导入SpringMVC的依赖

3. 配置web.xml，注册DispatchServlet，配置servlet-mapping，来匹配所有的请求

4. 编写web.xml文件中提出的springmvc配置文件，springmvc-servlet.xml

   ```xml
   <?xml version="1.0" encoding="UTF-8" ?>
   <beans xmlns="http://www.springframework.org/schema/beans"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:context="http://www.springframework.org/schema/context"
          xmlns:mvc="http://www.springframework.org/schema/mvc"
          xsi:schemaLocation="
      http://www.springframework.org/schema/beans
      http://www.springframework.org/schema/beans/spring-beans.xsd
      http://www.springframework.org/schema/context
      https://www.springframework.org/schema/context/spring-context.xsd
      http://www.springframework.org/schema/mvc
      https://www.springframework.org/schema/mvc/spring-mvc.xsd">
       <!--自动扫描包，让指定包下的注解生效，由IOC容器统一管理-->
       <context:component-scan base-package="com.kuang.controller"/>
       <!--让SpringMVC不处理静态资源 .css .js .html .mp3 .mp4-->
       <mvc:default-servlet-handler/>
       <!--
       支持mvc注解驱动
           在spring中一般采用@RequestMapping注解来完成映射关系
           要想使@RequestMapping注解生效
           必须向上下文中注册DefaultAnnotationHandlerMapping
           和一个AnnotationMethodHandlerAdapter实例
           这两个实例分别在级别和方法级别处理
           而annotation-driven配置帮助我们自动完成上述两个实例的注入
       -->
       <mvc:annotation-driven/>
   
       <!--视图解析器-->
       <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver" id="internalResourceViewResolver">
           <property name="prefix" value="/WEB-INF/jsp/"/>
           <property name="suffix" value=".jsp"/>
       </bean>
   </beans>
   ```

5. 创建springmvc中视图解析器的目标文件夹，并编写jsp页面（测试）

   ![image-20201130213803833](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201130213803833.png)

   ```jsp
   <%--
     Created by IntelliJ IDEA.
     User: 江尚奇
     Date: 2020/11/30
     Time: 20:52
     To change this template use File | Settings | File Templates.
   --%>
   <%@ page contentType="text/html;charset=UTF-8" language="java" %>
   <html>
   <head>
       <title>$Title$</title>
   </head>
   <body>
   ${msg}<!--可用于获取servlet中传入的数据-->
   </body>
   </html>
   ```

6. 编写servlet

   ```java
   package com.kuang.controller;
   
   import org.springframework.stereotype.Controller;
   import org.springframework.ui.Model;
   import org.springframework.web.bind.annotation.RequestMapping;
   
   @Controller
   @RequestMapping("/hello")
   public class controller1 {
       @RequestMapping("/c1")	//目录
       public String index(Model model){
           model.addAttribute("msg","controller1");	//传入的参数id，value
           return "hello";	// 跳转目标页面的名字
       }
   }
   ```

7. 运行测试

#### 4、restful风格

使用前

```java
package com.kuang.controller;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
@RequestMapping("/hello")
public class restfulController {
    @RequestMapping("/add")
    public String test(int a,int b,Model model){
        int c = a+b;
        model.addAttribute("msg","a + b = " + c );
        return "hello";
    }
}
```

![image-20201130214933679](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201130214933679.png)

使用后

```java
@RequestMapping("/add/{a}/{b}")
public String test(@PathVariable int a,@PathVariable int b, Model model){
    int c = a+b;
    model.addAttribute("msg","a + b = " + c );
    return "hello";
}
```

![image-20201130215302512](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201130215302512.png)

指定请求方式：

方式一：

RequestMethod.xxx

```java
@RequestMapping(value = "/add/{a}/{b}",method = RequestMethod.GET)
public String test(@PathVariable int a,@PathVariable int b, Model model){
    int c = a+b;
    model.addAttribute("msg","a + b = " + c );
    return "hello";
}
```

方式二：

@GetMapping\@PostMapping\@PutMapping\@DeleteMapping\@PatchMapping

```java
@GetMapping("/add/{a}/{b")
public String test1(@PathVariable int a,@PathVariable int b, Model model){
    int c = a+b;
    model.addAttribute("msg","a + b = " + c );
    return "hello";
}
```

通过SpringMVC来实现转发和重定向，有视图解析器

重定向，不需要视图解析器，本质就是重新请求一个新地方，所有注意路径问题

可以重定向到另一个请求实现

![image-20201201111227595](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201201111227595.png)

#### 5、乱码

配置springMVC的乱码过滤器web.xml，==url-pattern是/*==

```xml
<filter>
    <filter-name>encoding</filter-name>
    <filter-class>org.springframework.web.filter.CharacterEncodingFilter</filter-class>
    <init-param>
        <param-name>encoding</param-name>
        <param-value>utf-8</param-value>
    </init-param>
</filter>
<filter-mapping>
    <filter-name>encoding</filter-name>
    <url-pattern>/*</url-pattern>
</filter-mapping>
```

Tomcat配置文件

安装目录下，conf->server.xml

![image-20201201114712094](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201201114712094.png)

前后端分离时代：

后端部署后端，提供接口，提供数据：

​	json：数据格式

前端独立部署，负责渲染后端的数据：

json：

- 一种轻量级的数据交换格式
- 采用完全独立于编程语言的文本格式来存储和表示数据
- 简洁和清晰的层次结构使之成为理想的数据交换语言
- 易于人阅读和编写，同时也易于机器解析和生成，有效地提升网络传输效率
- 对象表示价值对，数据由逗号分隔；花括号保存对象；方括号保存数组

#### 6、SSM整合项目

1. 项目设计

2. 建立数据库、表结构

      ```sql
   create database `ssmbuild`;
   
   use `ssmbuild`;
   
   create table `books`(
       `bookID` int(10) not null auto_increment comment '书id',
       `bookName` varchar(100) not null comment '书名 ',
       `bookCounts` int(22) not null comment '数量',
       `detail` varchar(200) not null comment '描述',
       key `bookID` (`bookID`)
   )engine = innodb default charset = utf8;
   
   insert into `books`(`bookID`,`bookName`,`bookCounts`,`detail`) values
   (1,'Java',1,'从入门到放弃'),(2,'MySQL',10,'从删库到跑路'),(3,'Linux',5,'从进门到进牢');
   ```

3. 新建maven项目、导入依赖、解决静态资源导出问题

      ```xml
      <?xml version="1.0" encoding="UTF-8"?>
      <project xmlns="http://maven.apache.org/POM/4.0.0"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
          <parent>
              <artifactId>SpringMVC</artifactId>
              <groupId>com.kuang</groupId>
              <version>1.0-SNAPSHOT</version>
          </parent>
          <modelVersion>4.0.0</modelVersion>
      
          <artifactId>ssmbuild</artifactId>
      
          <!--依赖：junit，数据库驱动，连接池，servlet，jsp，mybatis，mybatis-spring，spring-->
          <dependencies>
              <dependency>
                  <groupId>junit</groupId>
                  <artifactId>junit</artifactId>
                  <version>4.13</version>
                  <scope>test</scope>
              </dependency>
              <dependency>
                  <groupId>mysql</groupId>
                  <artifactId>mysql-connector-java</artifactId>
                  <version>8.0.21</version>
              </dependency>
              <dependency>
                  <groupId>com.mchange</groupId>
                  <artifactId>c3p0</artifactId>
                  <version>0.9.5.5</version>
              </dependency>
              <dependency>
                  <groupId>javax.servlet</groupId>
                  <artifactId>servlet-api</artifactId>
                  <version>2.5</version>
              </dependency>
              <dependency>
                  <groupId>javax.servlet.jsp</groupId>
                  <artifactId>jsp-api</artifactId>
                  <version>2.2</version>
              </dependency>
              <dependency>
                  <groupId>javax.servlet</groupId>
                  <artifactId>jstl</artifactId>
                  <version>1.2</version>
              </dependency>
      
              <!--mybatis-->
              <dependency>
                  <groupId>org.mybatis</groupId>
                  <artifactId>mybatis</artifactId>
                  <version>3.5.6</version>
              </dependency>
              <dependency>
                  <groupId>org.mybatis</groupId>
                  <artifactId>mybatis-spring</artifactId>
                  <version>2.0.5</version>
              </dependency>
      
              <!--spring-->
              <dependency>
                  <groupId>org.springframework</groupId>
                  <artifactId>spring-webmvc</artifactId>
                  <version>5.2.9.RELEASE</version>
              </dependency>
              <dependency>
                  <groupId>org.springframework</groupId>
                  <artifactId>spring-jdbc</artifactId>
                  <version>5.2.9.RELEASE</version>
              </dependency>
          </dependencies>
      
          <!--静态资源导出问题-->
          <build>
              <resources>
                  <resource>
                      <directory>src/main/java</directory>
                      <includes>
                          <include>**/*.properties</include>
                          <include>**/*.xml</include>
                      </includes>
                      <filtering>false</filtering>
                  </resource>
                  <resource>
                      <directory>src/main/resources</directory>
                      <includes>
                          <include>**/*.properties</include>
                          <include>**/*.xml</include>
                      </includes>
                      <filtering>false</filtering>
                  </resource>
              </resources>
          </build>
      
      </project>
      ```

4. 创建项目结构包

      ![image-20201201202205611](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201201202205611.png)

5. 编写mybatis、spring配置文件

      mybatis：mybatis-config.xml

      ```xml
      <?xml version="1.0" encoding="UTF8" ?>
      <!DOCTYPE configuration
              PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
              "http://mybatis.org/dtd/mybatis-3-config.dtd">
      <configuration>
      
      </configuration>
      ```

      spring：applicationContext.xml

      ```xml
      <?xml version="1.0" encoding="UTF8"?>
      
      <beans xmlns="http://www.springframework.org/schema/beans"
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:aop="http://www.springframework.org/schema/aop"
             xsi:schemaLocation="http://www.springframework.org/schema/beans
          http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
              http://www.springframework.org/schema/aop
          http://www.springframework.org/schema/aop/spring-aop-3.0.xsd">
      
      </beans>
      ```

6. 配置数据库

      编写数据库连接的数据文件：db.properties

      ```properties
      jdbc.driver=com.mysql.cj.jdbc.Driver
      #如果使用的是mysql8.0+，增加一个时区的配置;&serverTimezone=Asia/Shanghai
      jdbc.url=jdbc:mysql://localhost:3306/mybatis?useSSL=true&useUnicode=true&characterEncoding=UTF-8
      jdbc.username=root
      jdbc.password=123456
      ```

      在mybatis配置文件(mybatis-config.xml)中导入（此时交给spring），取别名

      ```xml
      <!--配置数据源，交给spring-->
      <typeAliases>
          <package name="com.kuang.pojo"/>
      </typeAliases>
      ```

7. 创建实体类（pojo包），可以手动编写set/get，也可以使用lombok，需要导包

      ```xml
      <dependency>
          <groupId>org.projectlombok</groupId>
          <artifactId>lombok</artifactId>
          <version>1.18.16</version>
      </dependency>
      ```

      Books.class

      ```java
      package com.kuang.pojo;
      
      import lombok.AllArgsConstructor;
      import lombok.Data;
      import lombok.NoArgsConstructor;
      
      @Data
      @AllArgsConstructor
      @NoArgsConstructor
      public class Books {
          private int bookID;
          private String bookName;
          private int bookCounts;
          private String detail;
      }
      ```

8. 编写接口，对实体类的一些操作方法，编写对应的mapper.xml文件，注册mapper

      ```java
      package com.kuang.mapper;
      
      import com.kuang.pojo.Books;
      import org.apache.ibatis.annotations.Param;
      import java.util.List;
      
      public interface BookMapper {
          //增加一本书
          int addBook(Books books);
      
          //删除一本书
          int deleteBookById(@Param("bookId") int id);
      
          //更新一本书
          int updateBook(Books books);
      
          //查找一本书
          Books queryBookById(@Param("bookId") int id);
      
          //查找全部书
          List<Books> queryAllBooks();
      }
      ```

      编写对应的mapper.xml文件：

      ```xml
      <?xml version="1.0" encoding="UTF8" ?>
      <!DOCTYPE mapper
              PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
              "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
      <mapper namespace="com.kuang.mapper.BookMapper">
          <insert id="addBook" parameterType="Books">
              insert into ssmbuild.books (bookName,bookCounts,detail)
              values (#{bookName},#{bookCounts},#{detail});
          </insert>
          <delete id="deleteBookById" parameterType="int">
              delete from ssmbuild.books where bookID = #{bookId};
          </delete>
          <update id="updateBook" parameterType="Books">
              update ssmbuild.books
              set bookName = #{bookName},bookCounts=#{bookCounts},detail=#{detail}
              where bookID = #{bookID};
          </update>
          <select id="queryBookById" resultType="Books" parameterType="int">
              select * from ssmbuild.books where bookID = #{bookId};
          </select>
          <select id="queryAllBooks" resultType="Books">
              select * from ssmbuild.books;
          </select>
      </mapper>
      ```

      注册mapper，在mybatis-config.xml

      ```xml
      <mappers>
          <mapper class="com.kuang.mapper.BookMapper"/>
      </mappers>
      ```

9. 编写对应的业务层（service），接口，实现类

      接口：BookService

      ```java
      package com.kuang.service;
      
      import com.kuang.pojo.Books;
      import org.apache.ibatis.annotations.Param;
      
      import java.util.List;
      
      public interface BookService {
          //增加一本书
          int addBook(Books books);
      
          //删除一本书
          int deleteBookById(int id);
      
          //更新一本书
          int updateBook(Books books);
      
          //查找一本书
          Books queryBookById(int id);
      
          //查找全部书
          List<Books> queryAllBooks();
      }
      ```
      
      实现类：BookServiceImpl
      
      ```java
      package com.kuang.service;
      
      ```

import com.kuang.mapper.BookMapper;
      import com.kuang.pojo.Books;
import java.util.List;
      
      public class BookServiceImpl implements BookService{
      
          //service需要调用dao层，此处组合dao
          private BookMapper bookMapper;
      
          public void setBookMapper(BookMapper bookMapper) {
              this.bookMapper = bookMapper;
          }
      
          @Override
          public int addBook(Books books) {
              return bookMapper.addBook(books);
          }
      
          @Override
          public int deleteBookById(int id) {
              return bookMapper.deleteBookById(id);
          }
      
          @Override
          public int updateBook(Books books) {
              return bookMapper.updateBook(books);
          }
      
          @Override
          public Books queryBookById(int id) {
              return bookMapper.queryBookById(id);
          }
      
          @Override
          public List<Books> queryAllBooks() {
              return bookMapper.queryAllBooks();
          }
      }
      ```

10. 编写spring整合mybatis文件，spring-dao.xml（编写完之后在applicationContext文件中导入）

      关联数据库配置文件、连接池、数据库事务工厂sqlsessionfactory

      ```xml
      <?xml version="1.0" encoding="UTF8"?>
      
      <beans xmlns="http://www.springframework.org/schema/beans"
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:aop="http://www.springframework.org/schema/aop"
             xmlns:context="http://www.springframework.org/schema/context"
             xsi:schemaLocation="http://www.springframework.org/schema/beans
          http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
              http://www.springframework.org/schema/aop
          http://www.springframework.org/schema/aop/spring-aop-3.0.xsd http://www.springframework.org/schema/context https://www.springframework.org/schema/context/spring-context.xsd">
      
          <!--1.关联数据库配置文件-->
          <context:property-placeholder location="classpath:db.properties"/>
      
          <!--2.连接池
              dbcp:半自动化操作，不能自动连接
              c3p0:自动化操作（自动化的加载配置文件）
              druid:
              hikari:
          -->
          <bean id="dataSource" class="com.mchange.v2.c3p0.ComboPooledDataSource">
              <property name="driverClass" value="${jdbc.driver}"/>
              <property name="jdbcUrl" value="${jdbc.url}"/>
              <property name="user" value="${jdbc.username}"/>
              <property name="password" value="${jdbc.password}"/>
      
              <!--c3p0连接池的私有属性-->
              <property name="maxPoolSize" value="30"/>
              <property name="minPoolSize" value="10"/>
              <!--关闭来连接后不自动commit-->
              <property name="autoCommitOnClose" value="false"/>
              <!--获取连接超时时间-->
              <property name="checkoutTimeout" value="10000"/>
              <!--当获取连接失败重试次数-->
              <property name="acquireRetryAttempts" value="2"/>
          </bean>
      
          <!--3.sqlSessionFactory-->
          <bean id="sqlSessionFactory" class="org.mybatis.spring.SqlSessionFactoryBean">
              <property name="dataSource" ref="dataSource"/>
              <!--绑定Mybatis的配置文件-->
              <property name="configLocation" value="classpath:mybatis-config.xml"/>
          </bean>
          
          <!--4.配置dao接口扫描包，动态的实现了Dao接口可以注入Spring容器中-->
          <bean class="org.mybatis.spring.mapper.MapperScannerConfigurer">
              <!--注入sqlSessionFactory-->
              <property name="sqlSessionFactoryBeanName" value="sqlSessionFactory"/>
              <!--要扫描的dao包-->
              <property name="basePackage" value="com.kuang.dao"/>
          </bean>
      </beans>
      ```

11. 整合service层，spring-service.xml（编写完之后在applicationContext文件中导入）

       ```xml
       <?xml version="1.0" encoding="UTF8"?>
       
       <beans xmlns="http://www.springframework.org/schema/beans"
              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
              xmlns:aop="http://www.springframework.org/schema/aop"
              xmlns:context="http://www.springframework.org/schema/context"
              xsi:schemaLocation="http://www.springframework.org/schema/beans
           http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
               http://www.springframework.org/schema/aop
           http://www.springframework.org/schema/aop/spring-aop-3.0.xsd http://www.springframework.org/schema/context https://www.springframework.org/schema/context/spring-context.xsd">
       
           <!--1.扫描service下的包-->
           <context:component-scan base-package="com.kuang.service"/>
       
           <!--2.将我们所有业务类，注入到Spring，可以通过配置，或者注解实现-->
           <bean id="BookServiceImpl" class="com.kuang.service.BookServiceImpl">
               <property name="bookMapper" ref="bookMapper"/>
           </bean>
       
           <!--3.声明式事务配置-->
           <bean id="transactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">
               <!--注入数据源-->
               <property name="dataSource" ref="dataSource"/>
       
               <!--4.aop事务支持-->
           </bean>
       </beans>
       ```

       第二步可能失败，爆红，原因有二

       1. spring-dao.xml文件中，包名写错，无法找到

          ![image-20201202105520346](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201202105520346.png)

       2. 没有交给spring管理

          project structure-》modules-》当前项目下的spring

          ![image-20201202105642354](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201202105642354.png)

          三个xml不在ApplicationContext包下

       3. 

12. 添加web工程文件，编写web.xml文件

       ![image-20201202105837251](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201202105837251.png)

       ```xml
       <?xml version="1.0" encoding="UTF-8"?>
       <web-app xmlns="http://xmlns.jcp.org/xml/ns/javaee"
                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_4_0.xsd"
                version="4.0">
       
           <!--DispatcherServlet-->
           <servlet>
               <servlet-name>springmvc</servlet-name>
               <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
               <init-param>
                   <param-name>contextConfigLocation</param-name>
                   <param-value>classpath:spring-mvc.xml</param-value>
               </init-param>
               <load-on-startup>1</load-on-startup>
           </servlet>
           <servlet-mapping>
               <servlet-name>springmvc</servlet-name>
               <url-pattern>/</url-pattern>
           </servlet-mapping>
       
           <!--乱码过滤-->
           <filter>
               <filter-name>encodingFilter</filter-name>
               <filter-class>org.springframework.web.filter.CharacterEncodingFilter</filter-class>
               <init-param>
                   <param-name>encoding</param-name>
                   <param-value>utf-8</param-value>
               </init-param>
           </filter>
           <filter-mapping>
               <filter-name>encodingFilter</filter-name>
               <url-pattern>/*</url-pattern>
           </filter-mapping>
       
           <!--Session-->
           <session-config>
               <session-timeout>15</session-timeout>
           </session-config>
           
       </web-app>
       ```

13. spring-mvc.xml（编写完之后在applicationContext文件中导入）

       ```xml
       <?xml version="1.0" encoding="UTF8"?>
       
       <beans xmlns="http://www.springframework.org/schema/beans"
              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
              xmlns:context="http://www.springframework.org/schema/context"
              xmlns:mvc="http://www.springframework.org/schema/mvc"
              xsi:schemaLocation="http://www.springframework.org/schema/beans
           http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
               http://www.springframework.org/schema/mvc
           http://www.springframework.org/schema/mvc/spring-mvc-3.0.xsd
               http://www.springframework.org/schema/context
           https://www.springframework.org/schema/context/spring-context.xsd">
       
           <!--1.注解驱动-->
           <mvc:annotation-driven/>
           <!--2.静态资源过滤-->
           <mvc:default-servlet-handler/>
           <!--3.扫描包：controller-->
           <context:component-scan base-package="com.kuang.controller"/>
       
           <!--4.视图解析器-->
           <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
               <property name="prefix" value="/WEB-INF/jsp/"/>
               <property name="suffix" value=".jsp"/>
           </bean>
       </beans>
       ```

    编写完之后在applicationContext文件中导入

    ```xml
    <import resource="classpath:spring-dao.xml"/>
    <import resource="classpath:spring-mvc.xml"/>
    <import resource="spring-service.xml"/>
    ```

14. 编写controller，并编写对应的jsp页面

    BookController.java

    ```java
    package com.kuang.controller;
    
    import com.kuang.pojo.Books;
    import com.kuang.service.BookService;
    import org.springframework.beans.factory.annotation.Autowired;
    import org.springframework.beans.factory.annotation.Qualifier;
    import org.springframework.stereotype.Controller;
    import org.springframework.ui.Model;
    import org.springframework.web.bind.annotation.RequestMapping;
    
    import java.util.List;
    
    @Controller
    @RequestMapping("/book")
    public class BookController {
        //controller 调用service层
        @Autowired
        @Qualifier("BookServiceImpl")
        private BookService bookService;
    
        //查询所有的书籍，并返回书籍展示页面
        @RequestMapping("/allBook")
        public String list(Model model) {
            List<Books> books = bookService.queryAllBooks();
            model.addAttribute("list", books);
            return "allBook";
        }
        
        //跳转到增加书籍页面
        @RequestMapping("toAddBook")
        public String toAddBook(){
            return "addBook";
        }
    }
    ```

    index.jsp

    ```jsp
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <html>
      <head>
        <title>首页</title>
        <style>
          a{
            text-decoration: none;
            color: black;
            font-size: 18px;
          }
          h3{
            width: 180px;
            height: 38px;
            margin: 100px auto;
            text-align: center;
            line-height: 38px;
            background: deeppink;
            border-radius: 5px;
          }
        </style>
      </head>
      <body>
      <h3>
        <a href="${pageContext.request.contextPath}/book/allBook">进入书籍页面</a>
      </h3>
      </body>
    </html>
    ```

    allBook.jsp

    ```jsp
    <%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <html>
    <head>
        <title>书籍展示</title>
        <%--BootStrap美化界面--%>
        <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
    </head>
    <body>
    <div class="container">
        <div class="row clearfix">
            <div class="col-md-12 column">
                <div class="page-header">
                    <h1>
                        <small>书籍列表——显示所有书籍</small>
                    </h1>
                </div>
            </div>
            <div class="row">
                <div class="col-md-4 column">
                    <%--toAddBook--%>
                    <a class="btn btn-primary" href="${pageContext.request.contextPath}/book/toAddBook">新增书籍</a>
                </div>
            </div>
        </div>
        <div class="row clearfix">
            <div class="col-md-12 column">
                <table class="table table-hover table-striped">
                    <thead>
                    <tr>
                        <th>书籍编号</th>
                        <th>书籍名称</th>
                        <th>书籍数量</th>
                        <th>书籍详情</th>
                        <th>操作</th>
                    </tr>
                    </thead>
                    <%--书籍从数据库中查询出来，从这个list中遍历出来：foreach--%>
                    <tbody>
                    <c:forEach var="book" items="${list}">
                        <tr>
                            <td>${book.bookID}</td>
                            <td>${book.bookName}</td>
                            <td>${book.bookCounts}</td>
                            <td>${book.detail}</td>
                            <td>
                                <a class="btn btn-primary" href="${pageContext.request.contextPath}/book/toUpdateBook?id=${book.bookID}">修改</a>
                                &nbsp; | &nbsp;
                                <a class="btn btn-primary" href="${pageContext.request.contextPath}/book/deleteBook/${book.bookID}">删除</a>
                            </td>
                        </tr>
                    </c:forEach>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
    </body>
    </html>
    
    ```

15. BookController.java文件中添加“增加书籍请求”的方法，增加书籍的jsp页面

    ```java
    //添加书籍的请求
    @RequestMapping("/addBook")
    public String addBook(Books books) {
        System.out.println("addBooks=>" + books);
        bookService.addBook(books);
        //重定向到@RequestMapping("/allBook")请求
        return "redirect:/book/allBook";
    }
    ```

    addBook.jsp

    ```jsp
    <%--
      Created by IntelliJ IDEA.
      User: 江尚奇
      Date: 2020/12/3
      Time: 11:03
      To change this template use File | Settings | File Templates.
    --%>
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <html>
    <head>
        <title>增加书籍</title>
        <%--BootStrap美化界面--%>
        <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
    </head>
    <body>
    <div class="container">
        <div class="row clearfix">
            <div class="col-md-12 column">
                <div class="page-header">
                    <h1>
                        <small>书籍列表——新增书籍</small>
                    </h1>
                </div>
            </div>
        </div>
    
        <form action="${pageContext.request.contextPath}/book/addBook" method="post">
            <div class="form-group">
                <label for="bkname">书籍名称</label>
                <input type="text" name="bookName" class="form-control" id="bkname" required>
            </div>
            <div class="form-group">
                <label for="bkcount">书籍数量</label>
                <input type="text" name="bookCounts" class="form-control" id="bkcount" required>
            </div>
            <div class="form-group">
                <label for="bkdetail">书籍描述</label>
                <input type="text" name="detail" class="form-control" id="bkdetail" required>
            </div>
            <button type="submit" class="btn btn-primary">添加</button>
        </form>
    </div>
    </body>
    </html>
    ```

    

16. BookController.java文件中添加“修改书籍请求”的方法，修改书籍的jsp页面

    ```java
    //跳转到修改页面
    @RequestMapping("/toUpdateBook")
    public String toUpdateBook(int id,Model model) {
        Books books = bookService.queryBookById(id);
        model.addAttribute("qbook",books);
        return "updateBook";
    }
    
    //修改页面请求
    @RequestMapping("/updateBook")
    public String updateBook(Books books) {
        System.out.println("updateBooks=>" + books);
        bookService.updateBook(books);
        //重定向到@RequestMapping("/allBook")请求
        return "redirect:/book/allBook";
    }
    ```

    updateBook.jsp

    ```jsp
    <%--
      Created by IntelliJ IDEA.
      User: 江尚奇
      Date: 2020/12/3
      Time: 14:29
      To change this template use File | Settings | File Templates.
    --%>
    <%@ page contentType="text/html;charset=UTF-8" language="java" %>
    <html>
    <head>
        <title>修改书籍</title>
        <%--BootStrap美化界面--%>
        <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
    </head>
    <body>
    <div class="container">
        <div class="row clearfix">
            <div class="col-md-12 column">
                <div class="page-header">
                    <h1>
                        <small>书籍列表——修改书籍</small>
                    </h1>
                </div>
            </div>
        </div>
        <%--
            出现的问题，提交修改的sql请求，修改失败，
            考虑一：事务未提交；配置aop织入事务，测试仍失败
            考虑二：sql执行失败，修改未完成；前端利用隐藏域传参数bookId
        --%>
        <form action="${pageContext.request.contextPath}/book/updateBook" method="post">
            <input type="hidden" name="bookID" value="${qbook.bookID}">
            <div class="form-group">
                <label for="bkname">书籍名称</label>
                <input type="text" name="bookName" class="form-control" id="bkname" value="${qbook.bookName}" required>
            </div>
            <div class="form-group">
                <label for="bkcount">书籍数量</label>
                <input type="text" name="bookCounts" class="form-control" id="bkcount" value="${qbook.bookCounts}" required>
            </div>
            <div class="form-group">
                <label for="bkdetail">书籍描述</label>
                <input type="text" name="detail" class="form-control" id="bkdetail" value="${qbook.detail}" required>
            </div>
            <button type="submit" class="btn btn-primary">修改</button>
        </form>
    </div>
    </body>
    </html>
    ```

    添加事务织入:spring-service.xml

    ```xml
    <!--4.aop事务支持-->
        <!--结合AOP实现事务的织入-->
        <!--配置事务通知-->
        <tx:advice id="txAdvice" transaction-manager="transactionManager">
            <!--给那些方法配置事务-->
            <!--配置事务的传播特性：new propagation-->
            <tx:attributes>
    <!--            <tx:method name="add" propagation="REQUIRED"/>-->
    <!--            <tx:method name="delete" propagation="REQUIRED"/>-->
    <!--            <tx:method name="update" propagation="REQUIRED"/>-->
    <!--            <tx:method name="query" read-only="true"/>-->
                <tx:method name="*" propagation="REQUIRED"/>
            </tx:attributes>
        </tx:advice>
    
        <!--配置事务切入-->
        <aop:config>
            <aop:pointcut id="txPointCut" expression="execution(* com.kuang.mapper.*.*(..))"/>
            <aop:advisor advice-ref="txAdvice" pointcut-ref="txPointCut"/>
        </aop:config>
    ```

    配置日志

    mybatis-config.xml

    ```xml
    <!--配置日志-->
    <settings>
        <setting name="logImpl" value="STDOUT_LOGGING"/>
    </settings>
    ```

17. BookController.java文件中添加“删除书籍请求”的方法

    ```java
    //删除页面
    @RequestMapping("/deleteBook/{bookId}")
    public String deleteBook(@PathVariable("bookId") int id){
        bookService.deleteBookById(id);
        return "redirect:/book/allBook";
    }
    ```

18. 添加按书籍名称查询信息的功能

    添加功能的流程：自底向上		用户使用的流程：自顶向下

    持久层接口mapper.java->持久层实现类mapper.xml->业务层接口service.java->业务层实现类serviceImpl.java->控制器controller->前端页面

    1. 持久层接口mapper.java

       ```java
       //按书名查询书籍信息
       List<Books> queryBookByName(@Param("bookName")String bookName);
       ```

    2. 持久层实现类mapper.xml

       ```xml
       <select id="queryBookByName" parameterType="String" resultType="Books">
           select * from ssmbuild.books where bookName = #{bookName};
       </select>
       ```

    3. 业务层接口service.java

       ```java
       //按书名查询书籍信息
       List<Books> queryBookByName(String bookName);
       ```

    4. 业务层实现类serviceImpl.java

       ```java
       @Override
       public List<Books> queryBookByName(String bookName) {
           return bookMapper.queryBookByName(bookName);
       }
       ```

    5. 控制器controller

       ```java
       //查询书籍
       @RequestMapping("/queryBook")
       public String queryBook(String queryBookName, Model model) {
           List<Books> books = bookService.queryBookByName(queryBookName);
           model.addAttribute("list",books);
           return "allBook";
       }
       ```

    6. 前端页面

       ```jsp
       <a class="btn btn-primary" href="${pageContext.request.contextPath}/book/allBook">查询所有书籍</a>
       
       
       <div class="col-md-4 column" style="float: right">
           <%--查询书籍--%>
           <form class="form-inline" action="${pageContext.request.contextPath}/book/queryBook" method="post"
                 method="">
               <input type="text" name="queryBookName" class="form-control" placeholder="请输入要查询的书名" required>
               <input type="submit" class="btn btn-primary" value="查询">
           </form>
       </div>
       ```

    7. 

19. 

#### 7、Ajax

- AJAX = Asynchronous JavaScript and XML(异步的 JavaScript和XML)
- 一种在无需重新加载整个网页的情况下，能够更新部分网页的技术
- 不是一种新的编程 语言，是一种用于创建更好更快以及交互性更强的web应用程序技术

传统的网页，更新内容或提交表单，需要重新加载整个网页

使用ajax的网页，通过在后台服务器进行少量的数据交换，就可以实现异步局部更新，用户可以创建接近本地桌面应用的直接、高可用、更丰富、更动态的web用户界面

前端独立部署，负责渲染后端的数据

异步无刷新请求

jQuery是一个库；js的大量函数

HTML+CSS：略懂 + js（超级熟练）

js:

- 函数：闭包
- 面向对象
- DOM
  - id,name,tag
  - create,remove
- BOM
  - window
  - document

过滤器和拦截器：

**过滤器：**

- servlet规范中的一部分，任何java web工程都可以使用
- 在url-pattern中配置/*之后，可以对所有访问的资源进行拦截

拦截器：

- 是springmvc框架自己的，只有 使用了springmvc框架的工程才能使用
- 只会拦截访问的控制器方法，如果访问的是jsp/html/css/image/js是不会拦截的

springmvc拦截器、struts拦截器

- 拦截级别：springmvc是方法级别；struts2是类级别
- 数据独立性：springmvc方法间独立，独享request和response；struts2虽然方法独立，但所有action变量是共享的
- 拦截机制：springmvc独立的aop方式；struts2有自己的interceptor机制，所以配置文件大于



## MyBatis

思路：搭建环境-->导入MyBatis-->编写代码-->测试

### 1、简介



### 2、搭建MyBatis程序

#### 2.1、搭建环境

搭建数据库

```sql
create database `mybatis`;

use `mybatis`;

create table `user`(
	`id` int(20) not null primary key,
	`name` varchar(30) default null,
	`pwd` varchar(30) default null
)engine=innodb default charset=utf8;

insert into `user` (`id`,`name`,`pwd`) values
(1,'张三','123456'),
(2,'李四','654321'),
(3,'王五','234567')
```

新建项目

1. 新建maven项目，删除src目录

2. 导入maven依赖

```
<dependencies>
    <!--mysql驱动-->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.21</version>
    </dependency>
    <!--mybatis-->
    <dependency>
        <groupId>org.mybatis</groupId>
        <artifactId>mybatis</artifactId>
        <version>3.5.6</version>
    </dependency>
    <!--junit-->
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```

#### 2.2、创建一个模块

- 编写mybatis的核心配置文件

mybatis-config.xml

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE configuration
        PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
    <environments default="development">
        <environment id="development">
            <transactionManager type="JDBC"/>
            <dataSource type="POOLED">
                <property name="driver" value="com.mysql.cj.jdbc.Driver"/>
                <property name="url" value="jdbc:mysql://localhost:3306/mybatis?useSSL=true&amp;useUnicode=true&amp;characterEncoding=UTF-8"/>
                <property name="username" value="root"/>
                <property name="password" value="123456"/>
            </dataSource>
        </environment>
    </environments>
    <mappers>
        <mapper resource="org/mybatis/example/BlogMapper.xml"/>
    </mappers>
</configuration>
```

- 编写mybatis工具类

```
public class MybatisUtils {
    private static SqlSessionFactory sqlSessionFactory;
    static {
        try{
            //获取sqlSessionFactory对象
            String resource = "mybatis-config.xml";
            InputStream inputStream = Resources.getResourceAsStream(resource);
            sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);
        }catch (IOException e){
            e.printStackTrace();
        }
    }

    public static SqlSession getSqlSession(){
        return sqlSessionFactory.openSession();
    }
}
```

#### 2.3、编写代码

- 实体类

```
public class User {
    private int id;
    private String name;
    private String pwd;
    
    get、set方法;
    有参、无参构造方法;
    toString();
}
```

- Dao接口

```
public interface UserDao {
    List<User> getUserList();
}
```

- 接口实现类由原来的UserDaoImpl转变为Mapper

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.kuang.dao.UserDao">
    <select id="getUserList" resultType="com.kuang.pojo.User">
        select * from mybatis.user;
    </select>
</mapper>
```

#### 2.4、测试

注意点：

- org.apache.ibatis.binding.BindingException: Type interface com.kuang.dao.UserDao is not known to the MapperRegistry.

原因（翻译）：在Mapper注册中心中，未知的接口类型com.kuang.dao.UserDao

解决：每一个Mapper.xml都需要在Mybatis核心配置文件中注册，resources中mybatis-config.xml文件中

```
<mappers>
	<mapper resource="com/kuang/dao/UserMapper.xml（所用到的xml文件路径）"/>
</mappers>
```

- java.lang.ExceptionInInitializerError
  	at com.kuang.dao.UserDaoTest.test(UserDaoTest.java:20)

  Caused by: java.io.IOException: Could not find resource com/kuang/dao/UserMapper.xml

  原因（翻译）：

  1. 无法找到UserMapper.xml文件
  2. 测试的代码在test目录下，但是所需要的xml文件在main目录下

  解决：

  1. （low的方式）将缺少的xml文件复制到测试文件夹中的相同位置
  2. 添加资源过滤

```
<build>
    <resources>
        <resource>
            <directory>src/main/resources</directory>
            <includes>
                <include>**/*.properties</include>
                <include>**/*.xml</include>
            </includes>
            <filtering>true</filtering>
        </resource>
        <resource>
            <directory>src/main/java</directory>
            <includes>
                <include>**/*.properties</include>
                <include>**/*.xml</include>
            </includes>
            <filtering>true</filtering>
        </resource>
    </resources>
</build>
```

### 3、CRUD

#### 3.1、namespace

namespace中的包名要和Dao/mapper接口的包名一致

#### 3.2、select

选择，查询语句；

- id：就是对应的namespace中的方法名；
- resultType：Sql语句执行的返回值；
- parameterType：参数类型！

1. 编写接口

```
//查询全部用户
List<User> getUserList();
```

2. 编写对应的mapper中的sql语句

```
<select id="getUserList" resultType="com.kuang.pojo.User">
	select * from mybatis.user;
</select>
```

3. 编写测试类

```
@Test
public void test() {
    //第一步：；获取SqlSession对象
    SqlSession sqlSession = MybatisUtils.getSqlSession();
    UserMapper userMapper = sqlSession.getMapper(UserMapper.class);
    List<User> userList = userMapper.getUserList();

    for (User user : userList) {
    	System.out.println(user);
    }
    //关闭Sqlsession
    sqlSession.close();
}
```

#### 3.3、add

1. 编写接口

```
//insert一个用户
int addUser(User user);
```

2. 编写对应的mapper中的sql语句

```
<insert id="addUser" parameterType="com.kuang.pojo.User">
	insert into mybatis.user (id, name, pwd) value (#{id},#{name},#{pwd});
</insert>
```

3. 编写测试类

```
@Test
public void addUser() {
    //第一步：；获取SqlSession对象
    SqlSession sqlSession = MybatisUtils.getSqlSession();

    UserMapper mapper = sqlSession.getMapper(UserMapper.class);
    mapper.addUser(new User(4, "赵六", "345678"));
    sqlSession.commit();
    test();
    //关闭Sqlsession
    sqlSession.close();
}
```

#### 3.4、update

1. 编写接口

```
//修改用户
int updateUser(User user);
```

2. 编写对应的mapper中的sql语句

```
<update id="updateUser" parameterType="com.kuang.pojo.User">
	update mybatis.user set name=#{name},pwd=#{pwd} where id = #{id};
</update>
```

3. 编写测试类

```
@Test
public void updateUser() {
    SqlSession sqlSession = MybatisUtils.getSqlSession();

    UserMapper mapper = sqlSession.getMapper(UserMapper.class);
    mapper.updateUser(new User(4, "哈哈哈", "666666"));

    sqlSession.commit();
    sqlSession.close();
}
```

#### 3.5、delete

1. 编写接口

```
//删除一个用户
int deleteUser(int id);
```

2. 编写对应的mapper中的sql语句

```
<delete id="deleteUser" parameterType="int">
	delete from mybatis.user where id = #{id};
</delete>
```

3. 编写测试类

```
@Test
public void deleteUser() {
    SqlSession sqlSession = MybatisUtils.getSqlSession();

    UserMapper userMapper = sqlSession.getMapper(UserMapper.class);
    userMapper.deleteUser(4);

    sqlSession.commit();
    sqlSession.close();
}
```

#### 3.6、Map

1. 编写接口

```
//Map
int addUser2(Map<String,Object> map);
```

2. 编写对应的mapper中的sql语句

```
<insert id="addUser" parameterType="map">
	insert into mybatis.user (id, name, pwd) value (#{userid},#{username},#{userpwd});
</insert>
```

3. 编写测试类

```
@Test
public void addUser2() {
    //第一步：；获取SqlSession对象
    SqlSession sqlSession = MybatisUtils.getSqlSession();

    UserMapper mapper = sqlSession.getMapper(UserMapper.class);
    Map<String,Object> map = new HashMap<String, Object>();
    map.put("userid",5);
    map.put("username","赵六1");
    map.put("userpwd","335678");
    mapper.addUser2(map);
    sqlSession.commit();
    test();
    //关闭Sqlsession
    sqlSession.close();
}
```

#### 3.7、思考题

模糊查询：

1. Java代码执行的时候，传递通配符%%

```java
List<User> userList = userMapper.getUserList2("%李%");
```

   

2. 在sql拼接中使用通配符

```sql
<select id="getUserList2" resultType="com.kuang.pojo.User">
	select * from mybatis.user where name like "%"#{value}"%";
</select>
```

### 4、配置解析

#### 1、核心配置文件

- mybatis-config.xml

- MyBatis 的配置文件包含了会深深影响 MyBatis 行为的设置和属性信息。 配置文档的顶层结构如下

  ```
  configuration（配置）
  properties（属性）
  settings（设置）
  typeAliases（类型别名）
  typeHandlers（类型处理器）
  objectFactory（对象工厂）
  plugins（插件）
  environments（环境配置）
  environment（环境变量）
  transactionManager（事务管理器）
  dataSource（数据源）
  databaseIdProvider（数据库厂商标识）
  mappers（映射器
  ```

#### 2、环境配置

MyBatis 可以配置成适应多种环境，这种机制有助于将 SQL 映射应用于多种数据库之中， 现实情况下有多种理由需要这么做。例如，开发、测试和生产环境需要有不同的配置；或者想在具有相同 Schema 的多个生产数据库中使用相同的 SQL 映射。还有许多类似的使用场景。

**不过要记住：尽管可以配置多个环境，但每个 SqlSessionFactory 实例只能选择一种环境。**

所以，如果你想连接两个数据库，就需要创建两个 SqlSessionFactory 实例，每个数据库对应一个。而如果是三个数据库，就需要三个实例，依此类推，记起来很简单：

- **每个数据库对应一个 SqlSessionFactory 实例**

为了指定创建哪种环境，只要将它作为可选的参数传递给 SqlSessionFactoryBuilder 即可。

#### 3、属性properties

通过properties属性可以实现引用配置文件

这些属性可以在外部进行配置，并可以进行动态替换。你既可以在典型的 Java 属性文件中配置这些属性，也可以在 properties 元素的子元素中设置。

编写一个配置文件：

db.properties

```
driver=com.mysql.cj.jdbc.Driver
url=jdbc:mysql://localhost:3306/mybatis?useSSL=true&useUnicode=true&characterEncoding=UTF-8
username=root
password=123456
```

在核心配置文件中引入

```
<!--引入外部配置文件-->
<properties resource="db.properties"/>
```

注意顺序：

![image-20201121161102416](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201121161102416.png)

- 可以直接引入外部文件
- 可以在其中增加一些属性配置
- 如果两个文件有同一个字段，优先使用外部文件的

#### 4、类型别名（typeAliases）

- 为java类型设置一个短的名字
- 意义在于减少类完全限定名的冗余

```xml
<!--设置别名-->
<typeAliases>
    <typeAlias type="com.kuang.pojo.User" alias="User"/>
</typeAliases>
```

也可以指定一个包名，MyBatis会在包名下面搜索需要的JavaBean，比如：扫描实体类的包，默认别名就是该类的首字母小写的类名

```xml
<typeAliases>
    <package name="com.kuang.pojo"/>
</typeAliases>
```

实体类比较少时，使用第一种，比较多时，使用第二种。

第一种可以自己设置别名，第二种不可以，但可以通过注解自行设置

```java
@Alias("user")
public class User{

}
```

#### 5、设置setting

MyBatis中极其重要的调整设置，改变mybatis运行时行为

![image-20201121170237665](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201121170237665.png)

#### 7、映射器mappers

方式一：

```xml
<!--每一个Mapper.xml都需要在Mybatis核心配置文件中注册-->
<mappers>
    <mapper resource="com/kuang/dao/UserMapper.xml"/>
</mappers>
```

方式二：

```xml
<!--每一个Mapper.xml都需要在Mybatis核心配置文件中注册-->
<mappers>
    <mapper class="com.kuang.dao.UserMapper"/>
</mappers>
```

注意点：

- 接口和他的Mapper配置文件同名
- 接口和他的Mapper配置文件必须在同一个包下

方式三：

```xml
<!--每一个Mapper.xml都需要在Mybatis核心配置文件中注册-->
<mappers>
    <package name="com.kuang.dao"/>
</mappers>
```

 注意点同上

#### 8、生命周期

![image-20201121174301532](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201121174301532.png)

生命周期，和作用域，至关重要，错误的使用会导致严重的并发问题

**SqlSessionFactoryBuilder：**

- 一旦创建了SqlSessionFactory，就不再需要了
- 局部变量

**SqlSessionFactory**

- 类似数据库连接池
- 一旦创建就应该在应用的运行期间一直存在，没有任何理由抛弃或另建一个
- 最佳作用域是应用作用域
- 最简单的就是使用单例模式或静态单例模式（保证全局只有一个）

**SqlSession**

- 连接到连接池的一个请求
- 他的实例不是线程安全的，因此是不能共享的，最佳的作用域是请求或方法作用域
- 用完之后需要赶紧关闭，否则资源被占用

### 5、解决属性名和字段名不一致的问题

#### 1、问题

数据库中的字段

![image-20201122164049519](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201122164049519.png)

当实体类中属性为

![image-20201122174013644](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201122174013644.png)

时，将返回password=null

原因：sql语句中星号代表数据库表中的所有属性名，查询返回的结果只和名称相同的字段相匹配如id和name，password没有匹配的属性，所以为null

```xml
select * from mybatis.user where id = #{id};
等价于
select id,name,pwd from mybatis.user where id = #{id};
```

解决办法：

- 起别名

```xml
select id,name,pwd as password from mybatis.user where id = #{id};
```

#### 2、resultMap

结果集映射

```xml
id name pwd
id name password
```

```xml
<!--结果集映射-->
<resultMap id="UserMap" type="User">
    <!--column数据库中的字段，property实体类中的属性-->
    <result column="id" property="id"/>
    <result column="name" property="name"/><!--前两个相同的可以不用映射，此处冗余-->
    <result column="pwd" property="password"/>
</resultMap>
<select id="getUserById" resultMap="UserMap">
    select * from mybatis.user where id = #{id};
</select>
```

- resultMap元素是MyBatis中最重要的最强打的元素
- ResultMap的设计思想是，对于简单的语句根部不需要配置显示的结果映射，而复杂点的语句只需要描述它们的关系就行了。
- ResultMap最优秀的地方在于，虽然你已经对它相当了解了，但根本就不需要显示地用到它们。

### 6、日志

#### 6.1、日志工厂

如果一个数据库操作，出错了异常，我们需要排错。日志就是最好地帮手

曾经：sout、debug

现在：日志工厂

![image-20201122201533610](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201122201533610.png)

- SLF4J 
- LOG4J 
- LOG4J2 
- JDK_LOGGING
- COMMONS_LOGGING
- STDOUT_LOGGING
- NO_LOGGING

```xml
<!--配置日志-->
<settings>
    <setting name="logImpl" value="STDOUT_LOGGING"/>
</settings>
```

#### 6.2、Log4j

什么是Log4j？

- Apache的一个开源项目，可以控制日志信息输送的目的地是控制台、文件、GUI组件
- 控制每一条日志的输出格式
- 通过定义每一天日志信息的级别，更加细致地控制日志地生成过程
- 通过一个配置文件来灵活地进行配置，而不需要修改应用的代码

1. 导入log4j的包

   ```xml
   <dependency>
       <groupId>log4j</groupId>
       <artifactId>log4j</artifactId>
       <version>1.2.17</version>
   </dependency>
   ```

2. log4j.properties

   ```xml
   log4j.rootLogger=DEBUG,console,file
   
   #控制台输出的相关设置
   log4j.appender.console = org.apache.log4j.ConsoleAppender
   log4j.appender.console.Target = System.out
   log4j.appender.console.Threshold=DEBUG
   log4j.appender.console.layout = org.apache.log4j.PatternLayout
   log4j.appender.console.layout.ConversionPattern=[%c]-%m%n
   
   #文件输出的相关设置
   log4j.appender.file = org.apache.log4j.RollingFileAppender
   log4j.appender.file.File=./log/kuang.log
   log4j.appender.file.MaxFileSize=10mb
   log4j.appender.file.Threshold=DEBUG
   log4j.appender.file.layout=org.apache.log4j.PatternLayout
   log4j.appender.file.layout.ConversionPattern=[%p][%d{yy-MM-dd}][%c]%m%n
   
   #日志输出级别
   log4j.logger.org.mybatis=DEBUG
   log4j.logger.java.sql=DEBUG
   log4j.logger.java.sql.Statement=DEBUG
   log4j.logger.java.sql.ResultSet=DEBUG
   log4j.logger.java.sql.PreparedStatement=DEBUG
   ```

3. 配置log4j为日志的实现

   ```xml
   <!--配置日志-->
   <settings>
       <setting name="logImpl" value="STDOUT_LOGGING"/>
   </settings>
   ```

4. log4j的使用

![image-20201122210200162](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201122210200162.png)

**简单使用**

1. 使用log4j的类中，导入包import org.apache.log4j.Logger;

2. 生成日志对象，参数为当前类的class

   ```java
   static Logger logger = Logger.getLogger(UserMapperTest.class);
   ```

3. 日志级别

   ```java
   logger.info("info:进入了testLog4j");
   logger.debug("debug:进入了testLog4j");
   logger.error("error:进入了testLog4j");
   ```

4. 

### 7、分页

- 减少数据的处理量

**7.1、使用Limit分页**

使用limit 

```sql
select * from user limit 0,2;
```

使用Mybatis实现分页，核心SQL

1. 接口

   ```javascript
   List<User> getUserByLimit(Map<String, Integer> map);
   ```

2. Mapper.xml

   ```xml
   <select id="getUserByLimit" parameterType="map" resultMap="UserMap">
       select * from mybatis.user limit #{startIndex},#{pageSize}
   </select>
   ```

3. 测试

   ```java
   @Test
   public void getUserByLimit() {
       SqlSession sqlSession = MybatisUtils.getSqlSession();
       UserMapper userMapper = sqlSession.getMapper(UserMapper.class);
   
       HashMap<String, Integer> map = new HashMap<String, Integer>();
       map.put("startIndex", 0);
       map.put("pageSize", 2);
       List<User> userList = userMapper.getUserByLimit(map);
   
       for (User user:userList){
           System.out.println(user);
       }
   
       sqlSession.close();
   }
   ```

**7.2、RowBounds分页**

### 8、使用注解开发

#### 8.1、面向接口编程

**原因：**解耦，可扩展、提高复用、分层开发中，上层不用管具体的实现，大家都遵守共同的标准，是开发变得容易，规范性更好

**关于接口的理解：**

- 更深层次的理解，是定义（规范，约束）与实现（名实分离的原则）的分离
- 本身反映了系统设计人员对系统的抽象理解
- 分为两类
  - 对一个个体的抽象，可对应为一个抽象体
  - 对一个个体某一方面的抽象，即形成一个抽象面
- 一个个体有可能有多个抽象面，抽象体与抽象面是有区别的



**三个面向区别：**

- 面向对象：考虑问题时，以对象为单位，考虑它的属性及方法
- 面向过程：以一个具体的流程（事务过程）为单位，考虑它的实现
- 接口设计与非接口设计是针对复用技术而言的，与面向对象（过程）不是一个问题，更多的体现就是对系统整体的架构

#### 8.2、使用注解开发

1. 注解字接口上实现

   ```java
   @Select("select * from user")
   List<User> getUser();
   ```

2. 需要在核心配置文件中绑定

   ```xml
   <mappers>
       <mapper class="com.kuang.dao.UserMapper"/>
   </mappers>
   ```

3. 测试

本质：反射机制实现

底层：动态代理

![image-20201123111503874](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201123111503874.png)

myBatis详细的执行流程

![image-20201123160657147](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201123160657147.png)

#### 8.3、CRUD

在工具类创建的时候实现自动提交事务

```java
public static SqlSession getSqlSession() {
    return sqlSessionFactory.openSession(true);
}
```

编写接口，增加注解

```java
//方法存在多个参数时，所有的参数前面必须加上@Param("")注解
@Select("select * from user where id = #{id}")
User getUserById(@Param("id") int id);
```

绑定接口

```xml
<mappers>
    <mapper class="com.kuang.dao.UserMapper"/>
</mappers>
```

测试类

```java
User userById = userMapper.getUserById(1);
System.out.println(userById);
```

关于@Param()注解

- 基本类型的参数或者String类型，需要加上
- 引用类型不需要加
- 如果只有一个基本类型的话，可以不加
- 在SQL中引用的就是我们这里@Param()中设定的属性名

注意：

注解中使用#{}，也可以使用${}，但是无法防止sql注入

- 用来传入参数，sql解析的时候会加上""，当成字符串来解析，
- 可以很大程度上防止sql注入

### 9、Lombok

Lombok是一个可以通过简单的注解形式来帮助我们简化消除一些必须有但显得很臃肿的Java代码的工具，通过使用对应的注解，可以在编译源码的时候生成对应的方法.

例如：无参构造、get、set、toString、hashcode、equals



使用：

1. 安装插件

   File->Setting->Plugins

   ![image-20201123174203038](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201123174203038.png)

2. 引入lombk的jar包

   ```xml
   <dependency>
       <groupId>org.projectlombok</groupId>
       <artifactId>lombok</artifactId>
       <version>1.18.16</version>
   </dependency>
   ```

3. 使用，写完@Data后会提示导包import lombok.Data;

   ```java
   @Data
   @AllArgsConstructor	//有参构造
   @NoArgsConstructor	//无参构造
   @EqualsAndHashCode	//equalsAndHashCode方法
   @ToString	//tostring方法
   public class User {
       private int id;
       private String name;
       private String password;
   }
   ```

   ![image-20201123174725311](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201123174725311.png)

### 10、多对一处理

测试环境搭建：

1. 导入Lombok（见9、Lombok）

2. 新建实体类Teacher、Student

   ```java
   import lombok.Data;
   @Data
   public class Student {
       private int id;
       private String name;
       //学生需要关联老师
       private Teacher teacher;
   }
   ```

   ```java
   import lombok.Data;
   @Data
   public class Teacher {
       private int id;
       private String name;
   }
   ```

3. 建立Mapper接口

   ```java
   public interface StudentMapper {
   
   }
   ```

   ```java
   public interface TeacherMapper {
   
   }
   ```

4. 建立Mapper.XML文件

   ```xml
   <?xml version="1.0" encoding="UTF8" ?>
   <!DOCTYPE mapper
              PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
              "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
   <mapper namespace="com.kuang.dao.StudentMapper">
   
   </mapper>
   ```

   ```xml
   <?xml version="1.0" encoding="UTF8" ?>
   <!DOCTYPE mapper
              PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
              "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
   <mapper namespace="com.kuang.dao.TeacherMapper">
   
   </mapper>
   ```

5. 在核心配置文件中绑定注册Mapper接口或文件

   ```xml
   <mappers>
       <mapper class="com.kuang.dao.StudentMapper"/>
       <mapper class="com.kuang.dao.TeacherMapper"/>
   </mappers>
   ```

6. 测试查询是否能够成功

   ```java
   @Test
   public void getStudent() {
       SqlSession sqlSession = MybatisUtils.getSqlSession();
       StudentMapper studentMapper = sqlSession.getMapper(StudentMapper.class);
   
       List<Student> students = studentMapper.getStudent2();
       for (Student student : students)
           System.out.println(student);
       sqlSession.close();
   }
   ```

建表语句：

```sql
CREATE TABLE `teacher`(
	`id` INT(10) NOT NULL,
	`name` VARCHAR(30) DEFAULT NULL,
	PRIMARY KEY (`id`)
)ENGINE=INNODB DEFAULT CHARSET=utf8;

INSERT INTO teacher(`id`,`name`) VALUES(1,'张东升');

CREATE TABLE `student`(
	`id` INT(10) NOT NULL,
	`name` VARCHAR(30) DEFAULT NULL,
	`tid` INT(10) DEFAULT NULL,
	PRIMARY KEY (`id`),
	KEY `fktid` (`tid`),
	CONSTRAINT `fktid` FOREIGN KEY(`tid`) REFERENCES `teacher` (`id`)
)ENGINE=INNODB DEFAULT CHARSET=utf8;

INSERT INTO `student` (`id`,`name`,`tid`) VALUES ('1','小明','1');
INSERT INTO `student` (`id`,`name`,`tid`) VALUES ('2','小红','1');
INSERT INTO `student` (`id`,`name`,`tid`) VALUES ('3','小张','1');
INSERT INTO `student` (`id`,`name`,`tid`) VALUES ('4','小李','1');
INSERT INTO `student` (`id`,`name`,`tid`) VALUES ('5','小王','1');
```

**按照查询嵌套处理**

```xml
<select id="getStudent" resultMap="StudentTeacher">
    select * from student;
</select>
<resultMap id="StudentTeacher" type="Student">
    <result property="id" column="id"/>
    <result property="name" column="name"/>
    <!--复杂的属性，我们需要单独处理
            对象：association
            集合：collection
        -->
    <association property="teacher" column="tid" javaType="Teacher" select="getTeacher"/>
</resultMap>
<select id="getTeacher" resultType="Teacher">
    select * from teacher where id = #{id};
</select>
```

**按照结果嵌套查询**

```xml
<select id="getStudent2" resultMap="StudentTeacher2">
    select s.id sid,s.name sname,t.name tname
    from student s,teacher t
    where s.tid = t.id;
</select>
<resultMap id="StudentTeacher2" type="Student">
    <result property="id" column="sid"/>
    <result property="name" column="sname"/>
    <association property="teacher" javaType="Teacher">
        <result property="name" column="tname"/>
    </association>
</resultMap>
```

回顾Mysql多对一查询方式：

- 子查询：查询条件中，某个属性的值等于一个查询的结果，如：tid=(select id from teacher ...)
- 联表查询：一个查询语句中，from后面接着多个表，一起查询

### 11、一对多处理

比如一个老师拥有多个学生！

对于老师而言，就是一对多关系

1. 环境搭建（同10）

**实体类**

```java
@Data
public class Teacher {
    private int id;
    private String name;

    //一个老师拥有多个学生
    private List<Student> students;
}
```

```java
@Data
public class Student {
    private int id;
    private String name;
    private int tid;
}
```

**按照结果嵌套处理**

```xml
<select id="getTeacher" resultMap="TeacherStudent">
    select s.id sid, s.name sname, t.id tid, t.name tname
    from student s,
    teacher t
    where s.tid = t.id and t.id = #{tid};
</select>
<resultMap id="TeacherStudent" type="Teacher">
    <result property="id" column="tid"/>
    <result property="name" column="tname"/>
    <!--
        复杂的属性，需要单独处理 对象：association 集合：collection
        类型为对象时：javaType
        为集合时：ofType
        -->
    <collection property="students" ofType="Student">
        <result property="id" column="sid"/>
        <result property="name" column="sname"/>
    </collection>
</resultMap>
```

**按照查询嵌套处理**

```xml
<select id="getTeacher2" resultMap="TeacherStudent2">
    select * from teacher where id=#{tid};
</select>
<resultMap id="TeacherStudent2" type="teacher">
    <collection property="students" javaType="ArrayList" ofType="student" select="getStudentByTeacherId" column="id"/>
</resultMap>
<select id="getStudentByTeacherId" resultType="student">
    select * from student where tid = #{tid};
</select>
```

**小结：**

1. 关联-association【多对一】
2. 集合-collection 【一对多】
3. javaType & ofType
   1. javaType用来指定实体类中属性的类型
   2. ofType用来指定映射到list或者集合中的pojo类型，泛型中的约束类型

**注意点：**

- 保证SQL的可读性，尽量保证通俗易懂
- 注意一对多和多对一，属性名和字段的问题
- 问题不好排查，可以使用日志，建议使用log4j

### 12、动态SQL

是什么：动态sql就是值根据不同的条件生成不同的sql语句

- if
- choose (when, otherwise)
- trim (where, set)
- foreach

**搭建环境**

1. 导包

2. 配置文件

3. 实体类

   ```java
   import lombok.Data;
   
   import java.util.Date;
   
   @Data
   public class Blog {
       private int id;
       private String title;
       private String author;
       private Date createTime;
       private int views;
   }
   ```

4. 编写实体类对应的Mapper接口和Mapper.xml文件

**IF**

```xml
<select id="queryBlogIF" parameterType="map" resultType="Blog">
    select * from blog where 1=1
    <if test="title != null">
        and title = #{title}
    </if>
    <if test="author != null">
        and author = #{author}
    </if>
</select>
```

**choose(when,otherwise)**

```xml
<select id="queryBlogChoose" parameterType="map" resultType="blog">
    select * from blog
    <where>
        <choose>
            <when test="title != null">
                title = #{title}
            </when>
            <when test="author != null">
                and author = #{author}
            </when>
            <otherwise>
                and views = #{views}
            </otherwise>
        </choose>
    </where>
</select>
```

```xml
<update id="updateBlog" parameterType="map">
    update blog
    <set>
        <if test="title != null">
            title = #{title}
        </if>
        <if test="author != null">
            author = #{author}
        </if>
    </set>
    where id = #{id}
</update>
```

==所谓动态SQL，本质还是SQL语句，只是我们可以在SQL层面，去执行一个逻辑代码==

if

where	set	choose	when



**SQL片段**

有的时候，我们可能会将一些功能的部分抽取出来，方便复用

1. 使用SQL标签抽取公共的部分

   ```xml
   <sql id="if-title-author">
           <if test="title != null">
               and title = #{title}
           </if>
           <if test="author != null">
               and author = #{author}
           </if>
       </sql>
   ```

2. 在需要使用的地方使用标签引用

   ```xml
   <include refid="if-title-author"></include>
   ```

注意：（多表的时候复用性会降低）

- 最好基于单表定义SQL片段
- 不要存在where标签

**Foreach**

```sql
select * from user where 1=1 and (id=1 or id=2 or id=3)
```

示例：

```xml
<select id="queryBlogForeach" parameterType="map" resultType="blog">
    select * from blog
    <where>
        <foreach collection="ids" item="id" open="and (" close=")" separator="or">
            id = #{id}
        </foreach>
    </where>
</select>
```

```java
@Test
public void queryBlogForeach(){
    SqlSession sqlSession = MybatisUtils.getSqlSession();
    BlogMapper blogMapper = sqlSession.getMapper(BlogMapper.class);

    HashMap map = new HashMap();

    ArrayList<Integer> ids = new ArrayList<Integer>();
    ids.add(1);

    map.put("ids",ids);

    List<Blog> blogs = blogMapper.queryBlogForeach(map);
    for (Blog blog:blogs)
        System.out.println(blog);

    sqlSession.close();
}
```

==动态SQL就是在拼接SQL语句，我们只要保证SQL的正确性，按照SQL的格式，去排列组合就可以了==

注意：

- 可以先写出sql测试之后，再进行拼接

### 13、缓存

#### 13.1、简介

1. 是什么
   1. 存在内存中的临时数据
   2. 将用户经查询的数据放在缓存中，用户去查蓄奴数据就不需要从磁盘上（关系型数据库数据文件）查询，从缓存中存查询，从而提高查询效率，解决高并发系统的性能问题
2. 为什么用
   1. 减少和数据库的交互次数，减少系统开销，提高系统效率
3. 什么样的数据用
   1. 经常查询并且不经常修改的数据。

#### 13.2、Mybatis缓存

- Mybatis包含一个强大的查询缓存特性，可以方便的定制和配置缓存。缓存可以极大的提升查询效率
- Mybatis系统中默认定义了两级缓存：一级缓存、二级缓存
  - 默认只开启一级缓存（SqlSession级别的缓存，也称本地缓存），sqlsession.close之前均有效
  - 二级需要手动开启和配置，基于namespace级别的缓存
  - 为了提高扩展性，Mybatis定义了 缓存接口Cache，可以通过实现Cache接口来自定义二级缓存

#### 13.3、一级缓存

- 也称本地缓存
  - 与数据库同一次会话期间查询到的数据会放在本地缓存中
  - 如果需要获取相同的数据，直接从缓存中拿，没必要再去查询数据库
- 缓存失效的情况
  - 查询不同的东西
  - 增删改操作，可能会改变原来的数据，所以必定会刷新缓存
  - 查询不同的Mapper.xml
  - 手动清理缓存sqlSession.clearCache()

#### 13.4、二级缓存

how：

1. 在配置文件mybatis-config.xml中，显示开启全局缓存

   ```xml
   <!--显示开启全局缓存-->
   <setting name="cacheEnable" value="true"></setting>
   ```

2. 在需要开启的mapper.xml文件中添加<cache/>

   ```xml
   <cache/>
   <!--自定义-->
   <cache
          eviction="FIFO"	//先进先出
          flushInterval="60000"	//60秒刷新一次
          size="512"	//最多存512个引用
          readOnly="true"	//返回的对象默认是只读的/>
   ```

3. 测试

   1. 问题：我们需要将实体序列化，否则就会报错

      ```
      Caused by: java.io.NotSerializableException:com.kuang.pojo.User
      ```

      解决：让报错的类implements Serializable，实现序列化

   2. 

4. 小结

   1. 只要开启了二级缓存，在同一个mapper下就有效
   2. 所有数据都会先放在一级缓存中
   3. 只有当会话提交，或者关闭的时候，才会提交到二级缓存中

5. 

- 二级缓存也叫全局缓存，一级缓存作用域太低，所以产生二级缓存
- 基于namespace级别的缓存，一个名称控件对应一个二级缓存
- 工作机制
  - 一个会话查询一条数据，会被放在当前会话的一级缓存中
  - 如果当前会话关闭了，该会话的一级缓存就没了，但我们想要的是，会话关闭了，一级缓存中的数据被保存到二级缓存中
  - 新的会话查询信息，就可以从二级缓存中获取内容
  - 不同的mapper查出的数据会放在自己 对应的缓存中

![image-20201125100856962](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201125100856962.png)

先在二级缓存中找，找不到就在一级缓存中找，找不到就去连接数据库，获取数据

# 微服务
## Vue、webpack、Node.js

Vue

Soc：

HTML+CSS+JS：视图，给用户看，刷新后台给的数据

网络通信：axios

页面跳转：vue-router

状态管理：vues

Vue-UI：ICE

### 判断-循环

- if
- for

### 事件

- on

### 网络通讯

### Vue项目

1. 创建工程

   ![image-20201207194948520](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201207194948520.png)

2. 安装依赖

   ![image-20201207195354470](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201207195354470.png)

   报错：TypeError [ERR_INVALID_ARG_TYPE]: The "path" argument must be of type string. Received undefined

   ```json
   "node-sass": "^4.0.0",
   "sass-loader": "^7.3.1",
   ```

3. 创建router、views包，删除assets、components包下的文件（不删也行，对项目没用）

4. views包下创建Main.vue和Login.vue

   Main.vue

   ```vue
   <template>
     <h1>main</h1>
   </template>
   
   <script>
   export default {
     name: "Main"
   }
   </script>
   
   <style scoped>
   
   </style>
   ```
Login.vue

   ```vue
   <template>
     <div>
       <el-form ref="loginForm" :model="form" :rules="rules" label-width="80px" class="login-box">
         <h3 class="login-title">欢迎登录</h3>
         <el-form-item label="账号" prop="username">
           <el-input type="text" placeholder="请输入账号" v-model="form.username"/>
         </el-form-item>
         <el-form-item label="密码" prop="password">
           <el-input type="password" placeholder="请输入密码" v-model="form.password"/>
         </el-form-item>
         <el-form-item>
           <el-button type="primary" v-on:click="onSubmit('loginForm')">登录</el-button>
         </el-form-item>
       </el-form>
   
       <el-dialog
         title="温馨提示"
         :visible.sync="dialogVisible"
         width="30%"
         :before-close="handleClose">
         <span>请输入账号和密码</span>
         <span slot="footer" class="dialog-footer">
           <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
         </span>
       </el-dialog>
     </div>
   </template>
   <script>
   export default {
     name: "Login",
     data() {
       return {
         form: {
           username: '',
           password: ''
         },
         //表单验证，需要再el-form-item 元素中增加prop属性
         rules: {
           username: [
             {
               required: true, message: '账号不能为空',
               trigger: 'blur'
             }
           ],
           password: [
             {
               required: true, message: '密码不能为空',
               trigger: 'blur'
             }
           ]
         },
         //对话框显示和隐藏
         dialogVisible: false
       }
     },
     methods: {
       onSubmit(formName) {
         //为表单绑定验证功能
         this.$refs[formName].validate((valid) => {
           if (valid) {
             //使用 vue-router路由到指定页面，该方式称之为编程式导航
             this.$router.push("/main");
           } else {
             this.dialogVisible = true;
             return false;
           }
         });
       }
     }
   }
   </script>
   <style lang="scss" scoped>
   .login-box {
     border: 1px solid #DCDFE6;
     width: 350px;
     margin: 180px auto;
     padding: 35px 35px 15px 35px;
     border-radius: 5px;
     -webkit-border-radius: 5px;
     -moz-border-radius: 5px;
     box-shadow: 0 0 25px #909399;
   }
   
   .login-title {
     text-align: center;
     margin: 0 auto 40px auto;
     color: #303133;
   }
   </style>
   ```

5. router包下创建index.js

   ```js
   import Vue from 'vue'
   import VueRouter from "vue-router"
   
   //导入组件
   import Main from "../views/Main";
   import Login from "../views/Login";
   
   //显示引用
   Vue.use(VueRouter);
   
   //导出接口，配置路由
   export default new VueRouter({
     routes: [
       {
         path: '/main',
         component: Main
       },
       {
         path: '/login',
         component: Login
       }
     ]
   })
   ```

6. 编写main.js

   ```js
   import Vue from 'vue'
   import App from './App'
   
   //导入该目录下的所有路由
   import router from './router';
   
   import ElementUI from 'element-ui'
   import 'element-ui/lib/theme-chalk/index.css';
   
   Vue.use(router);
   Vue.use(ElementUI);
   
   new Vue({
     el: '#app',
     router,
     render: h => h(App)
   })
   ```

7. App.vue

   ```vue
   <template>
     <div id="app">
       <router-link to="/login">login</router-link>
       <router-view></router-view>
     </div>
   </template>
   
   <script>
   
   export default {
     name: 'App'
   }
   </script>
   
   <style>
   #app {
     font-family: 'Avenir', Helvetica, Arial, sans-serif;
     -webkit-font-smoothing: antialiased;
     -moz-osx-font-smoothing: grayscale;
     text-align: center;
     color: #2c3e50;
     margin-top: 60px;
   }
   </style>
   ```

8. npm run dev测试

## SpringBoot

### 第一个SpringBoot程序



### 原理初探

自动配置：

pom.xml

- spring-boot-dependencies：核心依赖在父类工程中
- 引入springboot依赖时，不需要指定版本（因为有版本仓库）



启动器

- ```xmml
  <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
  </dependency>
  ```

- 启动器：说白了就是SpringBoot的启动场景

- 比如spring-boot-starter-web，就会帮我们自动导入web环境所有的依赖

- springboot会将所有的功能场景，都变成一个个的启动器

- 我们要是用什么功能，就只需要找到对应的启动器就可以了

结论：springboot所有自动配置都是在启动的时候扫描并加载的：Spring。fa'ctories所有的自动配置类都在这里面，但是不一定生效，要判断条件是否成立（导入对应的start，就有了对应的启动器，自动装配就会生效，然后配置成功）。

启动过程：

1. 从类路径下/META-INF/spring。factories获取指定的值
2. 将这些自动配置的类导入容器，自动配置就会生效，帮我进行自动配置
3. 以前我们需要自动配置的东西，现在springboot帮我们做了
4. 整合javaEE，解决方案和自动配置的东西都在spring-boot-autoconfigure-2.2.0.RELEASE.jar包下
5. 它会把所有需要导入的组件，以类名的方式返回，这些组件就会被添加到容器
6. 容器中也会存在非常多的xxxAutoConfiguration文件（@Bean），就是这些类给容器导入了这个场景所需要的所有容器，并自动配置，@Configuration，
7. 有了自动配置类，免去了我们手动编写配置文件的工作

### SpringBoot配置

yaml可以直接给实体类赋值

![image-20201228155930271](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201228155930271.png)

![image-20201228155957540](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201228155957540.png)

![image-20210301165149974](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210301165149974.png)

JSR303校验

![image-20201228160134888](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201228160134888.png)

类上面加上@Validated注解，在需要加JSR303校验的变量上加上对应的注解，如email，加上@Email()注解，

也可以直接用正则表达式：@Pattern(regexp = "xxx", message = "xxx")

```
@Email(message = "邮箱格式非法")	//message可加可不加，有默认的
```

使用：

![image-20210228231127013](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210228231127013.png)

![image-20210228231235160](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210228231235160.png)![image-20210228231540438](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210228231540438.png)

![image-20210228230123115](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210228230123115.png)

**==自动装配的原理==**

1. SpringBoot启动会加载大量的自动配置类

2. 看我们需要的功能有没有在SpringBoot默认写好的自动配置类当中

3. 我们再来看这个自动配置类中到底配置了哪些组件（只要我们要用的组件存在其中，就不需要手动配置了）

4. 给容器中自动配置类添加组件时，会从properties类中获取某些属性。文件中指定这些属性的值即可

   xxxxAutoConfiguration： 自动配置类；给容器中添加组件

   xxxxProperties： 封装配置文件中相关属性（properties文件/yaml文件，设置值）

### SpringBoot Web开发

需要准备的东西

- 导入静态资源
- 首页
- jsp，模板引擎Thymeleaf
- 装配扩展SpringMVC
- 增删改查（crud）
- 国际化

总结：

1. 再springboot，我们可以使用一下方式处理静态资源
   - webjars     localhost:8080/webjars/
   - public,static,/**,resources   localhost:8080/
2. 优先级：resources   >   static   >   public

首页定制：

图标定制：

### 模板引擎

结论：只要需要使用thymeleaf，只需要导入对应的依赖就可以了，将html放在templates路径下。

```xml
<dependency>
    <groupId>org.thymeleaf</groupId>
    <artifactId>thymeleaf-spring5</artifactId>
</dependency>
<dependency>
    <groupId>org.thymeleaf.extras</groupId>
    <artifactId>thymeleaf-extras-java8time</artifactId>
</dependency>
```

html所有的属性都可以被thymeleaf接管

```html

```



### 国际化

1. 首页配置：
   1. 注意点，所有页面的静态资源都需要使用thymeleaf接管；
   2. url：@{}
2. 页面国际化：注意点：
   1. 需要配置i18n文件
   2. 如果需要在项目中进行自动化切换，需要自定义一个租金啊LocaleResolver
   3. 记得将自己写的组件配置到spring容器@Bean中
   4. 变量名：#{}
3. 登录 + 拦截器
4. 员工列表展示
   1. 提取公共页面
      1. `th:fragment="sidebar"`
      2. `th:insert="~{commons/commons::sidebar}"`
      3. 如果要传递参数，可以直接使用()传参，接收判断即可
   2. 列表循环展示
5. 添加员工
   1. 按钮提交
   2. 跳转到添加页面
   3. 添加员工成功
   4. 返回首页
6. CRUD搞定

### 编写网站

#### 前端搞定：页面长什么样子，数据

#### 设计数据库（难点）

#### 前端让他能够自动运行，独立化工程

#### 数据接口如何对接：json，对象 all in one

#### 前后端联调测试



需要有一套自己熟悉的后台模板：工作必要 x-admin

前端界面：至少自己能够通过前端框架，组合出来一个网站页面

	- index	首页
	- about
	- blog
	- post
	- user

让网站能够独立运行

### 整合jdbc



### 整合mybatis

![image-20210105160140641](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20210105160140641.png)

整合包：



1. 导入包

   `mybatis-spring-boot-starter`

2. 配置文件application.yml（此处使用的为yml文件，也可以使用properties文件）

   ```yml
   mybatis:
     type-aliases-package: com.kuang.pojo
     mapper-locations: classpath:mybatis/mapper/*.xml
   ```

3. mybatis配置

   在resource包下创建包mybatis

4. 编写sql

   上述包下创建mapper包，在里面编写UserMapper.xml文件

   ```xml
   <?xml version="1.0" encoding="UTF-8" ?>
   <!DOCTYPE mapper
           PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
           "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
   <mapper namespace="com.kuang.mapper.UserMapper">
       <select id="queryUserList" resultType="User">
           select * from user;
       </select>
   </mapper>
   ```

5. service层调用dao层

6. controller调用service层

### SpringSecurity（安全）

在web开发中，安全第一！过滤器，拦截器

功能性需求：否

做网站：安全应该在什么时间考虑（设计网站之初）

- 漏洞，隐私泄露
- 架构一旦确定，再考虑安全，需要修改大量东西

框架：shiro、SpringSecurity

认证、授权

- 功能权限
- 访问权限
- 菜单权限
- 拦截器、过滤器：大量的原生代码

MVC-SPRING-SPRINGBOOT-框架思想

Spring Security是针对Spring项目的安全框架，也是Spring Boot底层安全模块默认的技术选型，它可以实现强大的web安全控制，对于安全控制，我们仅需要引入spring-boot-start-security模块，进行少量配置，即可实现强大的安全管理

记住几个类：

- WebSecurityConfigurerAdapter：自定义Security策略
- Auth
- @

Spring Security的两个主要目标是“认证”和“授权”（访问控制）

“认证”（Authentication）

“授权”（Authorization）

通用概念，不只在Spring Security中存在

==使用==

导入包

```xml
<dependency>
    <groupId>org.thymeleaf.extras</groupId>
    <artifactId>thymeleaf-extras-springsecurity5</artifactId>
</dependency>
```

创建config文件夹，建类

```java
package com.kuang.config;

import org.springframework.security.config.annotation.authentication.builders.AuthenticationManagerBuilder;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter;
import org.springframework.security.crypto.bcrypt.BCryptPasswordEncoder;

// 交给spring托管
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {
    //授权
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        //首页所有人可以访问，功能页只有对应权限的人才能访问
        //请求授权的规则
        http.authorizeRequests()
                .antMatchers("/").permitAll()
                .antMatchers("/level1/**").hasRole("vip1")
                .antMatchers("/level2/**").hasRole("vip2")
                .antMatchers("/level3/**").hasRole("vip3");
        //没有权限默认会控制登录页面，开启登录的页面
        //定制登陆页面，设定自定义首页之后，注销功能失效，需要把注销功能改为post请求，或将csrf关闭
        http.formLogin().loginPage("/tologin");
        //注销，开启了注销功能，跳到首页
        http.logout().logoutSuccessUrl("/");
        //防止网站工具：get，post
        //http.csrf().disable();  //关闭csrf功能

        //开启记住我功能，cookie，默认保存两周
        http.rememberMe().rememberMeParameter("remember");
    }

    //认证，springboot 2.1.x可以直接使用
    //密码编码：passwordEncoder
    //在spring security5.0+中，新增许多加密方法，使用时必须先加密
    @Override
    protected void configure(AuthenticationManagerBuilder auth) throws Exception {

        //这些数据正常情况应该从数据库中读取
        auth.inMemoryAuthentication().passwordEncoder(new BCryptPasswordEncoder())
                .withUser("kuang").password(new BCryptPasswordEncoder().encode("123456")).roles("vip2","vip3")
                .and()
                .withUser("root").password(new BCryptPasswordEncoder().encode("123456")).roles("vip1","vip2","vip3")
                .and()
                .withUser("guest").password(new BCryptPasswordEncoder().encode("123456")).roles("vip1");

    }
}
```

### Shiro

1. 导入依赖

   ```xml
   <!-- https://mvnrepository.com/artifact/org.apache.shiro/shiro-core -->
   <dependency>
       <groupId>org.apache.shiro</groupId>
       <artifactId>shiro-core</artifactId>
       <version>1.7.0</version>
   </dependency>
   <!-- https://mvnrepository.com/artifact/org.slf4j/jcl-over-slf4j -->
   <dependency>
       <groupId>org.slf4j</groupId>
       <artifactId>jcl-over-slf4j</artifactId>
       <version>2.0.0-alpha1</version>
   </dependency>
   <!-- https://mvnrepository.com/artifact/org.slf4j/slf4j-log4j12 -->
   <dependency>
       <groupId>org.slf4j</groupId>
       <artifactId>slf4j-log4j12</artifactId>
       <version>2.0.0-alpha1</version>
       <scope>test</scope>
   </dependency>
   <dependency>
       <groupId>log4j</groupId>
       <artifactId>log4j</artifactId>
       <version>1.2.17</version>
   </dependency>
   ```

2. 配置文件

   

3. HelloWorld

### Springboot 整合 shiro

shiro三大对象

```text
Subject 用户
SecurityManager 管理所有用户
Realm   连接数据
```

1. 导入依赖

   ```xml
   <dependency>
       <groupId>org.apache.shiro</groupId>
       <artifactId>shiro-spring</artifactId>
       <version>1.7.0</version>
   </dependency>
   ```

2. 编写配置类（config.ShiroConfig.java）

   ```java
   @Configuration
   public class ShiroConfig {
   
       //ShiroFilterFactoryBean过滤对象
       @Bean
       public ShiroFilterFactoryBean getShiroFilterFactoryBean(@Qualifier("securityManager") DefaultWebSecurityManager defaultWebSecurityManager) {
           ShiroFilterFactoryBean bean = new ShiroFilterFactoryBean();
           //设置安全管理器
           bean.setSecurityManager(defaultWebSecurityManager);
           //添加shiro的内置过滤器
           /*
           anon：无需认证就可以访问
           authc：必须认证了才能访问
           user：必须拥有 记住我 功能才能用
           perms：拥有对某个资源的权限才能访问
           role：拥有某个角色权限才能访问
            */
           Map<String, String> filterMap = new LinkedHashMap<>();
   //        filterMap.put("/user/add","authc");
   //        filterMap.put("/user/update","authc");
           filterMap.put("/user/*", "authc");
           bean.setFilterChainDefinitionMap(filterMap);
           //设置自定义登陆界面
           bean.setLoginUrl("/toLogin");
           return bean;
       }
   
       //DefaultWebSecurityManager
       @Bean(name = "securityManager")
       public DefaultWebSecurityManager getDefaultWebSecurityManager(@Qualifier("userRealm") UserRealm userRealm) {
           DefaultWebSecurityManager securityManager = new DefaultWebSecurityManager();
           //关联UserRealm
           securityManager.setRealm(userRealm);
           return securityManager;
       }
   
       //创建realm对象，需要自定义类
       @Bean
       public UserRealm userRealm() {
           return new UserRealm();
       }
   }
   ```

3. 自定义类UserRealm，继承AuthorizingRealm，重写方法

   ```java
   public class UserRealm extends AuthorizingRealm {
       //授权
       @Override
       protected AuthorizationInfo doGetAuthorizationInfo(PrincipalCollection principalCollection) {
           System.out.println("执行了=》授权");
           return null;
       }
   
       //认证
       @Override
       protected AuthenticationInfo doGetAuthenticationInfo(AuthenticationToken authenticationToken) throws AuthenticationException {
           System.out.println("执行了=》认证");
           //用户名，密码（实际应该是从数据库中获取）
           String name = "123";
           String password = "123";
           UsernamePasswordToken usernamePasswordToken = (UsernamePasswordToken) authenticationToken;
           if (!usernamePasswordToken.getUsername().equals(name)) {
               return null;    //抛出异常 UnknownAccountException
           }
   
           //密码认证，shiro自动做
           return new SimpleAuthenticationInfo("", password, "");
       }
   }
   ```

4. 编写需要跳转的页面

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <title>Title</title>
   </head>
   <body>
   <h1>add</h1>
   </body>
   </html>
   ```

5. 拦截，添加shiro的内置过滤器（代码于第二步中）

6. 登陆页面

   ```html
   <!DOCTYPE html>
   <html lang="en" xmlns:th="http://www.thymeleaf.org">
   <head>
     <meta charset="UTF-8">
     <title>Title</title>
   </head>
   <body>
   <h1>登录</h1>
   <hr>
   <p th:text="${msg}" style="color: red"></p>
   <form th:action="@{/login}">
       <p>用户名：<input type="text" name="username"></p>
       <p>密码：<input type="text" name="password"></p>
       <p><input type="submit" placeholder="登录"></p>
   </form>
   </body>
   </html>
   ```

7. 认证用户

   在controller文件中，验证信息

   ```java
   @RequestMapping("/login")
   public String login(String username, String password, Model model){
       //获取当前的用户
       Subject subject = SecurityUtils.getSubject();
       //封装用户的登录数据
       UsernamePasswordToken token = new UsernamePasswordToken(username, password);
   
       try{
           subject.login(token);   //执行登录方法，如果没有异常就登录成功
           return "index";
       }catch (UnknownAccountException e){ //用户名不存在
           model.addAttribute("msg","用户名错误");
           return "login";
       }catch (IncorrectCredentialsException e){   //密码不存在
           model.addAttribute("msg","密码错误");
           return "login";
       }
   }
   ```

   第三步中，认证除了return的都是该步

8. 整合mybatis

   导入包：

   ```xml
   <dependency>
       <groupId>mysql</groupId>
       <artifactId>mysql-connector-java</artifactId>
   </dependency>
   <dependency>
       <groupId>log4j</groupId>
       <artifactId>log4j</artifactId>
       <version>1.2.17</version>
   </dependency>
   <dependency>
       <groupId>com.alibaba</groupId>
       <artifactId>druid</artifactId>
       <version>1.1.10</version>
   </dependency>
   <dependency>
       <groupId>org.mybatis.spring.boot</groupId>
       <artifactId>mybatis-spring-boot-starter</artifactId>
       <version>2.1.4</version>
   </dependency>
   ```

   编写mybatis配置文件

   ```yml
   spring:
     application:
       # 应用名称
       name: springboot-05-mybatis
   
     datasource:
       # 数据库驱动：
       driver-class-name: com.mysql.cj.jdbc.Driver
       # 数据源名称
       name: defaultDataSource
       # 数据库连接地址
       url: jdbc:mysql://localhost:3306/ssm_crud?serverTimezone=UTC
       # 数据库用户名&密码：
       username: root
       password: 123456
   
         #Spring Boot 默认是不注入这些属性值的，需要自己绑定
         #druid 数据源专有配置
         initialSize: 5
         minIdle: 5
         maxActive: 20
         maxWait: 60000
         timeBetweenEvictionRunsMillis: 60000
         minEvictableIdleTimeMillis: 300000
         validationQuery: SELECT 1 FROM DUAL
         testWhileIdle: true
         testOnBorrow: false
         testOnReturn: false
         poolPreparedStatements: true
   
         #配置监控统计拦截的filters，stat:监控统计、log4j：日志记录、wall：防御sql注入
         #如果允许时报错  java.lang.ClassNotFoundException: org.apache.log4j.Priority
         #则导入 log4j 依赖即可，Maven 地址：https://mvnrepository.com/artifact/log4j/log4j
         filters: stat,wall,log4j
         maxPoolPreparedStatementPerConnectionSize: 20
         useGlobalDataSourceStat: true
         connectionProperties: druid.stat.mergeSql=true;druid.stat.slowSqlMillis=500
   
   server:
     # 应用服务 WEB 访问端口
     port: 8080
   
   mybatis:
     type-aliases-package: com.kuang.pojo
     mapper-locations: classpath:mybatis/mapper/*.xml
   ```

   

   

   asdfadkljf 

   

9. 

## Swagger

学习目标：

- 了解Swagger的作用和概念
- 了解前后端分离
- 在SpringBoot中继承Swagger

前后端分离

- 后端：后端控制层、服务层、数据访问层
- 前端：前端控制层、视图层
- 前后端如何交互？ ===》API
- 前后端相对独立，松耦合
- 前后端甚至可以部署在不同的服务器上



产生一个问题：

- 前后端集成联调，前端人员和后端人员无法做到“及时协商，尽早解决”，最终问题爆发

解决方案

- 首先指定schema（计划），实时更新最新API，降低继承的风险
- 早些年：指定word计划文档
- 前后端分离：
  - 前端测试后端接口：postmen
  - 后端提供接口，需要实时更新最新的消息及改动



swagger：

- 号称世界上最流行的API框架
- RestFul Api文档在线自动生成工具 =》API文档与API定义同步更新
- 直接运行，可以在线测试API接口
- 支持多种语言



在项目中使用swagger需要springbox

- swagger2
- ui



### SpringBoot集成Swagger

1. 新建一个SpringBoot web项目

2. 导入相关依赖

   ```xml
   <dependency>
       <groupId>io.springfox</groupId>
       <artifactId>springfox-boot-starter</artifactId>
       <version>3.0.0</version>
   </dependency>
   ```

3. 编写helloWorld

4. 配置Swagger ===》Config

   ```java
   @Configuration  //表明是个配置类
   public class SwaggerConfig {
   
   }
   ```

5. 测试运行：访问：http://localhost:8080/swagger-ui/

6. 编写配置类（完成第四步的类）

   ```java
   package com.kuang.swagger.config;
   
   import org.springframework.context.annotation.Bean;
   import org.springframework.context.annotation.Configuration;
   import springfox.documentation.oas.annotations.EnableOpenApi;
   import springfox.documentation.service.ApiInfo;
   import springfox.documentation.service.Contact;
   import springfox.documentation.spi.DocumentationType;
   import springfox.documentation.spring.web.plugins.Docket;
   import springfox.documentation.swagger2.annotations.EnableSwagger2;
   
   import java.util.ArrayList;
   
   @Configuration  //表明是个配置类
   public class SwaggerConfig {
   
       //配置了Swagger的Docket的bean实例
       @Bean
       public Docket docket() {
           return new Docket(DocumentationType.OAS_30)
                   .apiInfo(apiInfo());
       }
   
       //配置Swagger信息apiInfo
       private ApiInfo apiInfo(){
           //作者信息
           Contact contact = new Contact("秦疆","https://www.baidu.com","123456789.@qq.com");
           return new ApiInfo(
                   "狂神的Swagger API文档",
                   "学如逆水行舟，不进则退",
                   "v1.0",
                   "https://blog.kuangstudy.com/",
                   contact,
                   "Apache 2.0",
                   "http://www.apache.org/licenses/LICENSE-3.0",
                   new ArrayList()
           );
       }
   }
   ```

7. 

### Swagger配置扫描接口

配置接口

.select().apis().build()：为完整一套，中间不能加别的（如enable（））

==.enable()：是否开启==

```java
//配置了Swagger的Docket的bean实例
@Bean
public Docket docket() {
    return new Docket(DocumentationType.OAS_30)
            .apiInfo(apiInfo())
        	.enable(false)  //是否启用swagger，false则不能在浏览器中访问
            .select()
            //RequestHandlerSelectors配置要扫描接口的方式
            //  basePackage()：指定要扫描的包
            //  any()：扫描全部
            //  none()：不扫描
            //  withClassAnnotation()：扫描类上的注解，参数是一个注解的反射对象
            //  withMethodAnnotation()：扫描方法上的注解
          .apis(RequestHandlerSelectors.basePackage("com.kuang.swagger.controller"))
            .paths(PathSelectors.ant("/kuang/**"))
            .build();
}
```

判断配置是否启动

```java
//设置要显示的swagger环境
Profiles profiles = Profiles.of("dev","test");

//判断是否在自己设定的环境当中，用于下面是否开启swagger（用户使用时不需要开启）
boolean b = environment.acceptsProfiles(profiles);
```

完整配置类：

```java
package com.kuang.swagger.config;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.core.env.Environment;
import org.springframework.core.env.Profiles;
import springfox.documentation.builders.PathSelectors;
import springfox.documentation.builders.RequestHandlerSelectors;
import springfox.documentation.oas.annotations.EnableOpenApi;
import springfox.documentation.service.ApiInfo;
import springfox.documentation.service.Contact;
import springfox.documentation.spi.DocumentationType;
import springfox.documentation.spring.web.plugins.Docket;
import springfox.documentation.swagger2.annotations.EnableSwagger2;

import java.util.ArrayList;

/**
 * @author JSQ
 * @ClassName SwaggerConfig.java
 * @Description TODO
 * @createTime 2021年01月10日 17:27:00
 */
@Configuration  //表明是个配置类
public class SwaggerConfig {

    //配置了Swagger的Docket的bean实例
    @Bean
    public Docket docket(Environment environment) {
        //设置要显示的swagger环境
        Profiles profiles = Profiles.of("dev","test");

        //判断是否在自己设定的环境当中，用于下面是否开启swagger（用户使用时不需要开启）
        boolean b = environment.acceptsProfiles(profiles);

        return new Docket(DocumentationType.OAS_30)
                .apiInfo(apiInfo())
                .enable(b)  //是否启用swagger，false则不能在浏览器中访问
                .select()
                //RequestHandlerSelectors配置要扫描接口的方式
                //  basePackage()：指定要扫描的包
                //  any()：扫描全部
                //  none()：不扫描
                //  withClassAnnotation()：扫描类上的注解，参数是一个注解的反射对象
                //  withMethodAnnotation()：扫描方法上的注解
                .apis(RequestHandlerSelectors.basePackage("com.kuang.swagger.controller"))
                //.paths(PathSelectors.ant("/kuang/**"))
                .build();
    }

    //配置Swagger信息apiInfo
    private ApiInfo apiInfo(){
        //作者信息
        Contact contact = new Contact("秦疆","https://www.baidu.com","123456789.@qq.com");
        return new ApiInfo(
                "狂神的Swagger API文档",
                "学如逆水行舟，不进则退",
                "v1.0",
                "https://blog.kuangstudy.com/",
                contact,
                "Apache 2.0",
                "http://www.apache.org/licenses/LICENSE-3.0",
                new ArrayList()
        );
    }
}
```

配置API分组

```java
.groupName("狂神")
```

如何配置多个分组；编写多个Docket实例

```java
@Bean
public Docket docket(Environment environment) {
    return new Docket(DocumentationType.OAS_30)
            .groupName("狂神");
}
```

实体类

```java
@ApiModel("用户实体类")
public class User {
    @ApiModelProperty("用户名")
    public String username;
    @ApiModelProperty("密码")
    public String password;
}
```

总结：

1. 我们可以通过Swagger给一些难以理解的属性或接口，增加注释信息
2. 接口文档实时更新
3. 可以在线测试、

==在正式发布时，关闭swagger，1. 安全	2. 节省内存==

## 任务

异步任务

定时任务

邮件任务

## 分布式Dubbo + Zookeeper + SpringBoot

步骤：

前提：zookeeper服务开启

1. 提供者提供服务
   1. 导入依赖
   2. 配置注册中心
   3. 在想要被注册的服务上面增加一个@Service（dubbo的）
2. 消费者如何消费
   1. 导入依赖
   2. 配置注册中心的地址，配置自己的服务名
   3. 从远程注入服务（@DubboReference）



## 总结

```
三层架构	+	MVC	
	架构 --》 解耦
	
开发架构
	Spring
		IOC：控制反转
			买房例子：
				原始：选址，打桩，准备砖石、水泥等等，搭建，住房
				IOC：选址，住房
			将所编写的所有东西都放进ioc容器中，什么地方需要使用就直接取出来用，不需要重新在建造
		AOP：切面（本质，动态代理）
			目的：不影响业务本来的情况下，实现动态增加功能，大量应用在日志、事务等方面
		轻量级开源框架，容器
		目的：解决企业开发的复杂性问题
		但是逐渐配置文件变复杂
		
	SpringBoot
		本质是spring的升级版
		新一代javaee开发标准，自动配置东西，开箱即用
		自动配置-》约定大于配置
		
微服务架构-->新架构
	原因：如淘宝，拥有用户、签到、小游戏、选择商品、支付等等很多服务，使用springboot将在同一个服务器下，用户多的时候服务器将出现卡顿甚至崩溃
	目的：模块化，功能化
	服务1占用90%	服务2占用10%	--负载均衡-->	服务1占用50%	服务2占用50%
	
微服务架构问题：
	1.这么多服务，客户端如何访问
	2.这么多服务，服务之间如何通信
	3.这么多服务，如何治理
	4.服务挂了怎么办
	
解决方案：
	SpringCloud，一套生态，用来解决上述问题，基于springboot
	1.Spring Cloud  NetFlix	一站式解决方案
	2.Apache Dubbo zookeeper	
	3.SpringCloud Alibaba 一站式解决方案
	
	1.API网关，服务路由
	2.HTTP，RPC框架，异步调用
	3.服务注册与发现，高可用
	4.熔断机制，服务降级
```





## SpringCloud

## 看开源项目

### GIT

![image-20201202200908278](C:\Users\江尚奇\AppData\Roaming\Typora\typora-user-images\image-20201202200908278.png)