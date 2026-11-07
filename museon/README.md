讓你的 AI 依你今天想處理的事，找到合適的 MuseON 用途入口。

# MuseON

## 開始使用 MuseON

讓你的 AI 帶你了解 MuseON 能幫什麼忙，從今天最想處理的一件事開始。

## 生意診斷與規劃

用 MuseON 的方法，讓你的 AI 陪你找出生意卡在哪裡，整理市場機會、合作風險與下一步方案。

## 把問題想清楚

用 MuseON 的方法，讓你的 AI 陪你釐清問題、比較取捨，或從不同觀點挑戰想法。

## 寫作與改稿

讓你的 AI 把想法寫成文章、文案或訊息，也能依讀者與場合調整語氣。

## 認識自己與合作夥伴

讓你的 AI 陪你了解自己的狀態、整理人際互動，或尋找合適的合作夥伴。

## 工作安排與進度

讓你的 AI 陪你排好工作順序、整理待辦，並在你回來時一起核對進度。

## 盡職調查

用 MuseON 的方法，讓你的 AI 陪你查證企業、個人、合作或投資的背景與風險，整理決定前還缺哪些依據。

## 會議記錄與追蹤

用 MuseON 的方法，讓你的 AI 陪你把會議內容整理成結論、承諾與待辦，接著核對後續進度。

## 提案與報價

用 MuseON 的方法，讓你的 AI 陪你釐清方案與條件，整理有依據的提案和報價。

## 找回與整理筆記

讓你的 AI 找回你在 MuseON 記過的重點，也能把這次的心得整理成日後好查找的筆記。

## 家庭日常幫手

讓你的 AI 陪你安排備餐、接送與親子相處，把家裡每天要做的事理出頭緒。

## 安裝步驟（Claude Code）

1. 在終端加入公開 marketplace 並安裝：

   ```bash
   claude plugin marketplace add zealchou/museon-plugin
   claude plugin install museon@museon
   ```

2. 開新 session，在 `/plugin` 核對啟用；在 `/mcp` 檢查 `plugin:museon:museon`，依提示由本人登入及允許授權。
3. 在 `/skills` 或 `/` 選單核對 MuseON 與用途入口。看不到入口、登入失敗或工具出錯時，保留版本與錯誤訊息，核對 plugin 是否啟用及 `/mcp` 連線狀態。

## Claude 網頁／Desktop／Cowork

在支援 plugin 的帳號開啟 **Customize → Plugins → Add → Add marketplace → Add from a repository**，填 `zealchou/museon-plugin`；到 Discover 選 MuseON → Add，再依提示登入與授權。可用性依方案、組織策略與實際介面確認。

## ChatGPT 開發者模式（MCP 連線）

合資格帳號／管理員在 ChatGPT web 啟用 developer mode，建立自訂 MCP app，填 `https://muse-on.biz/mcp`、選 OAuth，依介面 Scan Tools、完成本人授權並 Create。這個操作只設定 MCP 連線與工具，不會安裝本包的 12 支 skills。

## Codex CLI（MCP 與 skills 分開設定）

若不用 plugin，可先在終端設定 MCP：

```bash
codex mcp add museon --url https://muse-on.biz/mcp
codex mcp list
```

依該版 Codex 的 OAuth 提示完成本人登入。再將本套件 `skills/` 下的 12 個獨立資料夾放進使用者 `~/.agents/skills/` 或專案 `.agents/skills/`，開新 session 核對載入。已有 plugin 連線時，先辨識現有設定，避免重複設定同一 MCP。

操作參考：[Claude plugin 安裝](https://code.claude.com/docs/en/plugins/install)、[Claude 網頁 plugin](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)、[ChatGPT developer mode](https://help.openai.com/en/articles/12584461-developer-mode-and-full-mcp-connectors-in-chatgpt)、[OpenAI MCP](https://developers.openai.com/learn/docs-mcp)。

## Privacy

[Privacy](https://muse-on.biz/privacy)
