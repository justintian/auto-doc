
# Page.wait_disappear_by_xpath
```python
def wait_disappear_by_xpath(
        self,
        xpath: str,
        wait_timeout: int = 30
    ) -> bool
```  

在指定的时间内，等待指定选择器的网页元素消失。

**参数:**  
    &emsp;**xpath[必需]**: str     
        &emsp;&emsp; XPath 字符串。 
    &emsp;**wait_timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒  

**返回值:**  
    &emsp;如果网页元素消失，返回True， 否则返回False。  

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com")

# wait element disappear by XPath
result = page.wait_disappear_by_xpath("//*[@id=\"sb_form_q\"]", wait_timeout=5)
print(result)

```