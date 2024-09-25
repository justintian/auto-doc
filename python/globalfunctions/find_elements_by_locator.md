
# swifthorse.find_elements
```python 
def find_elements(
        locator: str,
        args: dict = {},
        timeout: int = 30
    ) -> List[PageElement]
```

返回相似元素列表

**参数:**  
    &emsp;**locator[必需]**: str
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素,关于选择器 [选择器](./../../../concepts/locator.md). 
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回:**  
    &emsp;相似元素列表，类型为 List([PageElement])(./../../python/pageelement/pageelement.md).

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

sw.chrome.open("https://www.bing.com/")
sw.find_element(locator.store.bing.search_sb_form_q).input_text('swifthorse')
sw.find_element(locator.store.bing.svg).click()

result_elements = sw.find_elements(locator.store.bing.a_search_result)
for elem in result_elements:
    elem.highlight(duration=1)
```