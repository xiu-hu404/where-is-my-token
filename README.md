# Where is my token

**简体中文** · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [한국어](README.ko.md)

[下载 macOS 测试版](https://github.com/xiu-hu404/where-is-my-token/releases/tag/v0.1.0-beta.4) · [反馈问题或提出建议](https://github.com/xiu-hu404/where-is-my-token/issues)

**Codex Token 用量监测与费用统计 · Codex token usage monitor for macOS**

任务还没结束，Token 已经消耗了不少，却不知道花在了哪里？Where is my token 把每条对话的用量、缓存命中率和上下文占用放在眼前，提醒你关注低缓存复用和持续日志增长，帮助你发现可能的浪费，更有依据地调整 Codex 的使用方式。

![Codex 使用场景：制作网页时查看 Token 用量、缓存命中率与上下文占用](docs/images/codex-workflow-en.jpg)

使用场景示意，非 Codex 实机截图；悬浮条来自实际界面，对话与数字均为示例。

## 为什么用它

- **看清消耗。** 每条对话用了多少 Token，同一个项目累计了多少，不必自己翻日志。
- **发现优化线索。** 近期缓存命中率持续偏低时收到提醒，再决定是否精简重复材料、工具输出或对话内容。
- **看懂成本。** 以 API 定价折算消费，生成包含模型用量与轮次明细的小票，定位消耗较多的轮次。
- **保持工作节奏。** 本机监测，在悬浮条内提醒，由你决定何时调整任务。

它适合正在寻找 **Codex Token 监测器、Token 用量统计、缓存命中率监测或 AI 使用费用计算工具** 的 macOS 用户。低缓存命中是一条检查线索，不能单凭它断定 Token 被浪费。

这是独立开发的项目，与 OpenAI 没有隶属或背书关系。当前为 **0.1.0-beta.4 测试版**。

## 能做什么

- 悬浮小条显示当前监测对话、累计 Token、缓存命中率和上下文占用。
- 固定某条对话，或跟随开启后最近提交的用户消息；支持所属项目汇总。
- 对近期低缓存命中和持续日志增长给出面板提醒，所有建议由你决定是否采纳。
- 按可确认的模型费率折算 API 金额；计费组件支持手工录入订阅月费和自然月分摊。
- 生成热敏小票预览：模型消费、合计、前 N 轮或全部轮次，支持对话／项目范围及 58／80 mm 纸宽。
- 设置页提供已配对经典蓝牙设备和系统打印机选择，打印由系统打印框确认。
- 随 Codex 窗口启停，支持简中、繁中、英文、日文、法文、德文和韩文。

本地计算，不注册 Codex 钩子、不向对话发消息、不额外调用模型、不自动修改任务或删除文件。

## 界面

英文界面截图使用示例数据；不包含私人对话或真实账单。界面会跟随系统语言，内置七种语言。

![任务小票：累计 Token、耗时、API 折算费用及消耗最多的轮次](docs/images/receipt-showcase-en.jpg)

任务完成后，按需回顾累计消耗并生成小票。

![近期缓存命中率较低时的橙色提示及悬停说明](docs/images/advisory-showcase-en.jpg)

悬浮条状态点提示近期缓存命中偏低；右侧展示其悬停提示原文。低命中率是检查线索，不代表已经判定浪费。

<details>
<summary>监测与设置界面</summary>

![英文悬浮监测条](docs/images/overview-en.jpg)

<img src="docs/images/settings-en.jpg" alt="Codex Token 监测设置：刷新频率、提醒、固定对话与项目汇总" width="500">

</details>


## 安装

完整应用要求 **Apple Silicon Mac、macOS 15+**。运行环境已内置，无需另装 Python、Xcode 或其他依赖。

解压 `Where-is-my-token-0.1.0-beta.4-macOS-arm64.zip`，双击 `Where is my token.app`，选择“安装并启动”。停用时双击 `Disable.command`，设置和统计会保留。当前包没有 Developer ID 签名或 Apple 公证。

关闭最后一个 Codex 普通窗口后，悬浮条和采集服务退出；重新打开窗口后恢复。最小化不退出，后台保留轻量启动监听。点击悬浮条的 × 只收起小条，点击 W·T 圆按钮可恢复。

[完整安装说明](docs/install.md) · [隐私与数据](docs/privacy.md)


## 当前边界

- 跟随最近发送不等于跟随界面选中的对话，也不读取未发送草稿。
- 只统计本机可读取的记录；未知用量或价格显示“—”，不推算套餐剩余 Token。
- 缓存命中率不是回答正确率；上下文占用不能证明内容无用。目前不判断内容的语义必要性。
- API 金额是折算值；订阅分摊是按已采集用量计算的估算。桌面小票目前以 API 金额展示为主，完整月费管理仍通过管理命令进行。
- 测试时机分析组件已保留，尚未接入悬浮条。低缓存和日志活动提醒已经接入。
- 蓝牙打印需要兼容的 macOS 打印队列；喵喵机等厂商专用协议和实体打印仍待实机验证。
- 关窗逻辑通过隔离窗口验证，实际 Codex 各版本的关闭／重开行为仍需兼容性验证。

## 使用许可与反馈

本软件免费闭源分发，**仅限非商业用途，公司内部使用也不允许**。允许免费进行非商业的复制、修改和重新打包分发；禁止转售、捆绑收费或收费提供软件功能。完整规则见 [许可条款](LICENSE)。

[反馈问题或提出建议](https://github.com/xiu-hu404/where-is-my-token/issues) · [隐私说明](docs/privacy.md) · [第三方声明](THIRD_PARTY_NOTICES.md)
