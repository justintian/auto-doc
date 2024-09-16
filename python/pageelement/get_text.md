# get_text
```python
def get_text(self, timeout: int = 30) -> str
```

获取目标元素的文本内容。

**参数:**    
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;str

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator
    
text = sw.find_element(locator.bing.search_sb_form_q).get_text()
```

- windows应用上的编辑控件，返回的是value
```python
from swifthorse import swifthorse as sw, locator
    
# edit document返回的是value
text = sw.find_element(locator.notepad.document).get_text()
```

- 对于windows应用上的 button, menuitem等, 返回的是name属性值
```python
from swifthorse import swifthorse as sw, locator
    
# menuitem返回的是name属性值
text = sw.find_element(locator.notepad.menuitem_format).get_text()
# text is 'format'
```

- 网页元素返回的是innerText.
```python
from swifthorse import swifthorse as sw, locator
page = sw.chrome.open("https://swifthorse.com")
# return inner text of div
text = page.find_element(locator.form.divItem).get_text()
```