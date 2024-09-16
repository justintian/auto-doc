# get_property
```python
def get_property(
        self,
        name: str,
        timeout: int = 30
    ) -> str
``` 

获取目标元素的上指定属性的值  

**参数:**   
    &emsp;**name [必需]**: str  
        &emsp;&emsp; 属性名称, 不同类型的页面元素可能支持的属性列表不同， 具体定义参见 [自动化基本概念](./../../../concepts/concepts.md).  
   &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;str

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator
    
tag = sw.find_element(locator.bing.search_sb_form_q).get_property("tag")
```