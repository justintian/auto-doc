
# Page.close

```python
def close(self) -> None
```  

关闭当前页面，如果所在的浏览器窗口没有其他页面，那么浏览器窗口也会被关闭。

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.bing.com")

# close the tab
page.close()
```