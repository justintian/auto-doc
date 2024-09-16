# restore

```python
def restore(
        self, 
        locator: Union[_Locator, str],
        args: dict = {}, 
        timeout: int = 30
    ) -> None
```  

Restore the window specified by locator.    
***注意***: The locator should be recorded using [UIA](../../../concepts/uia.md) technology, role is window, for example:  
        ![window locator](../../../img/window_locator.png) 

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; Locator string, the visit path of locator for target window element, eg: 'locator.explorer.window_downloads', locator store is explorer, and locator name is window_downloads. For more details, please refer to [Locator](./../../../concepts/locator.md).   
    &emsp;**args**: dict  
        &emsp;&emsp; Locator args, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about args, please refer to [Parametric Locator](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

# get window driver
window_driver = sw.window

# restore window
window_driver.restore("locator.notepad.window_notitle_notepad")

# parametric locator
args = {"title":"rpa"}
window_driver.restore("locator.notepad.window_notitle_notepad", args)
```