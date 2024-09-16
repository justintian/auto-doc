# get_position
```python
def get_position(self, timeout: int = 30) -> ElementPosition
```

获取元素位置。

**参数:**   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;ElementPosition 对象, 类定义如下: 
```python
    class ElementPosition:

    def __init__(self, left, top, right, bottom):
        self.Left = left
        self.Top = top
        self.Right = right
        self.Bottom = bottom
```

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator
from json
    
position = sw.find_element(locator.bing.search_sb_form_q).get_position()
print(position.__dict__)

# output: {"Left": 400, "Top": 300, "Right": 900, "Bottom": 330}

```