# clean_text
```python
def clean_text(
        self,
        by: Literal["set-property", "send-keys"],
        clear_keys: Literal["CA_D", "E_SH_D", "H_SE_D"] = "CA_D",
        preaction: Literal["focus", "click"] = "focus",
        timeout: int = 30
    ) -> None
```  

清除目标元素的文本内容

**参数:**  
     &emsp;**by[必需]**: ClearTextBy  
        &emsp;&emsp; 清除文本的方法类型  
        &emsp;&emsp; `set-property`: 通过设置目标元素的属性来清除文本，调用事件或者原生的命令。  
        &emsp;&emsp; `send-keys`: 通过发送快捷键的方式 "clear_keys" 和 "preaction" 参数都需要做相应的设置.   
    &emsp;**clear_hotkey**: ClearKeys  
        &emsp;&emsp; 如果参数 by 设置为 "send-keys", 那么必须指定快捷键组合, default is `CA_D`.  
        &emsp;&emsp; `CA_D` 代表`{CTRL}{A}-{DELETE}`: 先发送 "{CTRL}{A}" 全选文本, 然后发送 "{DELETE}".  
        &emsp;&emsp; `E_SH_D` 代表 `{END}-{SHIFT}{HOME}-{DELETE}`: 首先发送 "{END}" 然后发送组合键 "{SHIFT}{HOME}"全选文本, 然后发送 "{DELETE}".  
        &emsp;&emsp; `H_SE_D` 代表 `{HOME}-{SHIFT}{END}-{DELETE}`: 首先发送 "{HOME}", 然后发送组合键  "{SHIFT}{END}"全选文本, 然后发送  "{DELETE}".  
    &emsp;**preaction**: PreAction  
        &emsp;&emsp; 如果参数 by 设置为 "send-keys",那么需要指定在发送快捷键之前先对目标元素做的操作，是聚焦还是点击   
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;None


**异常:**  
    &emsp;参见[异常定义](../exceptions/exceptions.md)

**示例:**
***
- windows另存为对话框
```python
from swifthorse import swifthorse as sw, locator 

sw.find_element(locator.chrome.edit_1001).clean_text(by="set-property")
```

- 微信输入框 
```python
from swifthorse import swifthorse as sw, locator  

sw.find_element(locator.wechat.edit1).clean_text(by="send-keys", clear_hotkey="CA_D", preaction="click")

```

- 网页输入元素

```python
page = sw.chrome.open("https://swifthorse.com/")
page.find_element(locator.swifthorse.text).input_text("rpa")
page.find_element(locator.swifthorse.text).clean_text(by="set-property")
```