# WebDriver 

**WebDriver 类提供浏览器页面上的操作方法。**  

- `swifthorse.chrome`: Chrome 浏览器驱动 
- `swifthorse.edge`: Edge 浏览器驱动   

## 属性
- `browsers`: List[[Browser](./python/webdriver/browser/browser.md)], 返回指定浏览器类型的所有打开的浏览器对象。
- `extension`: [WebExtension](./python/webdriver/webextension/webextension.md), 返回指定浏览器类型的浏览器扩展实例，可以针对浏览器做扩展的安装升级等。

## 方法
- [open](./python/webdriver/open.md): 打开浏览器, return a [Page](./browser/page/page.md) 对象。
- [attach](./python/webdriver/attach.md): 根据指定的选择器，绑定到打开的浏览器页面，返回 [Page](./browser/page/page.md) 对象。
- [attach_by_title_url](./python/webdriver/attach_by_title_url.md):根据标题或者url，绑定到打开的浏览器页面，返回[Page](./browser/page/page.md) 对象。

## 示例
```python
from swifthorse import swifthorse as sw

# 安装chrome浏览器扩展
sw.chrome.extension.install()

# 打开浏览器新的页面
sw.chrome.open("www.bing.com")
```
