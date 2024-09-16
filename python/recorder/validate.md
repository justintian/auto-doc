
# recorder.validate
```python
def validate(
        self,
        project_folder: str,
        locator_store: str,
        locator_id: str,
        duration: int = 3
    ) -> bool
```  

验证选择器。
**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录。
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称。
    &emsp;**locator_id[必需]**: str     
        &emsp;&emsp; 选择器唯一标识id。
    &emsp;**duration[可选]**: int     
        &emsp;&emsp; 定位成功之后元素高亮的时长，默认值为3秒。

**返回值:**  
    定位成功，返回True，否则返回False
