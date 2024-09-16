# input_text
```python
def input_text(
        self,
        text: str,
        by: Literal["default", "set-property", "input-after-click", "input-after-focus"]= "default",
        overwrite: bool = True,
        timeout: int = 30
    ) -> None
```  

在目标元素上输入文本。 

**参数:**  
    &emsp;**text[必需]**: str  
        &emsp;&emsp; 需要输入的文本，支持输入中文. 
    &emsp;**by**: str | InputTextBy   
        &emsp;&emsp; 输入文本的方法类型  
        &emsp;&emsp; `set-property`: `set-property`: 通过设置目标元素的属性来设置文本，调用事件或者原生的命令。    
        &emsp;&emsp; `input-after-click`: 先点击目标元素，然后模拟键盘输入。 
        &emsp;&emsp; `input-after-focus`: 先聚焦目标元素，然后模拟键盘输入。  
        &emsp;&emsp; `default`: 由程序自动根据目标元素类型自动选择，例如网页元素默认用`set-property`; 桌面元素默认用 `input-after-click`。  
    &emsp;**overwrite**: bool  
        &emsp;&emsp; 是否覆盖目标元素现有的文本，默认为True， by参数为`set-property`，该参数才生效。   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

sw.find_element(locator.bing.search_sb_form_q).input_text("swifthorse", overwrite = False)
```