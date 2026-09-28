# Where is my token

[简体中文](README.md) · **繁體中文** · [English](README.en.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [한국어](README.ko.md)

[下載 macOS 測試版](https://github.com/xiu-hu404/where-is-my-token/releases/tag/v0.1.0-beta.4) · [回報問題或提出建議](https://github.com/xiu-hu404/where-is-my-token/issues)

**為 macOS 打造的 Codex Token 用量監測與費用統計工具。**

任務還沒完成，Token 卻一直增加，到底花在哪裡？Where is my token 讓你隨時看見每段對話的用量、快取命中率與上下文使用量。留意快取命中率偏低或日誌持續增長的情況，找出值得檢查的地方，再決定如何調整 Codex 的使用方式。

![Codex 使用情境：在對話上方查看 Token 用量](docs/images/codex-workflow-en.jpg)

Codex 工作區為情境示意；懸浮列擷取自實際介面，對話與數字皆為範例。展示圖統一使用英文。

## 能幫上什麼忙

- **看清用量。** 查看每段對話與所屬專案累計的 Token，不必自行翻找日誌。
- **掌握調整線索。** 近期快取命中率持續偏低或日誌持續增長時，在懸浮列中提醒。
- **了解費用。** 依已知 API 定價估算金額，透過收據查看各模型用量及消耗最多的輪次。
- **保留決定權。** 在本機計算，不額外呼叫模型、不向對話發送訊息、不自動更換模型或刪除檔案。

可固定一段對話、跟隨啟用後最新送出的使用者訊息，或查看所屬專案的總用量。介面隨 Codex 視窗啟停，依 macOS 語言顯示，內建簡中、繁中、英文、日文、法文、德文與韓文。ChatGPT、Codex 與模型名稱保留原名。

## 用量與提醒

![用量收據：Token、耗時、API 估算費用與輪次明細](docs/images/receipt-showcase-en.jpg)

需要時再產生收據。可選對話或專案、用量最高的前 N 輪或全部輪次、58／80 mm 紙寬，以及是否顯示 API 金額。列印預設關閉；啟用後，可選擇已配對的傳統藍牙裝置或系統印表機，再透過 macOS 列印視窗確認。

![快取命中率偏低的橘色提示與懸停說明](docs/images/advisory-showcase-en.jpg)

橘色狀態點提示近期快取命中偏低；右側呈現將游標停在狀態點上時顯示的說明。這是檢查線索，不能直接證明 Token 被浪費。

## 安裝與停用

目前為 **0.1.0-beta.4 測試版**，支援 **Apple Silicon Mac、macOS 15 以上**。執行環境已內建，無須另外安裝 Python 或 Xcode。

取得測試包後：

1. 解壓縮 `Where-is-my-token-0.1.0-beta.4-macOS-arm64.zip`。
2. 開啟 `Where is my token.app`，選擇安裝並啟動。
3. 要停用時，執行 `Disable.command`；設定與統計資料會保留。

關閉最後一個 Codex 一般視窗後，監測列與資料收集服務會退出；重新開啟視窗後恢復。最小化不會停止監測，背景會保留輕量的啟動監聽程式。點選懸浮列的 × 會收合成 W·T 圓形按鈕，再點一下即可展開。

目前安裝包尚未取得 Developer ID 簽署或 Apple 公證。這是搭配 Codex 使用的本機工具，不是匯入 Codex 插件目錄的 ZIP，也不需要啟用 Codex Hooks。

## 隱私與目前限制

- 在本機處理可讀取的 Codex 記錄，保存必要統計，不複製完整對話，也不上傳統計資料。資料保存在 `~/Library/Application Support/Where is my token/`。
- 跟隨的是最新送出的訊息，不是目前點選的對話或尚未送出的草稿。
- 快取命中率不是回答正確率；上下文使用量不能判斷內容是否必要，也不會單憑佔用量高就警示。
- 僅統計本機已收集的記錄。缺少的用量或價格顯示「—」，不推算訂閱套餐的剩餘 Token。
- API 金額是折算值，不是實際扣款。手動輸入訂閱費與月度分攤目前透過管理命令操作，桌面收據以 API 金額為主。
- 日誌提醒依據檔案大小與修改時間，不代表已測得實際磁碟寫入量。測試時機提醒尚未接入懸浮列。
- 藍牙列印需要相容的 macOS 列印佇列；廠商專用協定與實際出紙尚未驗證。視窗啟停已通過隔離測試，仍需驗證不同 Codex 版本的相容性。

## 使用授權與回饋

本軟體免費閉源提供，**僅限非商業用途，公司內部使用也不允許**。可免費進行非商業的複製、修改、重新封裝與散布；禁止轉售、付費綑綁或收費提供軟體功能。完整規則見[授權條款](LICENSE)。

[回報問題或提出建議](https://github.com/xiu-hu404/where-is-my-token/issues) · [隱私說明](docs/privacy.md) · [第三方聲明](THIRD_PARTY_NOTICES.md)
