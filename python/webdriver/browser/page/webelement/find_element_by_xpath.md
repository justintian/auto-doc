
# WebElement.find_element_by_xpath
```python
def find_element_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> WebElement
```  

根据指定xpath定位网页元素，如果匹配多个，默认返回第一个。

**参数:**  
    &emsp;**xpath[必需]**: str     
        &emsp;&emsp; XPath 字符串。 
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;[WebElement](./webelement.md)对象。

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com/images")

# find elements by XPath
element = page.find_element_by_xpath("//*[@id=\"ilp_t\"]")

# find sub element by XPath
subelement = element.find_element_by_xpath(".//*[@id=\"ilp_t\"]/div[1]/div/*")
subelement.highlight()

```