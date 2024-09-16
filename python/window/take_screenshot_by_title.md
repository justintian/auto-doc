# take_screenshot_by_title

```python
def take_screenshot_by_title(
        self, 
        image_file: str,
        title: str
    ) -> None
```  

根据标题定位到窗口，然后截屏该窗口。  

**参数:**  
    &emsp;**image_file[必需]**: str   
        &emsp;&emsp; 保存的图像文件路径，可以是相对路径或者绝对路径
    &emsp;**title[必需]**: str   
        &emsp;&emsp; 窗口标题，可以只包含标题的部分内容

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

#截屏窗口
sw.window.take_screenshot_by_title("C:\\快照.png","rpa")

```