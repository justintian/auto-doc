---
sidebar_position: 23
sidebar_label: rename
---
# locatorstore.rename

```python
def rename(
        self,
        project_folder: str,
        locator_store: str,
        locator_id: str,
        new_name: str
    ) -> bool
```  
重命名指定的元素。

**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录。
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称。
    &emsp;**locator_id[必需]**: str     
        &emsp;&emsp; 选择器唯一标识id。
    &emsp;**new_name[必需]**: str     
        &emsp;&emsp; 选择器新的名称。

**返回值:**  
    &emsp;重命名成功返回True，重命名失败返回False
