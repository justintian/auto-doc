---
sidebar_position: 14
sidebar_label: wait_locator_disappear
---
# Page.wait_locator_disappear
```python
def wait_locator_disappear(
        self,
        locator: Union[_Locator, str],
        args: dict = {},
        wait_timeout: int = 30
    ) -> bool
```  

在指定的时间内，等待指定选择器的网页元素消失。


**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器字符串，json格式, 例如: 'locator.bing.search_sb_form_q', 选择器库为bing, 选择器名称为search_sb_form_q. 更多细节参见[Locator](./../../../../../concepts/locator.md)。  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`。  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator)。
    &emsp;**wait_timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;如果网页元素消失，返回True， 否则返回False。 

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

page = sw.chrome.open("https://bing.com")

# wait element disappear
page.wait_locator_disappear(locator.bing.search_sb_form_q)

# parametric locator
args = {"title":"rpa"}
page.wait_locator_disappear(locator.bing.search_sb_form_v, args)

```