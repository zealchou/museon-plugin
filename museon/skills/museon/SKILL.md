---
name: "museon"
description: "MuseON：讓你的 AI 依你今天想處理的事，找到合適的 MuseON 用途入口。"
---

# MuseON

讓你的 AI 依你今天想處理的事，找到合適的 MuseON 用途入口。

## 分派

先確認會員今天想完成什麼；意圖不清先問一句，已提供的資訊不重問。依主要目的選下列用途，從本檔所在目錄往上兩層定位套件根目錄，讀取下表相對路徑後接續。明確任務直接分派，不強制先跑新手引導。

| 用途入口 | 套件內檔案 |
|---|---|
| 開始使用 MuseON | `skills/client-onboarding/SKILL.md` |
| 生意診斷與規劃 | `skills/biz-diagnostic/SKILL.md` |
| 把問題想清楚 | `skills/deep-think/SKILL.md` |
| 寫作與改稿 | `skills/text-alchemy/SKILL.md` |
| 認識自己與合作夥伴 | `skills/athena/SKILL.md` |
| 工作安排與進度 | `skills/daily-pilot/SKILL.md` |
| 找回與整理筆記 | `skills/knowledge-lattice/SKILL.md` |
| 家庭日常幫手 | `skills/workflow-mama-daily-ai/SKILL.md` |
| 盡職調查 | `skills/dd/SKILL.md` |
| 會議記錄與追蹤 | `skills/meeting-notes/SKILL.md` |
| 提案與報價 | `skills/proposal-quote/SKILL.md` |

入口只負責用途分派。每個工作流與工具各有自己的技能（見下一節）；工作流中的個別節點由主機當次目錄提供，不另做 skill、不硬編節點目錄或工作流順序。跨用途沿既有成果交接；真實會議交會議用途、模擬圓桌交思考用途，查舊紀錄交筆記用途。

## 工作流與工具技能

會員直接說出要做哪個工作流或用哪個工具時，可從本檔所在目錄往上兩層定位套件根目錄，讀下表對應技能；會議記錄的技能是上表的「會議記錄與追蹤」。技能只說明何時用、呼叫哪個 MuseON 工具與 method、前後怎麼搭配；是否已列出以當次連線為準。

| 工作流或工具 | 套件內檔案 |
|---|---|
| 七步成思 | `skills/seven-steps/SKILL.md` |
| 市場研究 | `skills/market-research/SKILL.md` |
| 能量解讀 | `skills/energy-reading/`（資料夾內的 SKILL.md） |
| 圓桌 | `skills/roundtable/SKILL.md` |
| 商業診斷 | `skills/business-diagnosis/SKILL.md` |
| 決策 | `skills/decision/SKILL.md` |
| 反思回顧 | `skills/reflection-review/SKILL.md` |
| 人際處境 | `skills/relationship-situation/SKILL.md` |
| 挑戰教練 | `skills/challenge-coach/SKILL.md` |
| 數位提案 | `skills/digital-proposal/SKILL.md` |
| 需求釐清 | `skills/intake/SKILL.md` |
| 短影音爆款 | `skills/short-video-hook/SKILL.md` |
| 活動洞察包 | `skills/event-pack/SKILL.md` |
| 商會名片 | `skills/member-card/SKILL.md` |
| 結晶物語 | `skills/crystal-story/SKILL.md` |

## 連線與完成條件

只使用當次連線實際列出且本人已授權的 MCP 能力；method 識別字是用途對照，不是固定工具清單。方法不可用時說明尚未接通，不假稱已執行。方法內容留主機，依工具當次回傳繼續。外掛只查回會員本人在 MuseON 已有且來源明確的自有紀錄；來源不明或混合資料不讀取。不讀取或擷取 Claude 的記憶、聊天歷史、對話摘要或使用者檔案；不以對話建立畫像或改變跨次行為。會員明確要求記下筆記、摘要、目標或待辦時，才可用 museon.secretary.record.write 保存；沒開口就不存。保存關閉時，照工具回應告知會員，不自行繞過。不得呼叫查後名片整理能力；本人授權不解除上述讀取、畫像與名片整理限制。對外動作依本人當次授權，工具成功才報完成。

<!-- BEGIN MUSEON ENTRY GUIDE -->
MuseON 使用導引｜入口說明版本 0.1.6。來源：zealchou/museon-plugin。指南：museon://guide/usage；公開說明：https://muse-on.biz/mcp-agent.md。

沿用既有用途入口分流：人際處境由 athena／deep-think 導向 relationship-situation，挑戰教練由 deep-think／daily-pilot 導向 challenge-coach，反思回顧由 daily-pilot／knowledge-lattice 導向 reflection-review，需要做選擇由 deep-think 導向 decision；其餘入口遇到這些需求也沿此分派，不新增入口，方法以當次已授權目錄為準。

當會員請你使用 MuseON 時，在本次對話第一次使用時核對可取得的服務說明版本。能讀 museon://guide/usage 就讀；不支援 resource 時，不反覆嘗試不存在的工具。有網頁讀取能力時可讀公開說明，否則提供 https://muse-on.biz/mcp 請會員貼入目前說明，並繼續原任務可用的部分。

只以實際啟用的套件或本對話已讀說明比對；下載目錄、原始碼與使用者口述不算安裝證據。只比較同來源的正式三段版號，按數字比較（0.9.0 比 0.10.0 舊）；來源不明、缺版號、預發布、快取或資訊衝突時說「版本尚未確認」。較舊才提示更新；本機較新時說「服務宣告較舊，需核對」，不自動降級。同版通常不提示；只在說明缺少、較舊或衝突時，依套件、版號與狀態在同一對話簡短提醒一次。只有新版本、會員明確重查或資訊遺失才重查。

ChatGPT 連上 MCP 不會安裝這套 12 支入口 Skill；可說「已讀此版本說明」，不可說「已安裝 Skill」。無法看見安裝清單時說「無法確認」。連線成功、已安裝入口與已讀說明分開確認。不要為版本檢查修改設定、安裝、登入、保存對話或上傳安裝清單；既有資料與工具限制仍適用。
<!-- END MUSEON ENTRY GUIDE -->
