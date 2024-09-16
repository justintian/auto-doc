---
sidebar_position: 4
sidebar_label: install_or_update
---
# WebDriver.extension.install_or_update

```python
def install_or_update(self) -> bool
``` 

安装或者更新浏览器扩展

**返回值:** bool  
    &emsp;返回True表示新扩展已经安装或者升级成功；返回False表示最新的浏览器扩展已经安装，无需再安装。

**示例:**
***
```python
from swifthorse import swifthorse as sw

# install or update chrome extension
sw.chrome.extension.install_or_update()

```