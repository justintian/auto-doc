# ExtensionOperationError

- 扩展: [BaseError](./baseerror.md)

**安装，更新或者卸载浏览器插件的时候失败**

- [ExtensionOperationError](#extensionoperationerror)
    - [message](#message)
    - [stacktrace](#stacktrace)
    - [extention\_type](#extention_type)
    - [operation](#operation)

### message
- 类型: str

错误消息。


### stacktrace
- 类型: str

call stack详细信息，基于此可以定位到失败的函数位置。


### extention_type
- 类型: str

扩展类型

### operation
- 类型: str

操作名称