
# Page.goto

```python
def goto(
        self,
        url: str,
        wait_complete: bool = True,
        timeout: int = 30
    ) -> None
```  

访问指定的网址。

**参数:**  
    &emsp;**url[必需]**: str   
        &emsp;&emsp; 网页地址，例如: <https://www.bing.com>.  
    &emsp;**wait_complete**: bool = True  
        &emsp;&emsp; 是否等待页面加载完成，默认为True。
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.bing.com")

# naviage to another website
page.goto("https://google.com")
```