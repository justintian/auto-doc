---
sidebar_position: 6
sidebar_label: scroll
---

# swifthorse.mouse.scroll

```python
def scroll(
        self,
        times = 1,
        modifier_key: Literal["none", "alt", "ctrl", "shift","win"]  = "none"
    ) -> None
```  

滚动鼠标。

**参数:**  
    &emsp;**times**: int  
        &emsp;&emsp; 滚动鼠标滚轮的次数，默认是1. 值为正数表示向上滚动，值为负数表示向下滚动。  
    &emsp;**modifier_key**: 辅助键  
        &emsp;&emsp;  在点击的同时，按下辅助键("alt", "ctrl", "shift", "win") ，默认为`none`，表示不按辅助键    

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

sw.mouse.scroll(2,'ctrl')

```