---
sidebar_position: 5
sidebar_label: find_element_by_css_selector
---
# WebElement.find_element_by_css_selector
```python
def find_element_by_css_selector(
        self,
        css_selector: str,
        timeout: int = 30
    ) -> WebElement
``` 

根据指定css_selector定位网页元素，如果匹配多个，默认返回第一个。

**参数:**  
    &emsp;**css_selector[必需]**: str     
        &emsp;&emsp; CSS selector 字符串  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;[WebElement](./webelement.md)对象。

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

# find elements by CSS selector
element = page.find_element_by_css_selector("#sb_form")

# find sub elements by CSS selector
webelement = element.find_element_by_css_selector("svg")
webelement.highlight()

```