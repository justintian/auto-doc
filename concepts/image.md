
# 图像识别自动化

## 概述
Swifthorse自动化与许多图像自动化功能集成。当常规的自动化技术没法定位到某个应用的界面元素时，图像识别是一个不错的选择。

## 图像选择器

图像选择器包含两个部分。 
第一部分是锚点元素。在运行过程中，首先找到锚点元素，然后根据 image 方法属性捕获 锚点元素的屏幕截图，通过图像匹配算法在锚点元素截图中找到目标图像。
第二部分是具有以下属性的图像本身：  

|姓名 |描述 | equals | contains |startWith |endWith |
|----------- |----------- |----------- |----------- |----------- |----------- |
|accuracy |目标图像与锚点元素的屏幕截图之间的最小相似度。当要找到的图像与锚点元素的屏幕截图略有不同时，此功能非常有用。测量单位介于 0 和 1 之间，默认值为 0.75。|<font color="Green"><B>是</B></font> |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|
|dpi | 建议开发和最终运行的电脑的 Windows 操作系统的 DPI 一致 |<font color="Green"><B>是</B></font> |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|
|method	 |图像匹配的算法。记录时自动设置该值 |<font color="Green"><B>是</B></font> |<font color="Red"><B>否</B></font> |<font color="Red"><B>否</B>|<font color="Red"><B>否</B>|
| filePath | 需要匹配的图像文件名 |<font color="Green"><B>是</B></font>   |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|
| matchIndex | 如果图像匹配到多个，选中的序号,默认为0，表示选择第一个匹配的区域 |<font color="Green"><B>是</B></font>   |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|
| elementRect | 记录锚点元素的大小，无需改动 |<font color="Green"><B>是</B></font>   |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|
| selectionRect | 记录选中的区域位置，无需改动 |<font color="Green"><B>是</B></font>   |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|
| timeout |图像匹配的超时时间，默认为5000毫秒  |<font color="Green"><B>是</B></font>   |<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|<font color="Red"><B>否</B></font>|

支持的图像匹配算法:
- HighestAccuracy: 与整个屏幕比较，选取最匹配的区域。
- InRegionHighestAccuracy: 在锚点元素区域以内进行匹配，选取最匹配的区域。
- OutRegionHighestAccuracy: 在锚点元素区域以外进行匹配，选取最匹配的区域。

`method` 属性是在录制过程中由录制器自动选择的，
如果选中的区域在锚点元素区域以内，会设置为'InRegionHighestAccuracy';  
如果选中的区域与锚点元素区域有部分交集，会设置为 'HighestAccuracy';
如果选中的区域完全在锚点元素区域之外，会设置为  'OutRegionHighestAccuracy';

## 在流程中使用图像选择器
图像选择器跟其他选择器的使用方式一样

```python
from swifthorse import swifthorse as sw, locator


#open new browser window
driver = sw.chrome.open("https://www.bing.com")
driver.find_element(locator.chrome.img1).click

sw.find_element(locator.notepad.menuitem).click()
```  

以下的操作支持使用图像选择器:
- click
- double_click
- mouse_up
- mouse_down
- drag_drop
- get_position
- get_size
- highlight
- hover
- send_keys
- input_text (参数 `by` 必须设置为 `input-after-click`)