
# Page.activate

```python
def activate(
        self,
        topmost: bool = True
    ) -> None
```  

前置当前的网页页面。 

**参数:**  
    &emsp;**topmost**: bool    
        &emsp;&emsp; 是否同时前置浏览器窗口，默认为True。

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.bing.com")

# activate the tab
page.activate()
```