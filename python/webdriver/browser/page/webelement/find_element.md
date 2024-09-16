---
sidebar_position: 3
sidebar_label: find_element
---
# WebElement.find_element
```python
def find_element(
        self,
        locator: Union[_Locator, str],
        args: dict = {},
        timeout: int = 30
    ) -> WebElement
```  

返回指定选择器对应的网页元素，如果匹配多个，默认返回第一个。 

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器字符串，json格式, 例如: 'locator.bing.search_sb_form_q', 选择器库为bing, 选择器名称为search_sb_form_q. 更多细节参见[Locator](./../../../../../concepts/locator.md)。  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`。  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator)。 
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;[WebElement](./webelement.md)对象。

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

page = sw.chrome.open("https://bing.com")

# find element
webelement = page.find_element(locator.bing.search_sb_form_q)

# find sub element   
subelement = webelement.find_element(locator.bing.search_icon)

```