---
sidebar_position: 4
sidebar_label: down
---

# swifthorse.mouse.down

```python 
def down(
        self,
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = "left"
    ) -> None
```

将鼠标移动到指定位置，做按下操作

**参数:**  
    &emsp;**x[必需]**: int  
        &emsp;&emsp; 横坐标位置  
    &emsp;**y[必需]**: int  
        &emsp;&emsp; 纵坐标位置  
    &emsp;**mouse_button**:   
        &emsp;&emsp; 鼠标按键，默认是"left"，左键   

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

sw.mouse.down(100,100)

```