# maximize

```python
def maximize(
        self, 
        locator: Union[_Locator, str],
        args: dict = {}, 
        timeout: int = 30
    ) -> None
```  

根据选择器定位到窗口，然后最大化该窗口。  
***注意***: 选择器仅支持桌面端的应用，[UIA](../../../concepts/uia.md) 技术, 类型为 window, 例如e:  
        ![桌面应用选择器](../../../img/window_locator.png)

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素, 例如: 'locator.bing.search_sb_form_q', 元素库是 chrome, 选择器名称是 search_sb_form_q. 关于选择器和元素库参考 [选择器](./../../../concepts/locator.md). 
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# 获取窗口驱动对象
win_instance = sw.window

#最大化窗口
win_instance.maximize("locator.notepad.window_notitle_notepad")

# 带参数的选择器
args = {"title":"rpa"}
win_instance.maximize("locator.notepad.window_notitle_notepad", args)
```