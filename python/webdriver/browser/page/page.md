# Page

**Page 类定义浏览器页面支持的操作方法和属性列表。**

## 属性
- `title`: str, 浏览器页面标题。
- `url`: str, 浏览器页面网址。
- `is_active`: bool, 表示该页面是否是活跃页面。
- `browser`: [Browser](./../browser.md), 返回当前页面所在的浏览器窗口对象。

## 方法
**在网页元素上的操作**
- [find_element](./find_element.md): 返回指定选择器对应的网页元素，如果匹配多个，默认返回第一个。 
- [find_element_by_xpath](./find_element_by_xpath.md): 根据指定xpath定位网页元素，如果匹配多个，默认返回第一个。
- [find_element_by_css_selector](./find_element_by_css_selector.md): 根据指定css_selector定位网页元素，如果匹配多个，默认返回第一个。
- [find_elements](./find_elements.md): 返回指定选择器的相似网页元素列表。
- [find_elements_by_xpath](./find_elements_by_xpath.md): 根据指定xpath定位网页元素，返回相似元素列表。
- [find_elements_by_css_selector](./find_elements_by_css_selector.md): 根据指定css_selector定位网页元素，返回相似元素列表。
- [is_existed](./is_existed.md): 根据指定的选择器，判断网页元素是否存在。  
- [is_existed_by_xpath](./is_existed_by_xpath.md): 根据指定的xpath字符串，判断网页元素是否存在。 
- [is_existed_by_css_selector](./is_existed_by_css_selector.md): 根据指定的css_selector字符串，判断网页元素是否存在。 
- [wait_locator](./wait_locator.md): 在指定的时间内，等待指定选择器的网页元素出现。
- [wait_locator_by_xpath](./wait_locator_by_xpath.md): 在指定的时间内，等待指定xpath字符串的网页元素出现。
- [wait_locator_by_css_selector](./wait_locator_by_css_selector.md): 在指定的时间内，等待指定css_selector字符串的网页元素出现。
- [wait_locator_disappear](./wait_locator_disappear.md): 在指定的时间内，等待指定选择器的网页元素消失。
- [wait_disappear_by_xpath](./wait_disappear_by_xpath.md): 在指定的时间内，等待指定xpath字符串的网页元素出现。
- [wait_disappear_by_css_selector](./wait_disappear_by_css_selector.md): 在指定的时间内，等待指定css_selector字符串的网页元素出现。

**在网页上的操作**
- [activate](./activate.md): 前置当前的网页页面。  
- [close](./close.md): 关闭当前页面，如果所在的浏览器窗口没有其他页面，那么浏览器窗口也会被关闭。
- [goto](./goto.md): 访问指定的网址。
- [refresh](./refresh.md): 刷新页面。
- [scroll](./scroll.md)：滚动浏览器页面的滚动条。
