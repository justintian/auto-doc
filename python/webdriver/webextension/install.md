---
sidebar_position: 1
sidebar_label: install
---
# WebDriver.extension.install

```python
def install(self) -> None
```

安装浏览器扩展

>**注意:**  
>- 安装之前，先关闭该类型的所有浏览器窗口。 
>- 完成成功之后，需要手动启用新安装的浏览器扩展， 浏览器出于安全因素考虑，只支持手动启用扩展。


**示例:**
***
```python
from swifthorse import swifthorse as sw

# install chrome extension
sw.chrome.extension.install()
```