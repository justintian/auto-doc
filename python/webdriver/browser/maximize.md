---
sidebar_position: 4
sidebar_label: maximize
---
# browser.maximize

```python
def maximize(self) -> None
```  

最大化浏览器窗口

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# get browser with type chrome
browser = sw.chrome.browsers[0]

# maximize the browser window
browser.maximize()
```