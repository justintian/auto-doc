# WebElement

- 扩展: [PageElement](./../../../../../python/pageelement/pageelement.md) 

**WebElement 类继承于PageElement, 包含网页元素特有的操作和属性列表**  

## 属性

- `parent`: 父元素，返回 WebElement。  

- `children`: 子元素列表，返回List[WebElement]。  

- `next`: 下一个兄弟节点，返回 WebElement。  

- `previous`: 上一个兄弟节点，返回 WebElement。  

## 方法
- [child](./child.md)：返回指定序号的子元素，当前仅支持web元素。
- [set_property](./set_property.md): 设置属性值。  
- [execute_js](./execute_js.md): 在当前网页元素上执行js。    
- [execute_js_file](./execute_js_file.md): 在当前网页元素上执行js文件。    
- [find_element](./find_element.md)：返回指定选择器对应的网页元素，如果匹配多个，默认返回第一个。 
- [find_element_by_xpath](./find_element_by_xpath.md)：根据指定xpath定位网页元素，如果匹配多个，默认返回第一个。
- [find_element_by_css_selector](./find_element_by_css_selector.md)：根据指定css_selector定位网页元素，如果匹配多个，默认返回第一个。
- [find_elements](./find_elements.md)：返回指定选择器的相似网页元素列表。
- [find_elements_by_xpath](./find_elements_by_xpath.md)：根据指定xpath定位网页元素，返回相似元素列表。
- [find_elements_by_css_selector](./find_elements_by_css_selector.md)：根据指定css_selector定位网页元素，返回相似元素列表。
- [scroll](./scroll.md)：滚动网页元素的滚动条。


