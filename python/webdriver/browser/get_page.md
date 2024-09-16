
# browser.get_page

```python
def get_page(self, title: str = '', url: str = '') -> Page
```  

根据标题或者url获取相应的浏览器页面对象

**参数:**  
    &emsp;**title**: str   
        &emsp;&emsp; 标题字符串，支持通配符。  
    &emsp;**url**: str  
        &emsp;&emsp; url 字符串，支持通配符。

**返回值:**  
    &emsp;[Page](./page/page.md) 对象, 浏览器页面对象，通过该对象可以继续定位到页面里的元素。

**示例:**
***
```python
from swifthorse import swifthorse as sw

browser = sw.chrome.browsers[0]
# by tile and url
browser.get_page("bing", "https://cn.bing.com/")

# by title only
browser.get_page("bing")

# by url only
browser.get_page(url = "https://cn.bing.com/")

# by title with wildcard
browser.get_page("bi*", "https://cn.bing.com/")
```