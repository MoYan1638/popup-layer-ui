# popup-layer-ui

弹出层（Popup Layer）选型与设计规范 —— 一个面向 AI Agent 的 [WorkBuddy Skill](https://workbuddy.cn)。

当设计或实现 UI 中的提示、反馈、确认框、弹窗、抽屉等临时交互层时，本 skill 提供一套可执行的选型决策与硬性规则，确保弹出层类型选择一致、打扰度最小、文案符合规范。

## 它解决什么问题

AI 生成界面时最常见的毛病之一就是弹出层滥用：该用 Toast 的地方弹 Modal，该走「撤销」的删除却强插二次确认，按钮文案清一色「是/否」。本 skill 把一套实战踩坑出来的规范变成 AI 能直接执行的设计约束。

## 内容速览

- **六类速查表**：Tooltip / Toast / Alert / Popconfirm / Drawer / Modal 的打扰度、消失方式、适用场景对比
- **三问选型法**：①只是传达信息？②需要确认动作？③需要输入大量内容？顺着问完答案自然出来
- **六条硬性规则**：填表弹窗禁蒙层关闭、删除默认走撤销、按钮文案写动作、Toast 单条上限、Alert 黄红语义、Modal 禁套娃
- **移动端差异**：Modal → 全屏/半屏 Sheet、Tooltip → 长按提示、触摸目标 ≥ 44px
- **正误对照示例**：8 个真实场景的「该用 / 别用」

核心排序：**Tooltip < Toast < Alert < Popconfirm < Drawer < Modal**
（Modal 才是完全打断；Drawer 虽面积大但不打断主流程，不要按面积判断打扰度。）

## 安装

解压后将 `popup-layer-ui` 文件夹放入你的技能目录：

```
~/.workbuddy/skills/popup-layer-ui/SKILL.md
```

重启会话即可生效。当对话涉及弹窗、提示、确认框设计时自动触发。

## 作者

**墨言**（[MoYan1638](https://github.com/MoYan1638)）

## License

MIT
