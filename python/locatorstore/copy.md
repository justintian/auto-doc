
# locatorstore.copy

```python
def copy(
        self,
        project_folder: str,
        locator_store: str,
        locator_id: str,
        new_locator_store: str,
        new_node: str=None,
        new_locator_name: str = None,
    ) -> str
```  
重命名指定的元素。

**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录。
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称。
    &emsp;**locator_id[必需]**: str     
        &emsp;&emsp; 选择器唯一标识id。
    &emsp;**new_locator_store[必需]**: str     
        &emsp;&emsp; 复制的元素到的元素库名称。
    &emsp;**new_node[可选]**: str     
        &emsp;&emsp; 元素存储库中的文件夹名称，如果不存在，就新建；默认值为None，表示选择器直接添加到元素库的根目录下。
    &emsp;**new_locator_name[可选]**: str     
        &emsp;&emsp; 复制的选择器名称，默认自动分配名称。

**返回值:**  
    &emsp;返回新复制的选择器唯一标识符
