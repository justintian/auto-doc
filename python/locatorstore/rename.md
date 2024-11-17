
# locatorstore.rename

```python
def rename_node(self, 
                name: str, node: NodeTreeItem
                ) -> bool:
```  
重命名指定的文件夹节点。

**参数:**  
    &emsp;**name[必需]**: str     
        &emsp;&emsp; 新的文件夹名称
    &emsp;**node[必需]**: NodeTreeItem     
        &emsp;&emsp; 当前的文件夹对象

**返回值:**  
    &emsp;重命名成功返回True，重命名失败返回False


```python
def rename_locator(self, name: str, node: EleTreeItem
                ) -> bool:
```  
重命名指定的选择器节点。

**参数:**  
    &emsp;**name[必需]**: str     
        &emsp;&emsp; 新的选择器名称
    &emsp;**node[必需]**: EleTreeItem     
        &emsp;&emsp; 当前的选择器节点对象

**返回值:**  
    &emsp;重命名成功返回True，重命名失败返回False
