
# MSAA 自动化
## 概述

Swifthorse MSAA 自动化基于 Microsoft Active Accessibility （MSAA） 来支持记录功能、定位符和对元素的所有操作。
由于 MSAA 现在被认为是legacy API，我们将 MSAA 视为 UIA 的补充，在某些 Electron&CEF 应用程序或legacy应用程序上，MSAA 可能会更好。如果您想在录制过程中使用 MSAA，请手动选择 MSAA 技术。

## 选择器属性
请先了解 [locator](./locator.md) 概念和定义. 对于MSAA自动化，支持的属性列表如下:

| 名称      | equals | contains |startWith |endWith |regex |
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| HelpText |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AccessKey |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| DefaultAction |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Description |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsDirectChild |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Tag |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|


## MSAA 元素属性
通过 [find_element](../references/python/globalfunctions/find_element.md) 可以获取到MSAA元素, 然后通过 [get_property](../references/python/pageelement/get_property.md)可以获取元素属性, Swifthorse MSAA 支持获取以下属性:


| 名称      | 描述 |
| ----------- | ----------- |
| Name      |  UI元素名称      |
| IsEnabled  | UI元素是否可用|
| AccessKey   |  UI元素的快捷键属性|
| BoundingRectangle   | UI元素的大小和位置信息|
| ProcessId   | UI元素所在的应用进程id|
| Description   |  UI元素的描述|
| AcceleratorKey   | 字符串，其中包含元素的加速键组合|
| HelpText   |UI元素的帮助信息|
| ControlType | UI元素控件类型|
