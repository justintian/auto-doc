---
sidebar_position: 7
sidebar_label: position
---

# swifthorse.mouse.position

```python 
def position(
        self
    ) -> Tuple[int,int]
```

获取当前光标位置。

**参数:**  
    &emsp;None   

**返回值:**  
    &emsp;鼠标当前横坐标和纵坐标位置

**示例:**
***
```python
from swifthorse import swifthorse as sw

# get the position of the mouse cursor
x,y = sw.mouse.position()
print("X integer coordinate is ", x)
print("Y integer coordinate is ", y)
```