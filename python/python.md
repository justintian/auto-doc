# Overview  

[Swifthorse Python包](https://pypi.org/project/swifthorse/) 支持桌面应用自动化和浏览器自动化, 例如 **Web** 浏览器, **Windows** 应用程序, **Java** 应用程序和**SAP** windows桌面客户端应用.

## 安装python模块

### 系统要求​
|                     | 版本                 | 
|---------------------|------------------------------|
| Python              | 3.7, 3.8, 3.9, 3.10, 3.11    | 
| 操作系统             | 推荐Windows 11, 10或者相应的windows server版本|
 

### 推荐开发工具
- Visual Studio Code

## 安装步骤
```
pip install swifthorse

也可以指定版本安装，例如
pip install swifthorse==1.0.0
```

## 接口文档   
- [录制操作](./python/recorder/recorder.md)：录制器接口.
- [通用操作](./python/globalfunctions/globalfunctions.md)：操作UI元素的全局操作.  
- [窗口操作](./python/window/window.md): 窗口支持的操作.  
- [元素操作](./python/pageelement/pageelement.md): UI元素对象的属性和支持的操作.  
- [浏览器驱动](./python/webdriver/webdriver.md): 浏览器驱动层的操作. 
- [异常定义](./python/exceptions/exceptions.md): 异常定义.  

## 第一个自动化项目示例

```python
import subprocess
from time import sleep
from swifthorse import swifthorse as sw, locator

def main():
    page = sw.chrome.open("https://www.bing.com/")
    page.find_element(
        locator.bing.search_sb_form_q).input_text('RPA')
    page.find_element(locator.bing.svg).click()
    sleep(3)
    page.close()

    process = subprocess.Popen("notepad")
    sw.find_element(locator.notepad.document_15).input_text("RPA")

if __name__ == "__main__":
    main()
``` 