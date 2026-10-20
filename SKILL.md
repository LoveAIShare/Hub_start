---
name: Hub_start
description: 打开工具箱网站，并在工具箱全站导航中定位工具/资源/教程。当用户说"打开工具箱"、"打开工具网站"、"打开工具"，或询问某个工具（如视频拆解、去水印、AI 生成 PPT、提取文案等）在工具箱哪里、工具箱有没有某个工具时使用。
---

# 打开工具箱网站

打开浏览器并导航到 https://tx3240.t.taoxiangyoushu.com/desktop，窗口持久停留。

## 查找工具

工具箱按「一级分类 > 二级分类 > 工具」组织，完整清单见 [references/tools-index.md](references/tools-index.md)：共 654 个工具，包含名称、描述、关键词和所在层级，不包含任何工具链接。

查找流程：

1. 读取 references/tools-index.md，按工具名称、描述、关键词匹配用户意图，支持近义说法（如"拆视频"对应"拆解"、"提取文案"）。
2. 命中后按 `<一级分类> > <二级分类> > <工具名>` 的格式回答位置，并补一句它能做什么。
   - 例：用户问"视频一键拆解"，回答：在「会员专享福利【无限使用】 > 运营工具 > 短视频一键拆解」，可输入短视频链接，智能解析结构、节奏与传播策略。
3. 命中多个时给出 2-3 个候选（同样带完整层级），让用户选择。
4. 没有命中时，说明工具箱暂未收录，并给出最接近的分类。
5. 回答中只给分类层级和工具名称，不要输出任何工具 URL 或链接。

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
