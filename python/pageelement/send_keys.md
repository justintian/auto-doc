# send_keys
```python
def send_keys(
        self,
        hotkey: str,
        preaction: Literal["focus", "click"] = "focus",
        timeout: int = 30
    ) -> None
```  

在目标元素上发送快捷键。

**参数:**  
    &emsp;**keys[必需]**: str   
        &emsp;&emsp; 一个键或者组合键，例如"A", "AB", 关于如何发送特殊键或者功能键或者组合，参见微软官方文档[快捷键定义](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks).
    &emsp;**preaction**:   
        &emsp;&emsp; 发送快捷键之前的操作  
        &emsp;&emsp; `focus`: 默认值，先聚焦当前元素，再发送快捷键。  
        &emsp;&emsp; `click`: 先点击当前元素，再发送快捷键。  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

#发送 Ctrl+a  全选
sw.find_element(locator.bing.search_sb_form_q).send_keys('^a')

#发送 Shift+End
sw.find_element(locator.bing.search_sb_form_q).send_keys('+{END}')

#发送 Win+e, 实际是先按下 'Win', 再按下 'E' 然后释放, 最后释放 'Win'
sw.find_element(locator.bing.search_sb_form_q).send_keys('{WIN DOWN}e{WIN UP}')
```