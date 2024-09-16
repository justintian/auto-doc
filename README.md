---
sidebar_position: 1
---
# 安装说明

## 先决条件
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

## 第一个自动化项目样例


```python
import subprocess
from time import sleep
from swifthorse import swifthorse as sw, locator

def main():
    page = sw.edge.open("https://www.bing.com/")
    page.find_element(
        locator.new_store.sample.bing.search_sb_form_q).input_text('RPA')
    page.find_element(locator.new_store.sample.bing.svg).click()
    sleep(3)
    page.close()

    process = subprocess.Popen("notepad")
    sw.find_element(locator.new_store.sample.notepad.document_15).input_text("swifthorse")

if __name__ == "__main__":
    main()
``` 
