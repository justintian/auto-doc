---
sidebar_position: 23
sidebar_label: list_elements
---
# locatorstore.list_elements

```python
def list_elements(
        self,
        project_folder: str,
        locator_store: str
    ) -> str
```  
返回指定元素库的元素列表信息。

**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录。
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称。

**返回值:**  
    &emsp;元素库文本信息，json格式字符串
