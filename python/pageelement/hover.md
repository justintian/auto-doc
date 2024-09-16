# hover
```python
def hover(self, timeout: int = 30) -> None
```  

鼠标悬停在目标元素上。

**参数:**    
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;None

**示例:**
***
- 悬停在web页面元素上 
  
![sample](../../../img/hover_sample1.png)  

```python
from swifthorse import swifthorse as sw, locator
    
sw.find_element(locator.bing.li_dots_overflow).hover()
# 下拉菜单会显示出来
```
  
![sample](../../../img/hover_sample2.png) 