# NotSupportedOperationError

- 扩展: [NotSupportedError](./notsupportederror.md)

**一些页面操作，页面元素不支持当前的操作**

- [NotSupportedOperationError](#notsupportedoperationerror)
    - [message](#message)
    - [stacktrace](#stacktrace)
    - [automation\_tech](#automation_tech)
    - [control\_type](#control_type)
    - [operation](#operation)


### message
- 类型: str

错误消息。


### stacktrace
- 类型: str

call stack详细信息，基于此可以定位到失败的函数位置。

### automation_tech
- 类型: str

使用的自动化技术名称,例如"UIA", "Chrome", "Edge"， 后续会添加"IE", "Firefox", "JAVA", "SAP"等。

### control_type
- 类型: str

页面元素类型， 例如: "Button", "Edit", "Document", "CheckBox", "Image", 其中"Image" 特指使用图像识别定位的元素。

### operation
- 类型: str

操作名称， 例如: "click", "check", "highlight".