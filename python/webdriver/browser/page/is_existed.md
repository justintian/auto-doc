
# Page.is_existed
```python
def is_existed(
        self,
        locator: Union[_Locator, str],
        args: dict = {},
        timeout: int = 30
    ) -> bool
```  

根据指定的选择器，判断网页元素是否存在。

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器字符串，json格式, 例如: 'locator.bing.search_sb_form_q', 选择器库为bing, 选择器名称为search_sb_form_q. 更多细节参见[Locator](./../../../../../concepts/locator.md)。  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`。  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator)。
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;返回True如果元素是存在的，否则返回False

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

page = sw.chrome.open("https://bing.com")

# check element if exist
page.is_existed(locator.bing.search_sb_form_q)

# parametric locator
args = {"title":"rpa"}
page.is_existed(locator.bing.search_sb_form_q, args)
```