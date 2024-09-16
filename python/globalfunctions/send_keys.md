---
sidebar_position: 6
---
# swifthorse.send_keys
```python
def send_keys(keys: str) -> None
```

在当前鼠标光标处，发送快捷键。

>**注意:**  
系统方法，在当前鼠标光标处，发送快捷键。如果需要先聚焦某个页面元素再发送快捷键，方式一先点击或者聚焦元素，然后使用该方法发送快捷键；方式二，使用元素对象上的方法 [send_keys](./send_keys.md)。

**参数:**  
    &emsp;**keys[必需]**: str   
        &emsp;&emsp; 一个键或者组合键，例如"A", "AB", 关于如何发送特殊键或者功能键或者组合，参见微软官方文档[快捷键定义](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks).

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

#send Ctrl+a
sw.send_keys('^a')

#send Shift+End
sw.send_keys('+{END}')

#send Win+e, first press 'Win', then press 'E' and release, and finally release 'Win'
sw.send_keys('{WIN DOWN}e{WIN UP}')
```