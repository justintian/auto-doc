# drag_drop
```python
def drag_drop(
        self,
        xpoint: int,
        ypoint: int,
        speed: int = 50,
        timeout: int = 30
    ) -> None
```  

按住目标元素，然后拖动到目标位置后再松开鼠标按键。

**参数:**  
    &emsp;**xpoint[必需]**: int    
        &emsp;&emsp; 横坐标移动的像素数  
    &emsp;**ypoint[必需]**: int   
        &emsp;&emsp; 纵坐标移动的像素数  
    &emsp;**speed[可选]**: int  
        &emsp;&emsp; 鼠标拖动的速度, 单位是 ms/10px, 默认值为 50.  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

# 拖动元素向右移动20个像素
sw.find_element(locator.app.bing.scrollbutton).drag_drop(20, 0)
  
# 拖动元素向下移动20个像素
sw.find_element(locator.app.bing.scrollbutton).drag_drop(0, 20)
```
