---
sidebar_position: 16
sidebar_label: wait_disappear_by_css_selector
---
# Page.wait_disappear_by_css_selector
```python
def wait_disappear_by_css_selector(
        self,
        css_selector: str,
        wait_timeout: int = 30
    ) -> bool
```  

在指定的时间内，等待指定css_selector字符串的网页元素出现。

**参数:**  
    &emsp;**css_selector[必需]**: str     
        &emsp;&emsp; CSS selector 字符串   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;如果网页元素消失，返回True， 否则返回False。 

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

#  wait element disappear by CSS selector
result = page.wait_disappear_by_css_selector("#sb_form_q", wait_timeout=5)
print(result)

```