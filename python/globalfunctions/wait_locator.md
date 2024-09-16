---
sidebar_position: 4
---
# swifthorse.wait_locator
```python
def wait_locator(
        locator: Union[_Locator, str],
        args: dict = {},
        wait_timeout: int = 30
    ) -> PageElement
```

在指定时间范围之内，等待元素出现

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素, 例如: 'locator.bing.search_sb_form_q', 元素库是 chrome, 选择器名称是 search_sb_form_q. 关于选择器和元素库参考 [选择器](./../../../concepts/locator.md).  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**wait_timeout[可选]**: int  
        &emsp;&emsp; 等待页面元素出现的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;如果元素出现，返回[PageElement](./../pageelement/pageelement.md) 对象；如果元素未出现，返回None。


**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

#wait element appear
sw.wait_locator(locator.bing.search_sb_form_q)

#parametric locator
args = {"title":"rpa"}
sw.wait_locator(locator.notepad.document_151, args)
```