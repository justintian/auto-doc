
# BaseError

- 扩展: [Exception](https://docs.python.org/3/library/exceptions.html#Exception "Python Built-in Exception")

**All Swifthorse exceptions inherit from this class.**

### message
- 类型: str

错误消息。


### stacktrace
- 类型: str

call stack详细信息，基于此可以定位到失败的函数位置。