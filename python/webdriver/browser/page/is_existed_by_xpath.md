
# Page.is_existed_by_xpath
```python
def is_existed_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> bool
```  

根据指定的xpath字符串，判断网页元素是否存在。

**参数:**  
    &emsp;**xpath[必需]**: str     
        &emsp;&emsp; XPath 字符串。 
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;返回True如果元素是存在的，否则返回False

**示例:**
***
```python
from swifthorse import swifthorse as sw

page = sw.chrome.open("https://bing.com/images")

# check element if exist by XPath
result = page.is_existed_by_xpath("//*[@id=\"sb_form_q\"]")
print(result)

```