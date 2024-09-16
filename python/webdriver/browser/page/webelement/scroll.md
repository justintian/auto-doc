
# WebElement.scroll

```python
def scroll(
        self,
        delta_x: int = 0,
        delta_y: int = 0,
        timeout: int = 30
    ) -> None
```   

滚动网页元素的滚动条。

**参数:**  
    &emsp;**delta_x**: int   
        &emsp;&emsp; 横向滚动的像素数。  
    &emsp;**delta_y**: int   
        &emsp;&emsp; 纵向滚动的像素数。 
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。   

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.swifthorse.com")

# scroll the element
web_element = page.find_element(locator.chrome.swifthorse.products_panel)
web_element.scroll(0, 500)
```