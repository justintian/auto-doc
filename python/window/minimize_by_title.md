# minimize_by_title

```python
def minimize_by_title(
        self, 
        title: str
    ) -> None
```  

根据标题定位到窗口，然后最小化该窗口。  

**参数:**  
    &emsp;**title[必需]**: str   
        &emsp;&emsp; 窗口标题，可以只包含标题的部分内容

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse as sw

#最小化窗口
sw.window.minimize_by_title("rpa")

```