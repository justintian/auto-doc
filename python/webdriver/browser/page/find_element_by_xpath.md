
# Page.find_element_by_xpath
```python
def find_element_by_xpath(
        self,
        xpath: str
    ) -> WebElement
```  

根据指定xpath定位网页元素，如果匹配多个，默认返回第一个。  

**参数:**  
    &emsp;**xpath[必需]**: str     
        &emsp;&emsp; XPath字符串。  

**返回值:**  
    &emsp;[WebElement](./webelement/webelement.md) 对象。

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

# find element by XPath
webelement = page.find_element_by_xpath("//*[@id=\"sb_form_q\"]")
webelement.highlight()

```