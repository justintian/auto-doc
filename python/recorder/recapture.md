
# recorder.recapture
```python
def recapture(
        self,
        project_folder: str,
        locator_store: str,
        locator_id: str
    ) -> str
```  

重新录制已经存在的选择器，新录制的选择器会覆盖原有的选择器。验证选择器。
**参数:**  
    &emsp;**project_folder[必需]**: str     
        &emsp;&emsp; 项目目录
    &emsp;**locator_store[必需]**: str     
        &emsp;&emsp; 元素存储库名称
    &emsp;**locator_id[必需]**: str     
        &emsp;&emsp; 选择器唯一标识id

**返回值:**  
    RecordInfo，新录制的选择器json字符串
