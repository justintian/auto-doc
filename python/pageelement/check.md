# check
```python
def check(
        self,
        check_type: Literal["check", "uncheck", "toggle"] = CheckType.Check,
        timeout: int = 30
    ) -> None
```  

设置勾选类型的页面元素的勾选状态

**参数:**  
    &emsp;**check_type**: str | CheckType   
        &emsp;&emsp; 设置的勾选状态: "check", "uncheck" 或者 "toggle"。
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。

**返回值:**  
    &emsp;None

**异常:**  
    &emsp;参见[异常定义](../exceptions/exceptions.md)