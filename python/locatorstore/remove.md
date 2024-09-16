---
sidebar_position: 23
sidebar_label: remove
---
# locatorstore.remove

```python
def remove(
        self,
        project_folder: str,
        locator_store: str,
        locator_id: str,
    ) -> bool
```  
在指定元素存储库中删除选择器。

**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录。
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称。
    &emsp;**locator_id[必需]**: str     
        &emsp;&emsp; 选择器唯一标识id。

**返回值:**  
    &emsp;删除成功返回True，删除失败返回False
