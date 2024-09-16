---
sidebar_position: 2
sidebar_label: Web Automation 
---
# 网页自动化 
## 概述

Swifthorse Web 自动化支持以行的 Web 浏览器：Chrome、Microsoft Edge。
在录制和运行之前，需要先安装浏览器扩展，通过pyhton接口可以直接安装。
在录制过程中，当您录制 Web 浏览器页面时，Swifthorse 将自动检测并选择合适的 Web 自动化来录制元素。

## 选择器属性
请先了解 [locator](./locator.md) 概念和定义. 对于UIA自动化，支持的属性列表如下:

## Page

| Name      | equals | contains |startWith |endWith | regex
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Title |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| URL |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## Web

| Name      | equals | contains |startWith |endWith | regex
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Id |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Type |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AncestorId |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AncestorName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| CssSelector |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Class |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AncestorClass |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| SInfo |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| TabIndex |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Href |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Src |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Title |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| XPath |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Tag |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| TableRow |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| TableCol |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsLeaf |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## 网页元素属性
通过 [find_element](../references/python/globalfunctions/find_element.md) 可以获取到MSAA元素, 然后通过 [get_property](../references/python/pageelement/get_property.md)可以获取元素属性, Swifthorse web 支持获取以下属性:

| Name      | Description |
| ----------- | ----------- |
| pagetitle      |页面标题|
| readystate      |网页的加载状态，如果 Document.readyState 等于 “complete” 则返回 1 或返回 0|
| ID     |网页元素属性'id'|
| URL      |页面网址|
| htmlwindowname      |`window.name`|
| title      |网页元素属性'title'|
| cookie      |当前页面的所有cookie|
| innertext      |元素的innertext|
| innertextshort      |innertext前512个字符|
| outertext      |元素的outertext|
| outertextshort      |outertext前512个字符|
| innerhtml      |元素的innerhtml|
| innerhtmlshort      |innerhtml前512个字符|
| outerhtml      |元素的outerhtml|
| outerhtmlshort      |outerhtml前512个字符|
| tag      |网页元素属性'tag'|
| ancestorid |DOM树上某个父元素的id属性|
| ancestorname      |DOM树上某个父元素的name属性|
| ancestorcss      |DOM树上某个父元素的class属性|
| tablerow      |如果元素在一个表格中，返回所在的行|
| tablecol      |如果元素在一个表格中，返回所在的列|
| rowname      |行标题名称|
| colname      |列标题名称|
| columncount      |列的总数|
| rowcount      |行的总数|
| ischecked      |元素(checkbox, radio) 是否选中|
| sinfo      |元素显示的文本内容|
| sinfoshort      |元素显示的文本内容前512个字符|
| css_selector      |css selector|
| class      |class属性|
| selecteditem      |下拉框选项|
| selecteditems      |多个下拉框选项|
| isleaf      |元素在DOM树上是否是叶子节点|
| tabindex      |tabindex属性|
| href      |href属性 |
| XPath      |元素的xpath值|
| Type      |type属性|
| Src      |src 属性|
| Role      |role 属性|
| Name      |name 属性|
