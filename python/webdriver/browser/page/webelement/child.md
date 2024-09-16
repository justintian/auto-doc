
# child
```python
def child(self, index: int)
```  

返回指定序号的子元素，当前仅支持web元素。

> **注意:**
>- 序号是从0开始计数的。

**参数:**    
    &emsp;**index[必需]**: int  
        &emsp;&emsp; 指定的序号, 获取第index个子元素

**返回值:**  
    &emsp;如果元素存在，返回[WebElement](./webelement.md) 对象, 否则返回None

**示例:**

```python
from swifthorse import swifthorse as sw, locator
    
page = sw.chrome.open("https://bing.com")

# get web element
ele = page.find_element(locator.bing.search_sb_form_q)

# get element's first child
first_child = ele.child[0]
```