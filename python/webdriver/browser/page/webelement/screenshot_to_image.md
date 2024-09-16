---
sidebar_position: 12
sidebar_label: screenshot_to_image
---
# WebElement.screenshot_to_image  

```python 
def screenshot_to_image(
        self,
        image_file: str,
        timeout: int = 30
    ) -> None
```  


Save target element's screenshot to file using cdp tech. Only support for chromium webelements.  

**参数:**  
    &emsp;**image_file[必需]**: str   
        &emsp;&emsp; File path to save image.    
    &emsp;**timeout**: int = 30   
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds  

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw
import os,sys

file = os.path.join(os.path.abspath(sys.path[0]), "tmp.jpg")
page = sw.chrome.open("http://swifthorse.com")
web_element = page.find_element(locator.chrome.sample)
web_element.screenshot_to_image(file, 1)
```