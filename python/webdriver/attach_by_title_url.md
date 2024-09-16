---
sidebar_position: 3
sidebar_label: attach_by_title_url
---
# WebDriver.attach_by_title_url

```python
def attach_by_title_url(
        self,
        title: str = '',
        url: str = '',
        maximize: bool = True,
        timeout = 30
    ) -> Page
```  

根据标题或者url，绑定到打开的浏览器页面。

**参数:**  
    &emsp;**title**: str   
        &emsp;&emsp; 标题，支持通配符 
    &emsp;**url**: str  
        &emsp;&emsp; 网址，支持通配符  
    &emsp;**maximize**: bool  
        &emsp;&emsp;是否要最大化打开的窗口，默认为True。   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;[Page](./browser/page/page.md) 对象，浏览器页面对象，通过该对象可以继续定位到页面里的元素。

**示例:**
***
```python
from swifthorse import swifthorse as sw

# attach chrome browser, by title only
page = sw.chrome.attach_by_title_url("bing")
```