# mouse_down 
```python
def mouse_down(
        self,
        mouse_button: Literal["left", "middle", "right"] = "left",
        location: Literal['center', 'left-top', 'left-bottom', 'right-top', 'right-bottom'] = "center",
        Xoffset: int = 0,
        Yoffset: int = 0,
        Xrate: float = 0,
        Yrate: float = 0,
        by: Literal["default", "mouse-emulation", "control-invocation"] = "default",
        modifier_key: Literal["none", "alt", "ctrl", "shift","win"]  ="none",
        timeout: int = 30
    ) -> None
```  

在目标元素上按下鼠标 

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
    &emsp;**modifier_key**: 辅助键  
        &emsp;&emsp; 在点击的同时，按下辅助键("alt", "ctrl", "shift", "win") ，默认为`none`，表示不按辅助键     
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

sw.find_element(locator.bing.svg).mouse_down(mouse_button = "left")
```