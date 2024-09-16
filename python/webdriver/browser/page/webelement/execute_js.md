---
sidebar_position: 10
sidebar_label: execute_js
---
# WebElement.execute_js

```python
def execute_js(
        self,
        javascript_code: str, 
        method: str = '', 
        timeout: int = 30
    ) -> str
```  

在当前网页元素上执行js。 

> **注意:**
> 在Javascript代码中, 可以使用如下方式获取当前网页元素 "_context$.currentElement."。

**参数:**  
    &emsp;**javascript_code[必需]**: str    
        &emsp;&emsp; Javascript 代码片段。
    &emsp;**method**: str    
        &emsp;&emsp; 需要执行的Javascript方法名称，也可以指定参数，例如: SetText(\"test\").  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。  

**返回值:**  
    &emsp;Str, 执行结果

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open chrome browser
page = sw.chrome.open("https://www.bing.com")

# execute js, set text for target element
webEle = page.find_element(locator.bing.search_sb_form_q)
js = "function SetText(text){_context$.currentElement.value = text; console.log(\"exit 0\"); return \"success\"}"

result = webEle.execute_js(js, "SetText(\"click\")")
```