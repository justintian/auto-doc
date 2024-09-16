# Browser

**Browser class provides methods to browser operations.**

## 属性 
- `pages`: List[[Page](./page/page.md)], 获取当前浏览器对象的Page对象列表

## 方法
- [close](./close.md): 关闭浏览器对象，会关闭该窗口的所有的浏览器页面。
- [get_active_page](./get_active_page.md): 获取活动的浏览器页面，返回 [Page](./page/page.md).  
- [get_page](./get_page.md): 根据标题或者url获取相应的浏览器页面对象，返回[Page](./page/page.md).  
- [maximize](./maximize.md): 最大化浏览器窗口。
- [new_page](./new_page.md): 打开新的浏览器页面, 返回 [Page](./page/page.md).  
