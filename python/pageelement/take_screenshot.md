# save_to_image  
````python 
def save_to_image(
        self,
        image_file: str,
        img_width: int = 0,
        img_height: int = 0,
        xoffset: int = 0,
        yoffset: int  = 0,
        timeout: int = 30
    ) -> None
```

对目标元素进行截屏并保存成本地图像。

**参数:**   
    &emsp;**image_file[必需]**: str  
        &emsp;&emsp; 保存的图像文件路径，可以是相对路径或者绝对路径。  
    &emsp;**img_width[可选]**: int  
        &emsp;&emsp; 保存的图像宽度. 默认值为0，会自动设置为当前元素的宽度。  
    &emsp;**img_height[可选]**: int  
        &emsp;&emsp; 保存的图像高度. 默认值为0，会自动设置为当前元素的高度。  
    &emsp;**xoffset[可选]**:  int  
        &emsp;&emsp; 相对于当前元素左上角位置的横向偏移。  
    &emsp;**yoffset[可选]**: int  
        &emsp;&emsp; 相对于当前元素左上角位置的纵向偏移。 
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator
    
sw.find_element(locator.bing.search_sb_form_q).save_to_image("D:\\screenshot.png")
```