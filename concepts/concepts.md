# 自动化基本技术说明

## 概述
在本节中，我们将说明有关 Swifthorse 自动化的技术信息，包括如何利用 Swifthorse 自动化技术使 RPA/自动化项目健壮且易于编辑、编写和维护。 
Swifthorse 自动化在后台组集成了多种自动化技术，Swifthorse 录制器接口 默认使用“auto”模式，这意味着 Swifthorse 将自动检测应用程序类型，并选择合适的后台技术。  
Swifthorse 定义了统一格式的 [元素选择器]（./locator.md） schema 来识别 UI 元素，选择器存储了 UI 元素及其父元素的属性，例如，Windows 应用程序上的按钮、网页上的输入框。

以下技术被广泛使用:
- [UIA](./uia.md): 桌面应用的自动化技术，基于微软UI Automation技术。
- [MSAA](./msaa.md): 桌面应用的另外一种自动化技术，可以作为UIA的有力补充, electron&CEF 等应用或者使用很旧的技术开发的应用使用MSAA可能会更好。
- [Chrome/Edge](./web.md)：浏览器网页自动化技术。
- [图像识别](./image.md): 图像识别可以和其他自动化技术结合使用。

## 自动化技术说明
- [Locator](./concepts/locator.md)
- [Web automation](./concepts/web.md)
- [UIA automation](./concepts/uia.md)
- [MSAA Automation](./concepts/msaa.md)
- [Image Automation](./concepts/image.md)

