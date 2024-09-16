# NotSupportedOperationOptionError

- 扩展: [NotSupportedOperationError](./notsupportedoperationerror.md)

**部分操作选项在目标元素上不支持**

## Constructor
- [NotSupportedOperationOptionError](#notsupportedoperationoptionerror)
  - [Constructor](#constructor)
    - [message](#message)
    - [stacktrace](#stacktrace)
    - [automation\_tech](#automation_tech)
    - [control\_type](#control_type)
    - [operation](#operation)
    - [option](#option)


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

### option
- 类型: str

选项值