# child
```python
def child(self, index: int)
```  

获取指定序号的子元素

> **注意:**
>- 序号是从0开始计数的。

**参数:**    
    &emsp;**index[必需]**: int  
        &emsp;&emsp; 指定的序号, 获取第index个子元素

**返回值:**  
    &emsp;如果元素存在，返回[PageElement](./pageelement.md) 对象, 否则返回None

**异常:**  
    &emsp;参见[异常定义](../exceptions/exceptions.md)

**示例:**

```python
from swifthorse import swifthorse as sw, locator
    
ele = sw.find_element(locator.bing.li_dots_overflow)
first_child = ele.child(0)
```