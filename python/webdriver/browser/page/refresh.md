---
sidebar_position: 21
sidebar_label: refresh
---
# Page.refresh

```python
def refresh(self) -> None
```  

刷新页面。

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.bing.com")

# refresh browser tab
page.refresh()
```