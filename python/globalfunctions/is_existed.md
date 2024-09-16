
# swifthorse.is_existing
```python
 def is_existed(
        locator: Union[_Locator, str],
        args: dict = {},
        timeout: int = 30
    ) -> bool 
 ```

判断选择器对应的页面元素是否存在

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素, 例如: 'locator.bing.search_sb_form_q', 元素库是 chrome, 选择器名称是 search_sb_form_q. 关于选择器和元素库参考 [选择器](./../../../concepts/locator.md).  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;返回True如果页面元素存在；返回False如果页面元素不存在或者窗口不存在。

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

sw.is_existed(locator.bing.search_sb_form_q)

#parametric locator
args = {"title":"rpa"}args = {"title":"rpa"}
sw.is_existed(locator.bing.search_sb_form_q, args)
```