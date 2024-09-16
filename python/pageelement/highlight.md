# highlight
```python
def highlight(
        self,
        color: Union[str, Color] = Color.Red,
        duration: int = 2,        
        timeout: int = 30
    ) -> None
```  

高亮目标元素。

**参数:**  
    &emsp;**color[可选]**: str | Color  
        &emsp;&emsp; 高亮框的颜色，默认是Red，红色.  
    &emsp;**duration[可选]**: int  
        &emsp;&emsp; 高亮持续的时间，默认是2秒  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;None

**示例:**
***
- 高亮网页元素  
```python
from swifthorse import swifthorse as sw, locator
    
sw.find_element(locator.bing.search_sb_form_q).highlight(color=Color.Yellow)
```

如图所示:  
![highlight](../../../img/highlight.png)