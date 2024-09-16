---
sidebar_position: 12
sidebar_label: wait_appear_by_xpath
---
# Page.wait_appear_by_xpath
```python
def wait_appear_by_xpath(
        self,
        xpath: str,
        wait_timeout: int = 30
    ) -> WebElement
```  

在指定的时间内，等待指定xpath字符串的网页元素出现。

**参数:**  
    &emsp;**xpath[必需]**: str     
        &emsp;&emsp; XPath 字符串。 
    &emsp;**wait_timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。    

**返回值:**  
    &emsp;[WebElement](./webelement/webelement.md) 对象, 或者返回None如果元素未出现。

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

#  wait element appear by XPath
webelement = page.wait_appear_by_xpath("//*[@id=\"sb_form_q\"]")
if webelement:
    webelement.highlight()

```