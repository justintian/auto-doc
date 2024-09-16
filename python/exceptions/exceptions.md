# Exceptions

当一个操作异常结束时，会抛出异常，除了可能抛出 python [内置的异常类型](https://docs.python.org/3/library/exceptions.html#built-in-exceptions)之外, 我们定义了特定的异常类型，都继承于 [BaseError](./baseerror.md).


## Swifthorse 异常类型 

| Exception      | Description |
| -----------| ----------- |
| [BaseError](./baseerror.md) |异常的基类|
| [ArgumentError](./argumenterror.md) | 参数无效|
| [ArgumentNullError](./argumentnullerror.md) | 必选参数为空时|
| [ArgumentOutOfRangeError](./argumentoutofrangeerror.md) | 参数值不正确，不在有效范围内|
| [BrowserNotInstallError](./browsernotinstallerror.md) | 当前操作系统环境下，未检测到指定的浏览器|
| [BrowserNotRunError](./browsernotrunerror.md) | 指定的浏览器未安装|
| [ElementNotFoundError](./elementcannotfounderror.md) | 目标页面元素在指定超时时间范围内为被定位到|
| [ExtensionOperationError](./extensionoperationerror.md) | 安装，更新或者卸载浏览器插件的时候失败|
| [InvalidOperationError](./invalidoperationerror.md)   | 无效的操作|
| [InvalidSelectedItemError](./invalidselecteditemerror.md)   | select-item的选项无效，无法选择|
| [LocatorUndefinedError](./locatorundefinederror.md) | 指定的选择器在选择器库中未找到|
| [NotSupportedError](./notsupportederror.md) | 不支持的操作，例如部分操作只支持在网页元素，在桌面元素上调用，就会失败|
| [NotSupportedOperationError](./notsupportedoperationerror.md) | 一些页面操作，页面元素不支持当前的操作|
| [NotSupportedOperationOptionError](./notsupportedoperationoptionerror.md)   | 部分操作选项在目标元素上不支持。|
| [OperationTimeoutError](./timeoutoperationerror.md) | 操作超时|
| [ScreenOperationError](./screenoperationerror.md)   | windows桌面上涉及屏幕操作失败|
| [UnAuthorizedError](./unauthoriederror.md) | 无权操作|
| [UnreachableBrowserExtensionError](./unreachablebrowserextensionerror.md) | 浏览器扩展没通信失败|
| [WebElementNotRespondingError](./webelementnotrespondingerror.md) | 网页操作无响应|
| [WebError](./weberror.md) | 网页操作异常的基类|
| [WindowError](./windowerror.md)   | 窗口类的操作失败|
| [WindowsNativeError](./windowsnativeerror.md)   | windows底层API报错|
| [WindowsPatternNotFoundError](./windowspatternnotfounderror.md)   | 桌面元素不支持的底层操作|


