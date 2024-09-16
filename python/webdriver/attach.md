
# WebDriver.attach

```python
def attach(
        self,
        locator: Union[_Locator, str],
        args: dict = {},
        maximize: bool = True,
        timeout = 30
    ) -> Page
```  

根据指定的选择器，绑定到打开的浏览器页面

**参数:**  
   &emsp;**locator[必需]**: str | _Locator   
        &emsp;&emsp; 选择器json格式的字符串, 用于定位页面元素, 例如: 'locator.bing.search_sb_form_q', 元素库是 chrome, 选择器名称是 search_sb_form_q. 关于选择器和元素库参考 [选择器](./../../../concepts/locator.md). 
    &emsp;**args[可选]**: dict  
        &emsp;&emsp; args, 数据字典，用于替换选择器中的参数, eg: `{ "title": 'rpa',  "col": 3}`.  
        &emsp;&emsp; 关于参数化的选择器参见 [参数化的选择器](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**maximize**: bool  
        &emsp;&emsp; 是否要最大化打开的窗口，默认为True。  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;[Page](./browser/page/page.md) 对象，浏览器页面对象，通过该对象可以继续定位到页面里的元素。

**示例:**
***
```python
from swifthorse import swifthorse as sw

# attach chrome browser
page = sw.chrome.attach("locator.chrome.document_newtab")
```