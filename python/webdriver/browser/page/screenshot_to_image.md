
# Page.screenshot_to_image  

```python
def screenshot_to_image(
        self,
        image_file: str,
        mode: Literal["bounds", "viewport", "full"] = ScreenShotMode.Full,
        rect: Rectangle = None,
        wait_for_page_delay: int = 0
    ) -> None
``` 


Save current browser tab's screenshot to file using CDP tech. Only support for chromium web tabs.   

**参数:**  
    &emsp;**image_file[必需]**: str   
        &emsp;&emsp; File path to save image.  
    &emsp;**mode**: Literal["bounds", "viewport", "full"] = ScreenShotMode.Full     
        &emsp;&emsp; Define the mode to capture browser tab's screenshot:  
        &emsp;&emsp;&emsp;&emsp; bounds: takes a screenshot of the specified rectangle of the page, using parameter `rect` to define the rectangle.  
        &emsp;&emsp;&emsp;&emsp; viewport: takes a screenshot of the currently visible viewport.  
        &emsp;&emsp;&emsp;&emsp; full: takes a screenshot of the full scrollable page, using parameter `wait_for_page_delay` to wait the page ready.      
    &emsp;**next_page_button_locator**: Union[_Locator, str] = None       
        &emsp;&emsp; The visit path of locator for goto next page UI element. If it's None, means just extract the current page data.      
    &emsp;**rect**: Rectangle = None  
        &emsp;&emsp; an object which specifies clipping of the resulting image.   
    &emsp;**wait_for_page_delay**: int = 0   
        &emsp;&emsp; The timout for waiting for the page ready, the unit is second.  

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw
from swifthorse.common.enums import ScreenShotMode
import os,sys


file = os.path.join(os.path.abspath(sys.path[0]), "tmp.jpg")
page = sw.chrome.open("http://swifthorse.com")
page.screenshot_to_image(file, ScreenShotMode.Viewport)

```