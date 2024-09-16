
# UIA Automation 
## Overview

Swifthorse UIA 自动化基于 Microsoft UI Automation技术，支持录制功能、生成选择器以及对 UI 元素的所有操作。 
在录制过程中，对于 Windows 应用程序，例如记事本、计算器和 ERP 客户端应用程序，Swifthorse 将使用 UIA 自动化来录制元素。

## 选择器属性
请先了解 [locator](./locator.md) 概念和定义. 对于UIA自动化，支持的属性列表如下:

| Name      | equals | contains |startWith |endWith | regex
| ----------- | ----------- |----------- |----------- |----------- |----------- |
| Name |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| AutomationId |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| ClassName |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| HelpText |  <font color="Green"><B>Yes</B></font>   |<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|<font color="Green"><B>Yes</B></font>|
| Role |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsDirectChild |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AccessKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| IsPassword |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| AcceleratorKey |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| ItemType |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| ItemStatus |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Orientation |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|
| Index |  <font color="Green"><B>Yes</B></font>   |<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|<font color="Red"><B>No</B></font>|

## UIA 元素属性
通过 [find_element](../references/python/globalfunctions/find_element.md) 可以获取到MSAA元素, 然后通过 [get_property](../references/python/pageelement/get_property.md)可以获取元素属性, Swifthorse UIA 支持获取以下属性:

| 名称      | 描述 |
| ----------- | ----------- |
| Name      |  UI元素名称 |
| IsEnabled  | UI元素是否可用 |
| AccessKey   | UI元素的快捷键属性 |
| AutomationId | UI元素的自动化标识符 |
| BoundingRectangle   | UI元素的大小和位置信息|
| ProcessId   | UI元素所在的应用进程id |
| ItemType   | 项类型的描述 |
| IsPassword   |  UI元素是否为内容保护类型控件 |
| IsOffscreen   | UI元素在屏幕上是否可见 |
| AcceleratorKey   | 字符串，其中包含元素的加速键组合|
| HelpText   | UI元素的帮助信息 |
| IsKeyboardFocusable   |UI元素是否支持光标焦点|
| IsContentElement   |UI元素是否为 content element|
| IsControlElement   | |UI元素是否为 control element |
| HasKeyboardFocus   | |UI元素是否获取光标焦点 |
| FrameworkId   | UI框架的名称, 例如 "Win32", "WinForm", 或者 "DirectUI". 大部分元素默认为空。 |
| ControlType | UI元素控件类型 |
