---
name: "short-video-hook"
description: "短影音爆款：一次問一題問清目的與影片規格，對上品牌與三重漏斗，用熱搜找切入點，每輪 5 個混搭鉤子讓你挑到滿意，再給分鏡、腳本、台詞與審計成績單。"
---

# 短影音爆款

短影音爆款：一次問一題問清目的與影片規格，對上品牌與三重漏斗，用熱搜找切入點，每輪 5 個混搭鉤子讓你挑到滿意，再給分鏡、腳本、台詞與審計成績單。

## 何時用與前後搭配

只在 `museon.method.step` 當次列出的 method 含 `short-video-hook`、而且會員要做一支短影音（問清目的與影片規格、找熱搜切入點、挑鉤子、給分鏡與腳本）時使用。當次沒有列出 `short-video-hook` 就不用，也不要說「已做過短影音爆款」。

## 怎麼呼叫

呼叫 MuseON 的 `museon.method.step`，`method` 帶 `short-video-hook`。第一次只帶 method；之後帶上工具回傳的 run_id，並依工具當次回傳的欄位與格式交回 answer。一次只做工具當次交給你的這一步，不自行跳關、不替會員作答。

屬於用途入口「生意診斷與規劃」（`skills/biz-diagnostic/SKILL.md`）；總入口見 `skills/museon/SKILL.md`。

## 連線與完成條件

只使用當次連線實際列出且本人已授權的 MCP 能力；method 識別字是用途對照，不是固定工具清單。方法不可用時說明尚未接通，不假稱已執行。方法內容留主機，依工具當次回傳繼續。外掛只查回會員本人在 MuseON 已有且來源明確的自有紀錄；來源不明或混合資料不讀取。不讀取或擷取 Claude 的記憶、聊天歷史、對話摘要或使用者檔案；不以對話建立畫像或改變跨次行為。會員明確要求記下筆記、摘要、目標或待辦時，才可用 museon.secretary.record.write 保存；沒開口就不存。保存關閉時，照工具回應告知會員，不自行繞過。不得呼叫查後名片整理能力；本人授權不解除上述讀取、畫像與名片整理限制。對外動作依本人當次授權，工具成功才報完成。

<!-- BEGIN MUSEON ENTRY GUIDE -->
MuseON 使用導引｜入口說明版本 0.1.6。來源：zealchou/museon-plugin。指南：museon://guide/usage；公開說明：https://muse-on.biz/mcp-agent.md。

沿用既有用途入口分流：人際處境由 athena／deep-think 導向 relationship-situation，挑戰教練由 deep-think／daily-pilot 導向 challenge-coach，反思回顧由 daily-pilot／knowledge-lattice 導向 reflection-review，需要做選擇由 deep-think 導向 decision；其餘入口遇到這些需求也沿此分派，不新增入口，方法以當次已授權目錄為準。

當會員請你使用 MuseON 時，在本次對話第一次使用時核對可取得的服務說明版本。能讀 museon://guide/usage 就讀；不支援 resource 時，不反覆嘗試不存在的工具。有網頁讀取能力時可讀公開說明，否則提供 https://muse-on.biz/mcp 請會員貼入目前說明，並繼續原任務可用的部分。

只以實際啟用的套件或本對話已讀說明比對；下載目錄、原始碼與使用者口述不算安裝證據。只比較同來源的正式三段版號，按數字比較（0.9.0 比 0.10.0 舊）；來源不明、缺版號、預發布、快取或資訊衝突時說「版本尚未確認」。較舊才提示更新；本機較新時說「服務宣告較舊，需核對」，不自動降級。同版通常不提示；只在說明缺少、較舊或衝突時，依套件、版號與狀態在同一對話簡短提醒一次。只有新版本、會員明確重查或資訊遺失才重查。

ChatGPT 連上 MCP 不會安裝這套 12 支入口 Skill；可說「已讀此版本說明」，不可說「已安裝 Skill」。無法看見安裝清單時說「無法確認」。連線成功、已安裝入口與已讀說明分開確認。不要為版本檢查修改設定、安裝、登入、保存對話或上傳安裝清單；既有資料與工具限制仍適用。
<!-- END MUSEON ENTRY GUIDE -->
