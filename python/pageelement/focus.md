# focus
```python
def focus(self, timeout: int = 30) -> None
```  

聚焦到当前页面元素

**参数:**  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。   

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

sw.find_element(locator.bing.search_sb_form_q).focus()
```