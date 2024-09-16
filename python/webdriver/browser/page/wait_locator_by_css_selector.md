
# Page.wait_appear_by_css_selector
```python
def wait_appear_by_css_selector(
        self,
        css_selector: str,
        wait_timeout: int = 30
    ) -> WebElement
```  

在指定的时间内，等待指定css_selector字符串的网页元素出现。

**参数:**  
    &emsp;**css_selector[必需]**: str     
        &emsp;&emsp; CSS selector 字符串   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;[WebElement](./webelement/webelement.md) 对象, 或者返回None如果元素未出现。

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

#  wait element appear by CSS selector
webelement = page.wait_appear_by_css_selector("#sb_form_q")
if webelement:
    webelement.highlight()

```