
# WebElement.find_elements_by_css_selector
```python
def find_elements_by_css_selector(
        self,
        css_selector: str,
        timeout: int = 30
    ) -> List[WebElement]
```  

根据指定css_selector定位网页元素，返回相似元素列表。

**参数:**  
    &emsp;**css_selector[必需]**: str     
        &emsp;&emsp; CSS selector 字符串  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。   

**返回值:**  
    &emsp;[WebElement](./webelement.md)对象列表。 

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com/images")

# find elements by CSS selector
element = page.find_element_by_css_selector("#ilp_t")

# find sub elements by CSS selector
webelements = element.find_elements_by_css_selector("IMG")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```