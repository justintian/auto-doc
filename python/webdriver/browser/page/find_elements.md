---
sidebar_position: 5
sidebar_label: find_elements
---
# Page.find_elements
```python
def find_elements(
        self,
        locator: Union[_Locator, str],
        args: dict = {},
        timeout: int = 30
    ) -> List[WebElement]
```  

返回指定选择器的相似网页元素列表。
 

**参数:**  
    &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器字符串，json格式, 例如: 'locator.bing.search_sb_form_q', 选择器库为bing, 选择器名称为search_sb_form_q. 更多细节参见[Locator](./../../../../../concepts/locator.md)。  
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`。  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator)。
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;List of [WebElement](./webelement/webelement.md) 对象。

**示例:**
***
```python
from swifthorse import swifthorse as sw, locator

page = sw.edge.open("https://www.bing.com/")
page.find_element(locator.new_store.sample.bing.search_sb_form_q).input_text('swifthorse')
page.find_element(locator.new_store.sample.bing.svg).click()
result_elements = page.find_elements(locator.new_store.sample.bing.a_search_result)
for elem in result_elements:
    elem.highlight(duration=1)
page.close()
```