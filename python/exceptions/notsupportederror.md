# NotSupportedError

- 扩展: [BaseError](./baseerror.md)

**不支持的操作，例如部分操作只支持在网页元素，在桌面元素上调用，就会失败**

- [NotSupportedError](#notsupportederror)
    - [message](#message)
    - [stacktrace](#stacktrace)


### message
- 类型: str

错误消息。


### stacktrace
- 类型: str

call stack详细信息，基于此可以定位到失败的函数位置。