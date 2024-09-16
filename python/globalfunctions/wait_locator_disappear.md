
# swifthorse.wait_locator_disappear
```python 
def wait_locator_disappear(
        locator: Union[_Locator, str],
        args: dict = {},
        wait_timeout: int = 30
    ) -> bool
```

在指定时间范围之内，等待指定的元素消失。

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素, 例如: 'locator.bing.search_sb_form_q', 元素库是 chrome, 选择器名称是 search_sb_form_q. 关于选择器和元素库参考 [选择器](./../../../concepts/locator.md).  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**wait_timeout[可选]**: int  
        &emsp;&emsp; 等待页面元素消失的超时时间，默认是30秒，单位是秒。 

**返回值:** bool  
    &emsp;如果元素消失，返回True；如果元素未消失，返回False。


**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

#wait element disappear
sw.wait_locator_disappear(locator.bing.search_sb_form_q)

#parametric locator
args = {"title":"rpa"}
sw.wait_locator_disappear(locator.notepad.document_151, args)
```