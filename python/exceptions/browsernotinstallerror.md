# BrowserNotInstallError

- 扩展: [WebError](./weberror.md)

**当前操作系统环境下，未检测到指定的浏览器**

- [BrowserNotInstallError](#browsernotinstallerror)
    - [message](#message)
    - [stacktrace](#stacktrace)
    - [browser\_type](#browser_type)


### message
- 类型: str

错误消息。


### stacktrace
- 类型: str

call stack详细信息，基于此可以定位到失败的函数位置。

### browser_type
- 类型: str

浏览器类型，支持的类型有"Chrome" 和 "Edge", 即将支持 "IE", "Firefox"。