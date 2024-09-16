
# swifthorse.input_text
```python
def input_text(
        self,
        text: str
    ) -> None
```

在当前鼠标光标处，发送文本。

>**注意:**  
系统方法，在当前鼠标光标处，发送指定文本。如果需要先聚焦某个页面元素再输入文本，方式一先点击或者聚焦元素，然后使用该方法输入文本；方式二，使用元素对象上的方法 [input_text](./input_text.md)。


**参数:**  
    &emsp;**text[必需]**: str  
        &emsp;&emsp; 需要输入的文本  

**返回值:**  
    &emsp;None

**示例:**
***
```python
from swifthorse import swifthorse

swifthorse.find_element(locator.bing.search_sb_form_q).focus()

swifthorse.input_text("swifthorse")
```