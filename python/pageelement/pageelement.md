# PageElement 
**PageElement 类代表一个桌面应用或者浏览器页面上的页面元素，该类中定义了通用的元素的属性和操作方法。**  

## 属性

- `parent`: 父页面元素, 返回 PageElement，当前仅支持web元素。
- `children`: 子元素列表, 返回 list[PageElement],当前仅支持web元素。
- `next`: 下一个兄弟页面元素，返回 PageElement，当前仅支持web元素。
- `previous`: 上一个兄弟页面元素，返回 PageElement，当前仅支持web元素。

## 方法
- [check](./check.md): 勾选目标元素，例如radiobutton, checkbox等类型元素。
- [child](./child.md)：返回指定序号的子元素，当前仅支持web元素。
- [clean_text](./clean_text.md): 清除目标页面元素上的文本内容。
- [click](./click.md)：单击目标元素。
- [double_click](./double_click.md)：双击目标元素。
- [drag_drop](./drag_drop.md): 按住目标元素，然后拖动到目标位置后再松开鼠标按键。
- [focus](./focus.md): 聚焦到目标元素。
- [get_position](./get_position.md): 获取元素位置。
- [get_property](./get_property.md): 获取目标元素的上指定属性的值。  
- [get_size](./get_size.md): 获取目标元素的大小（长宽）。
- [get_text](./get_text.md): 获取目标元素的文本内容。
- [highlight](./highlight.md): 高亮目标元素。
- [hover](./hover.md): 鼠标悬停在目标元素上。
- [input_text](./input_text.md): 在目标元素上输入文本。
- [mouse_down](./mouse_down.md)：在目标元素上按下鼠标。
- [select_item](./select_item.md): 针对下拉框类型的元素，选择指定的选项。
- [select_items](./select_items.md): 针对支持多选的下拉框类型的元素，选择多个选项。
- [send_keys](./send_keys.md): 在目标元素上发送快捷键。
- [take_screenshot](./take_screenshot.md): 对目标元素进行截屏并保存成本地图像。