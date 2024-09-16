# click 
```python
def click(
        self,
        mouse_button: Literal["left", "middle", "right"] = "left",
        location: Literal['center', 'left-top', 'left-bottom', 'right-top', 'right-bottom'] = "center",
        Xoffset: int = 0,
        Yoffset: int = 0,
        Xrate: float = 0,
        Yrate: float = 0,
        by: Literal["default", "mouse-emulation", "control-invocation"] = "default",
        modifier_key: Literal["none", "alt", "ctrl", "shift","win"]  = "none",
        timeout: int = 30
    ) -> None
```  

Single click the target element.

**参数:**  
    &emsp;**mouse_button**:  
        &emsp;&emsp; 有效值为: 'left', 'right' 和 'center',默认为 'left'，左键点击.  
    &emsp;**location**:  
        &emsp;&emsp; 鼠标在目标元素上点击的位置. 有效值为:  'center', 'left-top', 'left-bottom', 'right-top' 和 'right-bottom', 默认为 'center'，点击在元素的中心位置.  
    &emsp;**Xoffset**: int   
        &emsp;&emsp; 横坐标偏移的像素数，默认为 0。 正数表示向右偏移，负数表示向左偏移。  
    &emsp;**Yoffset**: int  
        &emsp;&emsp; 纵坐标偏移的像素数，默认为 0。 正数表示向下偏移，负数表示向上偏移。  
    &emsp;**Xrate**: float  
        &emsp;&emsp; 横坐标偏移比例（相对于目标元素宽度）。 默认为0，正数表示向右偏移，负数表示向左偏移。  
    &emsp;**Yrate**: float  
        &emsp;&emsp; 纵坐标偏移比例（相对于目标元素宽度）。 默认为0，正数表示向下偏移，负数表示向上偏移。
    &emsp;**by**:   
        &emsp;&emsp; 点击使用的方法。  
        &emsp;&emsp; `mouse-emulation`: 模拟鼠标点击，鼠标会被移动到目标元素上， 
        &emsp;&emsp; `control-invocation`: 使用元素内置的功能，例如web元素使用js事件调用的方式，桌面元素使用invoke-pattern的方式，一些桌面元素可能不支持该方式.  
        &emsp;&emsp; `default`: 由程序自动根据目标元素类型自动选择，例如网页元素默认用`control-invocation`; 桌面元素默认用 `mouse-emulation`。  
    &emsp;**modifier_key**: 辅助键  
        &emsp;&emsp; 在点击的同时，按下辅助键("alt", "ctrl", "shift", "win") ，默认为`none`，表示不按辅助键      
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;None

**注意**:
> 以下示意图展示点击位置: 
>
> ![sample1](../../../img/location-center-offset.png)
> ![sample2](../../../img/location-lefttop-offset.png)

**示例:**

- 左键点击
***
```python
from swifthorse import swifthorse as sw, locator
sw.find_element(locator.bing.svg).click(mouse_button = "left")

page = sw.chrome.open("https://swifthorse.com")
page.find_element(locator.swifthorse.svg).click(mouse_button = "left")
```

- 自定义点击位置
目标元素为按钮 '5'，通过设定位置参数，我们可以点击其他元素
![sample1](../../../img/click_sample1.png)


```python
from swifthorse import swifthorse as sw, locator

# 点击按钮 '5'
sw.find_element(locator.applicationframe.button_num5butto).click()

# 点击按钮 '6' 
sw.find_element(locator.applicationframe.button_num5butto).click(xrate=1)

# 点击按钮 '8'
sw.find_element(locator.applicationframe.button_num5butto).click(yrate=-1)
```

- 使用辅助键  
windows资源管理器窗口:  
![sample2-1](../../../img/click_sample21.png)  
点击目录test3 `sw.find_element(locator.explorer.edit_system_item).click()`, 然后点击目录test1，
![sample2-2](../../../img/click_sample22.png)  
Click on folder 'test3' as `sw.find_element(locator.explorer.edit_system_item).click(modifier_key=ModifierKey.Ctrl)`, 保证test1，test3都被选中，  
![sample2-3](../../../img/click_sample23.png) 