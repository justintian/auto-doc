
# WebElement.set property

```python
def set_property(
        self,
        name: str,
        value: str,
        timeout: int = 30
    ) -> None
```  

设置属性值。  

**参数:**  
    &emsp;**name[必需]**: str  
        &emsp;&emsp; 属性名称， 网页元素支持的属性列表参见 [Automation Concepts](./../../../../../../concepts/concepts.md) 。
    &emsp;**value[必需]**: str  
        &emsp;&emsp; 属性值。    
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

page = sw.chrome.open("https://bing.com")

# set the web propery with specified value
page.find_element(locator.bing.search_sb_form_q).set_property("tag", "search_tag")
```