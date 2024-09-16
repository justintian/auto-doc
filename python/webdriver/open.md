---
sidebar_position: 1
sidebar_label: open
---
# WebDriver.open

```python
def open(
        self,
        url: str,
        maximize: bool = True,
        wait_complete: bool = True,
        userdata_folder_mode: Literal["automatic", "default", "custom"] = "automatic",
        userdata_folder_path: str = "",
        args: List[str] = None,
        timeout: int = 30
    ) -> Page 
```

打开浏览器并访问指定的url页面，浏览器扩展需要先安装和启用。


**参数:**  
    &emsp;**url[必需]**: str   
        &emsp;&emsp; 网址字符串, 例如: <https://www.bing.com>.     
    &emsp;**maximize**: bool  
        &emsp;&emsp; 是否要最大化打开的窗口，默认为True。  
    &emsp;**wait_complete**: bool  
        &emsp;&emsp; 是否要等浏览器页面加载完成，默认为True。   
    &emsp;**userdata_folder_mode**:     
        &emsp;&emsp; userdata的类型  
        &emsp;&emsp; `automatic`：自动使用当前环境相应的user data，用户无需指定。    
        &emsp;&emsp; `default`：使用默认的user data目录    
        &emsp;&emsp; `custom`：使用用户指定的目录，通过参数 'userdata_folder_path'指定。  
    &emsp;**userdata_folder_path**: str  
        &emsp;&emsp; 用户指定的user data目录  
    &emsp;**args**: 启动浏览器的其他启动参数， Chromium启动参数列表参见 https://peter.sh/experiments/chromium-command-line-switches/, 例如: args=["--profile-directory=Default"]  
    &emsp;**timeout[可选]**: int  
        &emsp;&emsp; 定位页面元素的超时时间，默认是30秒，单位是秒。 

**返回值:**  
    &emsp;[Page](./browser/page/page.md) 对象, 浏览器页面对象，通过该对象可以继续定位到页面里的元素。

**示例:**
***
```python
from swifthorse import swifthorse as sw

# 打开chrome浏览器，访问必应
page = sw.chrome.open("https://www.bing.com")

```