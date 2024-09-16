---
sidebar_position: 1
sidebar_label: click
---

# swifthorse.mouse.click

```python
def click(
        self, 
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] ="left",
        modifier_key: Literal["none", "alt", "ctrl", "shift","win"]  = "none",
        delay: int = 0
    ) -> None
```  

鼠标点击操作

**参数:**  
    &emsp;**x[必需]**: int  
        &emsp;&emsp; 横坐标位置  
    &emsp;**y[必需]**: int  
        &emsp;&emsp; 纵坐标位置  
    &emsp;**mouse_button**:   
        &emsp;&emsp; 鼠标按键，默认是"left"，左键
    &emsp;**modifier_key**: 辅助键  
        &emsp;&emsp;  在点击的同时，按下辅助键("alt", "ctrl", "shift", "win") ，默认为`none`，表示不按辅助键  
    &emsp;**delay**: int  
        &emsp;&emsp; 在鼠标按下和松开之间的持续的时间，单位是秒，默认为0.

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# 在屏幕位置 (100,100)处，鼠标左击
sw.mouse.click(100,100)

```