---
sidebar_position: 6
sidebar_label: find_elements_by_xpath
---
# Page.find_elements_by_xpath
```python
def find_elements_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> List[WebElement]
```  

根据指定xpath定位网页元素，返回相似元素列表。

**参数:**  
    &emsp;**xpath[必需]**: str     
        &emsp;&emsp; XPath 字符串。 
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;List of [WebElement](./webelement/webelement.md) 对象.

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com/images")

# find elements by XPath
webelements = page.find_elements_by_xpath("//*[@id=\"ilp_t\"]/div[1]/div/*")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```