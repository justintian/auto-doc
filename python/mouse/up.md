---
sidebar_position: 3
sidebar_label: up
---

# swifthorse.mouse.up

```python
def up(
        self,
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = "left"
    ) -> None
```

在屏幕指定的位置将鼠标松开。

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

sw.mouse.up(100,100)

```