
# Page.find_element_by_css_selector
```python
def find_element_by_css_selector(
        self,
        css_selector: str
    ) -> WebElement
```  

根据指定css_selector定位网页元素，如果匹配多个，默认返回第一个。

**参数:**  
    &emsp;**css_selector[必需]**: str     
        &emsp;&emsp; CSS selector 字符串。 

**返回值:**  
    &emsp;[WebElement](./webelement/webelement.md)对象。

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

# find element by CSS selector
webelement = page.find_element_by_css_selector("#sb_form_q")
webelement.highlight()

```