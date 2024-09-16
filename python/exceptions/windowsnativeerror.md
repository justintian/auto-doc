# WindowsNativeError

- 扩展: [WindowError](./windowerror.md)

**windows底层API报错**

- [WindowsNativeError](#windowsnativeerror)
    - [message](#message)
    - [stacktrace](#stacktrace)
    - [name](#name)
    - [native\_errorcode](#native_errorcode)

### message
- 类型: str
错误消息。


### stacktrace
- 类型: str

call stack详细信息，基于此可以定位到失败的函数位置。

### name
- 类型: str

Win32接口名称


### native_errorcode
- 类型: str

Win32错误码