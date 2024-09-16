# select_item
```python
def select_item(
        self,
        item: str,
        timeout: int = 30
    ) -> None
```  

针对下拉框类型的元素，选择指定的选项。

**参数:**  
    &emsp;**item [必需]**: str   
        &emsp;&emsp; 下拉框的一个选项值  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。   

**返回值:**  
    &emsp;None

**示例:**
***
- 网页上选择项目 (元素类型是 select)  
![sampel1](../../../img/select-item-sample1.png)

```python
from swifthorse import swifthorse as sw, locator

page = sw.chrome.open("https://swifthorse.com")
page.find_element(locator.chrome.page.select).select_item('One')

```
-  windows应用程序上的选择项目示例 

![sample](../../../img/select_item_sample2.png)  
```python
from swifthorse import swifthorse as sw, locator

sw.find_element(locator.notepad.combobox_filetype).select_item('All Files  (*.*)')

```