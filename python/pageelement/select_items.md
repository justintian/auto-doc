# select_items
```python
def select_items(
        self,
        items: list,
        clear_selected: bool = True,
        timeout: int = 30
    ) -> None
```  

针对支持多选的下拉框类型的元素，选择多个选项。

**参数:**  
    &emsp;**items [必需]**: list  
        &emsp;&emsp; 下拉框选项列表
    &emsp;**clear_selected**: bool  
        &emsp;&emsp; 是否清除当前选中的状态，默认为是
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。   

**返回值:**  
    &emsp;None

**示例:**
***
- 网页上选择多个选项的操作示例
  
```python
from swifthorse import swifthorse as sw, locator
page = sw.chrome.open("https://swifthorse.com")  
page.find_element(locator.chrome.page.multiselect).select_item({'One', 'Three'})  
# as showing below, 'One' and 'Three' are selected.
```

![sample](../../../img/select_items_sample2.png)  