---
sidebar_position: 11
sidebar_label: execute_js_file
---
# WebElement.execute_js_file

```python
def execute_js_file(
        self,
        javascript_file: str, 
        method: str = '', 
        timeout: int = 30
    ) -> str
```  

在当前网页元素上执行js文件。

> **注意:**
> 在Javascript代码中, 可以使用如下方式获取当前网页元素 "_context$.currentElement."。

**参数:**  
    &emsp;**javascript_file[必需]**: str    
        &emsp;&emsp; Javascript文件名称包括路径， 例如: "c:\\test.js".  
    &emsp;**method**: str    
        &emsp;&emsp; 需要执行的Javascript方法名称，也可以指定参数，例如: SetText(\"test\").  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;Str, 执行结果。

**示例:**
***
```python
from swifthorse import swifthorse as sw

# open Chrome browser
page = sw.chrome.open("https://www.bing.com")

# execute js, set text for target element

# test.js content can be:  
#  function SetText(st){  
#     _context$.currentElement.value = st;
#     console.log("execute js");
#     return "success"
#  }

result = page.find_element(locator.bing.search_sb_form_q).execute_js_file("C:\\test.js", "SetText(\"click\")")
```