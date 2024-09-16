
# browser.get_active_page

```python
def get_active_page(self) -> Page
```  

获取活动的浏览器页面

**返回值:**  
    &emsp;[Page](./page/page.md) 对象, 浏览器页面对象，通过该对象可以继续定位到页面里的元素。

**示例:**
***
```python
from swifthorse import swifthorse as sw

# get browser with type chrome
browser = sw.chrome.browsers[0]

# get active tab
page = browser.get_active_page()

# get tab's title
title = page.title
print(title)
```