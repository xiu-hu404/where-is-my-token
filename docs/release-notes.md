# Where is my token 0.1.0-beta.4

## English

A small, local token monitor for Codex on macOS. See how much a conversation or project uses, notice low cache reuse, and review the cost of a task on a receipt.

### Included in this beta

- A compact floating bar showing tokens used, cache hit rate, and context usage.
- A pinned conversation, following newly submitted messages, or project totals.
- In-panel advisories for low recent cache reuse and sustained log growth.
- API-price estimates and receipts with model totals, time, and top N or all turns.
- Seven interface languages, selected from the macOS language setting.
- Startup and shutdown with Codex windows, with a bundled runtime and no Codex hooks.

### Download and install

Choose `Where-is-my-token-0.1.0-beta.4-macOS-arm64.zip` for **Apple Silicon Macs running macOS 15 or later**. Unzip it, open `Where is my token.app`, and choose the installation option. Python and Xcode are not needed.

Run `Disable.command` to stop monitoring and disable automatic startup. Settings and usage data are kept.

This is a free, closed-source distribution for **non-commercial use only**. Internal company use and resale are not permitted. Free non-commercial sharing and modification are allowed under [the license](https://github.com/xiu-hu404/where-is-my-token/blob/main/LICENSE). `SHA256SUMS.txt` contains checksums for the attached installer.

### Before you try it

This is a beta, without Developer ID signing or Apple notarization. Installation on a second Mac and behavior across Codex versions have not yet been verified. Intel Macs are not supported by this build.

Following submitted messages does not follow the conversation selected on screen. Only locally collected records are counted. Low cache reuse is a prompt to review the task, not proof of wasted tokens; high context usage alone does not trigger an alert. API amounts are estimates, not actual subscription charges. Printing requires a compatible macOS printer queue, and physical output remains unverified.

Usage statistics stay local. The monitor does not send messages to Codex, make additional model requests, switch models, or delete files.

## 简体中文

为 macOS Codex 制作的轻量本机监测工具。看清对话或项目用了多少 Token，留意低缓存命中，并通过小票回顾任务消耗。

### 本版功能

- 紧凑悬浮条：Token 消耗、缓存命中率、上下文占用。
- 固定对话、跟随新发送的消息，或查看项目汇总。
- 近期低缓存命中与持续日志增长提醒，仅在面板内显示。
- API 费用折算与小票，支持模型合计、耗时、前 N 轮或全部轮次。
- 七种界面语言，跟随 macOS 语言设置。
- 随 Codex 窗口启停，内置运行环境，不注册 Codex 钩子。

### 下载与安装

**Apple Silicon Mac、macOS 15 以上**请选择 `Where-is-my-token-0.1.0-beta.4-macOS-arm64.zip`。解压后打开 `Where is my token.app`，选择安装并启动。无需另装 Python 或 Xcode。

运行 `Disable.command` 可退出监测并关闭自动启动，设置与统计保留。

本软件免费闭源分发，**仅限非商业用途，公司内部使用和转售也不允许**。按[许可条款](https://github.com/xiu-hu404/where-is-my-token/blob/main/LICENSE)可免费进行非商业的分享和修改。`SHA256SUMS.txt` 提供安装包的校验值。

### 测试版说明

当前未做 Developer ID 签名或 Apple 公证，另一台 Mac 的安装和不同 Codex 版本的兼容性仍待验证。此安装包不支持 Intel Mac。

跟随新消息不等于跟随界面选中的对话。统计只覆盖本机已采集记录；低缓存命中是检查线索，不是浪费的证据，也不会单因上下文占用高而报警。API 金额是折算值，不是订阅实扣。打印需要兼容的 macOS 打印队列，实际出纸尚未验证。

统计保留在本机，不向 Codex 发送消息、不额外调用模型、不自动切换模型或删除文件。
