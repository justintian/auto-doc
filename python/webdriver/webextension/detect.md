
# WebDriver.extension.detect

```python
def detect(self) -> ExtensionStatus
``` 

检测和返回当前浏览器扩展的状态。

.

**返回值:**  
    &emsp;ExtensionStatus, 通过如下命令导入模块 `from swifthorse.common.enums import ExtensionStatus`, 定义如下: 
```python
class ExtensionStatus:
    NotInstalled = "NotInstalled"
    NeedUpdate = "NeedUpdate"
    Installed = "Installed" 
```

**示例:**
***
```python
from swifthorse import swifthorse as sw
from swifthorse.common.enums import ExtensionStatus

# detect chrome extension
chrome_status = sw.chrome.extension.detect()
if chrome_status == ExtensionStatus.NeedUpdate:
    sw.chrome.extension.update()
```