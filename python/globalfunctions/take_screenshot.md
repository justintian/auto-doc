---
sidebar_position: 8
---
# swifthorse.take_screenshot
```python
def take_screenshot(image_file: str) -> None
```

截取当天屏幕截图，保存为图像文件，支持png，jpg等格式。

**参数:**  
    &emsp;**image_file[必需]**: str   
        &emsp;&emsp; 保存的图像文件路径，可以是相对路径或者绝对路径

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

sw.take_screenshot("C:\\快照.png")

```