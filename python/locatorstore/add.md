
# locatorstore.add

```python
def add(
        self,
        project_folder: str,
        locator_store: str,
        locator: str,
        node: str=None 
    ) -> str
```  
返回指定元素库的元素列表信息。

**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录。
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称。
    &emsp;**locator[必需]**: str     
        &emsp;&emsp; 选择器json格式字符串。
    &emsp;**locator[可选]**: str     
        &emsp;&emsp; 元素存储库中的文件夹名称，如果不存在，就新建；默认值为None，表示选择器直接添加到元素库的根目录下。

**返回值:**  
    &emsp;选择器唯一标识符
