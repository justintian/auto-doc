---
sidebar_position: 5
sidebar_label: close
---
# browser.close

```python
def close(self, force: bool = False) -> None
```  

关闭浏览器对象，会关闭该窗口的所有的浏览器页面。

**参数:**  
    &emsp;**force**: bool, 强制关闭。    

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.bing.com")

# close the browser
page.browser.close()

```