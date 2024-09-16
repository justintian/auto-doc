---
sidebar_position: 5
sidebar_label: move
---

# swifthorse.mouse.move

```python
def move(
        self,
        x: int, 
        y: int
    ) -> None
```  

移动鼠标。

**参数:**  
    &emsp;**x[必需]**: int  
        &emsp;&emsp; 横坐标位置  
    &emsp;**y[必需]**: int  
        &emsp;&emsp; 纵坐标位置    

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# Move the mouse to position (100,100)
sw.mouse.move(100,100)

```