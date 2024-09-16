
# browser.new_page

```python
def new_page(self, url: str, wait_complete: bool = True, timeout: int = 30) -> Page
```  

打开新的浏览器页面

**参数:**  
    &emsp;**url[必需]**: str   
        &emsp;&emsp; Url 字符串，例如: <https://www.bing.com>。
    &emsp;**wait_complete**: bool  
        &emsp;&emsp; 是否等待网页加载完成，默认为True。  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;[Page](./page/page.md) 对象, 浏览器页面对象，通过该对象可以继续定位到页面里的元素。

**示例:**
***
```python
from swifthorse import swifthorse as sw

_page = sw.chrome.open("https://www.bing.com/")

# get tab's browser
_browser = _page.browser

# new tab
_browser.new_page("https://www.bing.com/")

```