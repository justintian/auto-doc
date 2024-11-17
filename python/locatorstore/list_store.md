
# locatorstore.list_store

```python
def list_store(
    init_root = False
    ) -> List[ElementStore]:
```  

返回当前项目目录下的元素库列表。

**参数:**  
    &emsp;**init_root**: bool     
        &emsp;&emsp; 是否初始化元素列表信息     

**返回值:**  
    &emsp;ElementStore，针对元素的操作方法，比如列表，移除，重命名在该类中实现
