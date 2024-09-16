---
sidebar_position: 22
sidebar_label: scroll
---
# Page.scroll

```python
def scroll(
        self,
        delta_x: int = 0,
        delta_y: int = 0
    ) -> None
```  

滚动浏览器页面的滚动条。

**参数:**  
    &emsp;**delta_x**: int   
        &emsp;&emsp; 横向滚动的像素数。  
    &emsp;**delta_y**: int   
        &emsp;&emsp; 纵向滚动的像素数。 

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.swifthorse.com")

# scroll tab
page.scroll(0, 500)
```