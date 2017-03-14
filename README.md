# RES站点首页

## js编码规范 － 强制 {#js-}

* 禁止使用同步ajax
* 必须使用var修饰私有变量
* 判断时必须使用精确的比较操作符 !== 或 ===
* 禁止使用eval
* js语句需分号\(;\)结尾
* 单行注释必须独占一行。//后跟一个空格; 注释缩进与下一行被注释说明的代码一致;注释上一行是空行，紧临下一行代码
* 事件统一通过eventMap管理, jqx相关事件有可能需要自行绑定
* 不允许擅自引入三方JS,引入需经开发经理同意
* \*BS.js负责与后台交互处理数据，\*.js负责事件响应
* 避免在js中写大段html，正确的做法是抽取成单独的html文件，然后在js中引入
* 子页面使用前需使用pushSubView注册
* 缩进，保证可读性\(sublime\),使用空格代替TAB，每次缩进4个空格
* 不再使用BH\_UTILS,使用utils
* 文本内容用双引号包围。（建议）

## css编码规范 － 强制 {#css-}

* css保持全小写，单词间以减号（-）连接，功能模块中的样式命名以目录名-标识名的方式进行标注（如：gnlx-index-search-bar）
* 选择器跟 { 之间必须包含空格
* 属性跟 : 之间不能有空格，: 跟属性值之间必须包含空格
* +、
  &gt;
  、~选择器的两边各保留一个空格。
* 一个rule中有多个选择器时，选择器间必须换行
* 数值为 0 的属性值须省略单位。
* RGB颜色值必须使用十六进制形式 如：\#3f3f3f，能简写成\#333就不许使用 \#333333，颜色值中的英文字母使用小写
* css 选择中DOM节点 id、class 属性赋值时 = 之间不得有空格，属性值必须用双引号包围，不得用单引号。
* id 选择器不需嵌套其他选择器。
* 在可以使用缩写的情况下，尽量使用属性缩写。
* 组件的边距在规范中已经预先定义好，使用代替bh-mh-4、bh-p-8等，代替自己定义的margin,padding样式。

## html编码规范 － 强制 {#html-}

* 不允许出现style属性
* 对于无需闭合的标签（如input,br,img,hr），不允许使用闭合,例如

```
<
!-- good --
>
<
input type="text" name="title"
>
<
!-- bad --
>
<
input type="text" name="title"/
>
```

* HTML5中规定可以省略的闭合类标签，实际使用中不允许省略，例如：

```
<
!-- good --
>
<
ul
>
<
li
>
1st
<
/li
>
<
li
>
2se
<
/li
>
<
/ul
>
<
!-- bad --
>
<
ul
>
<
li
>
1st
    
<
li
>
2se

<
/ul
>
```

* 自定义属性以data-
  _\*_
  命名，强制使用小写字母
* 按钮避免ie9-10回车默认触发事件（ie11没有默认回车事件问题），增加type=button：

```
<
button type=“button”
>
<
button
>
```

  


