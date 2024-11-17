
# recorder.record
```python

def record(mode : CaptureMode | str = 'multiple'):
    pass

class CaptureMode(Enum):
    Once = 'once'
    Multiple = 'multiple'
```  

录制元素，会打开录制器，支持一次录制多个元素，保存到元素库中。在录制器中支持命名新录制的元素。

**参数:**  
    &emsp;**mode**: str     
        &emsp;&emsp; 录制模式，默认为`'multiple'`

**说明：**
>  once 模式看不到元素库的Tree节点，multiple 可以看到当前项目下的元素库列表及其对应的元素列表

**返回值:**  
    None 
