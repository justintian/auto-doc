
# swifthorse.find_element
```python
def find_element(
        locator: str,
        args: dict = {},
        top_most: : Literal["true", "auto", "false"] = "auto"
    ) -> PageElement
```
返回指定选择器对应的页面元素，如果匹配到多个，默认返回第一个。


**参数:**  
    &emsp;**locator[必需]**: str, json格式字符串
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素。关于选择器 [选择器](./../../../concepts/locator.md).   
    &emsp;**args**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**top_most**: 选择器对应的窗口的前置处理方式  
        &emsp;&emsp; 定义是否要对选择器元素所在的窗口做前置动作处理。
        &emsp;&emsp;`true`: 在做具体的操作（例如点击）之前，先  尝试将窗口前置。
        &emsp;&emsp;`auto`: 自动化决定是否将窗口前置，如果前置动作已经将窗口前置，下一个动作就不需要做前置操作；如果前一个动作是操作不同的应用，下一个动作就会先尝试将窗口前置。
        &emsp;&emsp;`false`: 不做窗口前置操作。 

**返回:**  
    &emsp;返回指定选择器对应的页面元素，如果匹配到多个，默认返回第一个。返回对象类型为 [PageElement](./../../python/pageelement/pageelement.md).

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

searchBox = sw.find_element(locator.bing.search_sb_form_q)

#如果选择器是带参数的
args = {"title":"rpa"}
searchBox = sw.find_element(locator.bing.search_sb_form_q, args)
```