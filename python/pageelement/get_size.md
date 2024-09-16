# get_size
```python
def get_size(self, timeout: int = 30) -> ElementSize
```

获取目标元素的大小（长宽）。

**参数:**   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;ElementSize 对象, 类定义如下: 
```python
    class ElementSize:

    def __init__(self, width, height) -> None:
        self.Width = width
        self.Height = height
```

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator
from json
    
size = sw.find_element(locator.bing.search_sb_form_q).get_size()
print(json.dumps(size.__dict__))

# output: {"Width": 500, "Height": 40}

```