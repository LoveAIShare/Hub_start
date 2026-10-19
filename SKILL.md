---
name: open-taoxiang-desktop
description: 打开工具箱网站。当用户说"打开工具箱"、"打开工具网站"、"打开工具"时使用。
---

# 打开工具箱网站

打开浏览器并导航到 https://tx3240.t.taoxiangyoushu.com/desktop，窗口持久停留。

## 执行方式

使用桌面控制（computer_use_tool, plane="cu"）打开默认浏览器并加载目标 URL：

```python
import seed_computer_use as cu
import time

# 启动 Chrome
cu.launch_app("Google Chrome#0063457ddf2ec9266eba504e3522f88b1467207224")
time.sleep(3)

# 点击地址栏并输入 URL
cu.click(150, 30)
time.sleep(0.5)
cu.type("https://tx3240.t.taoxiangyoushu.com/desktop")
time.sleep(0.5)
cu.press("Enter")
```

窗口保持打开状态，不会自动关闭。
