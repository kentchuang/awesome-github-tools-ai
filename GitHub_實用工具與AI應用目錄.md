# 🛠️ GitHub 實用工具與AI應用目錄

本目錄彙整了所有 **GitHub 好用工具、AI 應用、精選套件及學習資源**，並在下方提供對應的詳細功能說明，方便您快速查閱與使用。

---

## 快速導覽目錄
1. [🤖 AI 輔助與 Agent 相關工具](#-ai-輔助與-agent-相關工具)
2. [💻 大語言模型與本地部署](#-大語言模型與本地部署)
3. [📄 文件與資料解析處理工具 (OCR / PDF / 轉檔 / 隱私脫敏)](#-文件與資料解析處理工具-ocr--pdf--轉檔--隱私脫敏)
4. [🌐 網路爬蟲與資料擷取](#-網路爬蟲與資料擷取)
5. [⚡ 實用與效能優化工具](#-實用與效能優化工具)
6. [📈 金融、交易與生活助手](#-金融交易與生活助手)
7. [🎬 影音與串流工具](#-影音與串流工具)
8. [🔄 工作流自動化](#-工作流自動化)
9. [📚 AI 學習資源、電子書與認證指南](#-ai-學習資源電子書與認證指南)

---

## 🤖 AI 輔助與 Agent 相關工具

### 1. Hermes AI Agent 系列
* **功能簡介**: 可以在本機端「做事」的 AI Agent 助理。它不僅能聊天，還能讀取專案檔案、修改程式碼、執行終端機指令（如跑測試、啟動服務），並透過安裝各式 Skills 來擴充功能（如 Freqtrade 量化研究 Skill、前端設計 Skill 等）。

---

### 2. [Codebase Memory MCP](https://github.com/DeusData/codebase-memory-mcp) (7 大爆紅 Skill 之一)
* **功能簡介**: 能將整個 Codebase 程式庫轉換成 AI Agent 查得到的「3D 知識圖譜」。在 Claude Code、Cursor 或 Codex 中特別實用，能在大型專案中協助 AI 瞬間讀懂檔案關聯，實測可視覺化展示數百個檔案與數千個節點。

---

### 3. [Webwright](https://github.com/microsoft/Webwright)
* **開發團隊**: 微軟 (Microsoft)
* **功能簡介**: 擁有「終端機控制權」的瀏覽器自動化框架。不同於傳統 Playwright 無腦將網頁原始碼塞滿 Context Window，Webwright 會讓 Agent 在本機端產生並迭代一個可重複執行的 Python 腳本，透過無頭瀏覽器截圖自我驗證抓取資料的正確性。

---

### 4. [linebot-multimodal-rag](https://github.com/kkdai/linebot-multimodal-rag)
* **作者**: Evan Lin
* **功能簡介**: 基於 Google Gemini API File Search 打造的 LINE Bot 多模態 RAG 知識庫。支援將文字、圖片、影片、音訊共享於同一個向量空間以實現「以圖找文 / 以文找圖」，並具備多租戶 Metadata 過濾與頁級引用（直接標註出自 PDF 第幾頁），僅需不到 600 行 Python 即可實作。

---

### 5. [rag-anything MCP](https://github.com/jesse-merhi/rag-anything-mcp)
* **功能簡介**: 企業知識庫 MCP 工具。使用者只需以自然語言提問，Agent 即可透過 MCP tools 從 PDF、LINE、Discord 等多元渠道的散亂文件中查詢解答並附上來源。支援多入口對話流回流追蹤。

---

### 6. [Openhanako](https://github.com/liliMozi/openhanako)
* **功能簡介**: 開源的「類龍蝦 (Claw/Cline)」AI 助手。原生支援 Windows 系統且設定簡單（填入 API Key 即可），支援多 Agent 能力，適合不想折騰 Linux 或虛擬機環境的開發者。

---

### 7. [Caveman](https://github.com/juliusbrussee/caveman)
* **功能簡介**: 專門掛載於 Claude Code、Cursor 或 Gemini CLI 的「山頂洞人模式」Token 節省外掛。能自動省略所有主詞、冠詞與客套過渡句（例如：「好的，這就為您修改」），直接以最短的技術單字輸出，可暴力節省約 75% 的 API Token 並提升輸出速度。

---

### 8. [agency-agents](https://github.com/msitarzewski/agency-agents)
* **作者**: msitarzewski
* **功能簡介**: 支援一鍵部署 147 個不同領域（包含設計、學術、工程、遊戲開發、行銷等）的 AI 員工 Agent 專案。

---

### 9. [Headroom](https://github.com/headroomlabs-ai/headroom) (7 大爆紅 Skill 之一)
* **功能簡介**: 本地運行的 AI Agent 上下文壓縮層。在資料傳給大模型前，會先過濾與壓縮工具輸出、系統日誌、檔案內容和 RAG 切片，壓縮率達 60%~95%。支援「可逆壓縮」(CCR)，當 AI 需要時能自動還原完整資料，避免 Context Token 暴漲的痛點。
* **與 Caveman 的差異**: Headroom 著重於**優化輸入端**（將讀取的 Context 裁剪精煉後再給 AI）；而 Caveman 著重於**優化輸出端**（讓 AI 回答時使用山頂洞人極簡模式省略客套話）。兩者結合能達到極致的 Token 節省。

---

### 10. [Agent-Reach](https://github.com/Panniantong/Agent-Reach) (7 大爆紅 Skill 之一)
* **功能簡介**: 給 AI 代理配備上網的「眼睛」。作為網頁資料的路由器、安裝器與健康檢查器，讓 AI 代理能夠直接調用 `yt-dlp` 等 upstream 開源工具來瀏覽、搜尋和讀取包含 Twitter/X、Reddit、YouTube、GitHub、Bilibili、小紅書等 13+ 個社群平台，免去官方昂貴的 API 費用。

---

### 11. [Agent Skills](https://github.com/addyosmani/agent-skills) (7 大爆紅 Skill 之一)
* **功能簡介**: 專門為 AI 程式碼編寫代理設計的生產級工程技能庫。透過將「專案規劃」、「測試撰寫」、「安全性稽核」等高級工程流程封裝成標準的 Agent Skills 格式，讓 AI 代理在遇到對應任務時能主動加載最佳實踐，產出更安全、更符合工程規範的程式碼。

---

### 12. [SkillSpector](https://github.com/NVIDIA/SkillSpector) (7 大爆紅 Skill 之一)
* **開發團隊**: NVIDIA
* **功能簡介**: NVIDIA 開源的 AI 代理技能安全掃描器。為了避免部署惡意或含有安全漏洞的 AI Skills，SkillSpector 會在部署前進行靜態分析與 LLM 語意分析，檢測包括 Prompt 注入、敏感資料洩漏、特權提升和 MCP 工具 Poisoning 等 16 種類別共 64 種漏洞模式，並產出風險評估報告。

---

### 13. [mattpocock/skills](https://github.com/mattpocock/skills) (AI Agent 技能庫)
* **功能簡介**: 由前 Vercel 工程師 Matthieu (Matt) 分享在 GitHub 上的 AI Agent 技能庫。內含多個能大幅提升開發與專案規劃效率的實用技能，特別適合在與 AI 協作時進行需求對齊與流程管理。本專案透過一個路由器指令進行串接與流程引導。
* **專案網址**: [mattpocock/skills](https://github.com/mattpocock/skills)
* **安裝指令**: `npx skills add mattpocock/skills` (安裝後可執行 `/setup-matt-pocock-skills` 初始化)
* **核心技能說明**:
  * **問答路由器 (Ask Matt - `/ask-matt`)**: 作為技能庫的路由中心，引導 AI 根據使用者的開發階段（從 Idea 到最終上線）呼叫適合的 Skill 流程。
  * **Grill Me (需求訪談技能 - `/grill-me`)**: 扮演「開工前的檢察官」角色。在專案初期反過來對使用者進行深度拷問與訪談（釐清開發動機、技術框架、限制等模糊細節），避免 AI 認真地「亂做」或猜測需求，拉高專案完整度與減少重構時間。
  * **Grill with Docs (文件對齊技能 - `/grill-with-docs`)**: 適用於既有開發專案。讓 AI 針對既有文件與使用者對齊所有的「文件定義、審核標準、錯誤管理」，並在專案中留下 `CONTEXT.md` 和設計決策記錄（ADRs）。
  * **to-spec & to-tickets (PRD 與任務拆解技能 - `/to-spec` / `/to-tickets`)**: 將前述訪談拷問出來的內容，直接轉換為產品需求文件（PRD / Spec）與可執行的任務票券（Tickets），並自動規劃 blocking dependencies。
  * **to-questionnaire (需求問卷產生技能 - `/to-questionnaire`)**: 當要做決定且關鍵資訊只有同事或利害關係人知道時，自動產生精準的 Markdown 問卷。只問核心事項、對齊資訊落差，並預留填答空位，最後自動附帶開放式反思問題。
  * **TDD (測試驅動開發技能 - `/tdd`)**: 在開發時執行，讓 AI 根據 spec 進行每個功能的測試（紅燈與綠燈案例測試），確保專案執行中最大程度降低 Bug 發生機率。
  * **Code Review (代碼雙軸審查技能 - `/code-review`)**: 針對標準規範（Standards）與功能規格（Spec）對程式碼進行雙軸審核，確保安全性與品質。

---

### 14. [github/spec-kit](https://github.com/github/spec-kit) (規格驅動開發工具包)
* **功能簡介**: 由 GitHub 官方推出的 AI 規格驅動開發 (Spec-Driven Development, SDD) 工具包。旨在終結盲目的「直覺式 Prompt 開發 (Vibe Coding)」，將開發流程系統化拆解為定義專案憲法（Constitution）、撰寫規格書（Specify）、產生實作計畫（Plan）及拆解任務（Tasks）等階段，讓 AI 代理嚴格對齊專案目標。
* **專案網址**: [github/spec-kit](https://github.com/github/spec-kit)
* **安裝指令**: 使用 `uv` 安裝：`uv tool install specify-cli --from git+https://github.com/github/spec-kit`
* **與 mattpocock/skills 的比較與選擇建議**:
  * **核心哲學**: `spec-kit` 強調系統化、端到端的 Rigorous（嚴密性），以 spec 作為 living artifact 並整合至專案特定結構（如 `.specify/` 目錄）；而 `mattpocock/skills` 則提倡輕量、靈活的「模組化 Skills/MCP」來保護開發者的控制權。
  * **適用場景**:
    * **選擇 spec-kit**: 適用於中大型專案、團隊協作，或希望從需求到實作留下嚴密追蹤軌跡的場景。
    * **選擇 mattpocock/skills**: 適用於個人敏捷開發、需求非常模糊需要拷問引導（使用 `/grill-me` 互動），或著重在獨立的測試驅動開發（`/tdd`）與雙軌審查（`/code-review`）的場景。

---

### 15. [說人話 speak-human-tw](https://github.com/Raymondhou0917/speak-human-tw)
* **功能簡介**: 專為繁體中文設計的「去 AI 味」改寫工具（Skill）。可精準偵測 35+ 種常見的 AI 中文寫作痕跡（如誇大意義、說教深度腔、公式化段落等），並將簡體中文、中國用語及半形標點符號轉換為台灣在地化的寫法。特別適用於 Claude Code、Codex、Cursor 等 AI Agent，提供「先標出問題，確認後再改寫」的兩輪安全修改機制，協助創作者與開發者產出更自然、更像真人寫作的文案。

---

### 16. [Multi-AI-Chat-Desktop](https://github.com/teddashh/multi-ai-chat-desktop)
* **作者**: Theodore Huang
* **功能簡介**: 將 ChatGPT、Claude、Gemini、Grok 四大多模態 AI Web Chat 整合在同一個桌面視窗中的開源工具。免填 API Key，直接使用官方 Web 介面與帳號登入，不透過中間伺服器儲存隱私。支援 Windows、macOS、Linux 與 Chrome Extension，內建繁中/英文/日文/德文多語系與三種主題，並附帶 Claude Code 與 Codex 專用 Agent Skills。

---

### 17. [open-code-review](https://github.com/alibaba/open-code-review)
* **開發團隊**: 阿里巴巴 (Alibaba)
* **功能簡介**: 專門用於程式碼審查 (Code Review) 的開源專案與模型。在 AACR-BENCH 基準測試中，程式碼審核品質與採納率 (>30%) 顯著優於通用型 AI (如 Claude Code、Codex)，能更精準給出如密碼雜湊 cost factor、安全弱點等具體修正建議，並大幅節省代碼審核的 Token 成本。

---

### 18. [codex-plugin-cc](https://github.com/openai/codex-plugin-cc)
* **開發團隊**: OpenAI
* **功能簡介**: OpenAI 官方釋出的 Claude Code 外掛。安裝後可在同一場 Claude Code 工作階段 (session) 中直接呼叫 Codex 執行代碼審查 (Code Review)、對抗式審查，或是當任務卡住時一鍵整包交由 Codex 救援 (Rescue)，實現多模型協同開發。

---

### 19. [Index (Laminar)](https://github.com/lmnr-ai/index)
* **開發團隊**: Laminar
* **功能簡介**: 將網頁瀏覽器封裝為可呼叫 API 的強大 AI 瀏覽器 Agent。在 WebVoyager 評測達到 92% 的超高準確率。支援終端機一行指令 `index run` 執行、本機 Chrome Session 複用、多模態模型 (Claude/Gemini) 推理，能以一句話自動抓取網頁資料並寫入 Google 試算表，內建視覺化操作回放與步驟追蹤。

---

### 20. [Ego-lite](https://github.com/citrolabs/ego-lite)
* **功能簡介**: 人類與 AI Agent 共同協作的專屬瀏覽器。解決傳統自動化 Agent 遇到驗證碼、雙因子認證 (2FA) 或登入狀態失效時卡死的問題；當遇到需人工授權的流程時，人類可無縫接管操作，完成後再交由 Agent 繼續執行。

---

### 21. [harness-starter-kit](https://github.com/agentcrew-academy/harness-starter-kit)
* **開發團隊**: AgentCrew Academy
* **功能簡介**: 專為 Claude Code 設計的防護 Hooks 與技能啟動套件。核心包含三大防護 Hook：
  * **claim-guard hook**: 避免 AI 幻覺與說謊（當 AI 聲稱已驗證或查不到時，自動檢查是否有調用驗證指令與 tool call，未附證據則強制重做）。
  * **no-emoji hook**: 自動掃描並移除 AI 寫入文件中的 emoji，維持專業乾淨排版。
  * **lint-check hook**: 統一知識庫與筆記格式規範，防止格式發散。

---

### 22. [Kiro Crew](https://github.com/kirodotdev/KiroCrew)
* **開發團隊**: AWS (原 MeshClaw)
* **功能簡介**: AWS 內部已有超過 3.9 萬人採用的開源多代理協作工具 (Multi-Agent System)。可同時分派多個 AI 代理平行處理 Issue 工單、異常調查與系統搬遷，並持久化保存專案脈絡、排程與修正紀錄，即使工程師離線休眠，Agent 也能持續推進工作。

---

### 23. [HermesOffice (GenOffice)](https://github.com/genspark-ai/genoffice)
* **功能簡介**: 專為 AI 原生設計的免費開源辦公套件。涵蓋文件處理器 (Docs)、試算表 (Sheets)、簡報 (Slides) 及 PDF 模組，原生整合 Hermes Agent，使用者只需將需求連結丟給 Agent 即可自動產出各類辦公文件與圖表。

---

### 24. [herdr](https://github.com/herdrdev/herdr)
* **功能簡介**: 讓本機 AI Agent 在背景持續運行的排程與執行工具。即使使用者闔上筆記型電腦螢幕，已指派的前端 Agent（如頁面重構）與後端 Agent（如補充 API 測試）仍能在背景無中斷持續運作完成任務。
* **多 Agent 自動化工作流協同架構**:
  * **A (流程控制角色 - Codex)**: 負責拆解總體目標、呼叫 `herdr agent wait` 進行非同步等待與多 Agent 調度。
  * **B (執行者 - OpenCode)**: 專注於具體功能開發、專案建置與代碼編寫。
  * **C (驗證者 - Claude)**: 執行驗證缺口檢視與測試，通過後核准並標記下一階段任務，實現零死角的多 Agent 自律閉環。

---

### 25. [Claude 5 大實用 Skills 與外掛精選指南](#-ai-輔助與-agent-相關工具)
* **功能簡介**: 彙整社群熱推的 5 個高生產力 Claude / AI Agent 外掛：
  1. **Stop Slop**: 自動移除 AI 腔調、破折號與套話，使文案像真人撰寫。
  2. **Claude Mem**: 跨對話持久記憶，記錄專案與偏好。
  3. **UI/UX Pro Max**: 內建 50+ UI 風格與 99 條 UX 設計規範，生成專業級介面。
  4. **Task Observer**: 靜默觀察工作流並自動優化專屬 Skills。
  5. **Find Skills**: 以自然語言搜尋與一鍵安裝所需 Skills。

---

### 26. [OpenWorker](https://github.com/andrewyng/openworker)
* **開發團隊**: 吳恩達團隊 (Andrew Ng / Rohit Prasad)
* **官方網站**: [openworker.com](https://openworker.com)
* **功能簡介**: 在本機電腦上運行的開源 Local-first AI 數位員工。打破純聊天機器人僅能輸出文字的限制，能跨工具自動操作本地檔案、整理行事曆、發送 Slack 訊息並產出最終交付檔案。具備 Local-first 隱私架構，支援自備 API Key 或連接本地 Ollama 大模型；內建嚴謹的 Check-in 授權機制，在執行關鍵寫入或發送前會主動請求使用者確認。

---

### 27. [reverse-skill](https://github.com/zhaoxuya520/reverse-skill)
* **作者**: zhaoxuya520
* **功能簡介**: 專為 AI Coding Agent（如 Claude Code、Cursor、Kiro、Cline）設計的逆向工程與資安滲透測試 Skill Router Pack。將 AI 轉化為「白帽駭客」，只需提供專案或系統目標，即可自動化執行漏洞掃描與情境攻擊測試，並生成專業的資安審計報告，大幅降低系統資安體檢成本。

---

### 28. [cangjie-skill (倉頡 Skill)](https://github.com/kangarooking/cangjie-skill)
* **作者**: kangarooking (AI 袋鼠帝)
* **功能簡介**: 認知植入式思維與高價值內容蒸餾引擎。採用七階段 RIA-TV++ 流程，能將書籍、長影片、播客等非結構化知識進行深度提煉與驗證，轉換為 AI Agent（如 Claude Code、Cursor）可直接載入、組合與執行的模組化 AI Skill Packs，實現將海量閱讀內容轉化為可執行行動工具的知識變現。

---

### 29. [OfficeCLI](https://github.com/iOfficeAI/OfficeCLI)
* **專案團隊**: iOfficeAI
* **功能簡介**: 讓 AI Agent（如 Claude Code、Codex、OpenClaw、Hermes 等）能把 Word (.docx)、Excel (.xlsx)、PowerPoint (.pptx) 當成 API 一樣精準操作的開源工具，本機**完全不需要安裝 Microsoft Office**。
  * **API 化文件操作**: 支援讀取分析、精準增刪查改、批次處理、套用模板 Merge、自動重新計算 Excel 公式與樞紐分析 (Pivot)。
  * **「Render → Look → Fix」閉環回饋**: 能直接將產出的 Office 文件渲染成 HTML 或 PNG 圖片，讓具備視覺能力的 Agent 親眼「看到」生成結果，自動檢查是否有文字爆框、重疊或排版異常並自行修正，實現全自動化的辦公文件產出工作流。
  * **多種接入方式**: 原生支援 MCP Server、CLI 終端指令與 SDK 整合。

---

### 30. [AI Office Dollhouse](https://github.com/leavemagic-cyber/ai-office-dollhouse)
* **作者**: leavemagic (leavemagic-cyber)
* **功能簡介**: 專為 Windows 打造的開源 2.5D 像素辦公室視覺化小工具。能將本機端運行的 Codex、Claude Code、Gemini CLI、Grok 等 AI Coding Agents 的即時工作狀態，轉換為一間活靈活現、會動的 2.5D 迷你小辦公室。具備 Local-first 隱私設計，完全不讀取使用者的 Prompts、模型回覆或工具操作內容，支援 MIT 開源免費使用。

---

### 31. [pxpipe](https://github.com/teamchong/pxpipe)
* **開發團隊**: teamchong
* **功能簡介**: 透過「代碼轉圖片」大幅節省 Token 成本的開源代理工具。
  * **核心原理**: 現代多模態模型（如 Claude 3.7 / Opus 5 / Gemini Flash 3.7）在讀取圖片時消耗的 Token 遠小於讀取海量文字代碼。pxpipe 在請求送出前自動將程式碼壓縮渲染為一張高密度圖片再丟給 AI，可省下約 46%~59% 的 Token 費用。
  * **視覺化儀表板**: 內建網頁主控台，可即時查看每筆請求節省的 Token 數量與累積節省的實際美金費用。

---

### 32. [diagram-design](https://github.com/cathrynlavery/diagram-design)
* **作者**: Cathryn Lavery (cathrynlavery)
* **功能簡介**: 專為 Claude Code 與 AI Agent 設計的架構圖與資訊圖表生成技能。
  * **純 HTML + SVG 輸出**: 不需 Webpack 打包、零 JavaScript、無任何外部依賴，生成即可直接在瀏覽器完美渲染。
  * **涵蓋 28 種圖表**: 架構圖、流程圖、時序圖、甘特圖、四象限圖、漏斗圖、雷達圖等，每種皆支援淺色極簡、深色極簡與完整編輯版三種樣式。
  * **嚴格設計規範**: 內建 4 像素網格對齊、最多 10px 圓角、極簡強調色等設計原則，徹底消除 AI 繪圖的粗糙感。

---

### 33. [Agenvoy](https://github.com/agenvoy/agenvoy)
* **作者**: 邱敬幃
* **功能簡介**: 台灣自研的開源 AI Agent Harness 框架。
  * **純 Go 語言單一二進位**: 單一 Go binary 直接自架於本機電腦，效能卓越且開箱即用 28 個工具（檔案處理、Shell 指令、網頁查詢、排程工作等）。
  * **工具動態自擴充**: 缺失工具時能即時自動建立，並透過 MCP 沙箱工具庫共享給 Claude Code、Codex 等其他 Agent。
  * **快照還原與智能路由**: 支援檔案一鍵快照還原，並根據任務複雜度與模型健康狀態自動切換分配後端 LLM。

---

### 34. [Nario AI](https://nario.ai/)
* **開發團隊**: Nario AI
* **功能簡介**: 專為企業內部流程設計的 AI 數位員工 (AI Agent) 服務系統。
  * **無縫串接通訊軟體**: 直接讀取團隊現有的 LINE、Email、Slack 訊息，自動辨識訂單與客服需求。
  * **直連傳統 ERP 自動開單**: 透過專屬資料庫安全通道直連正航、鼎新等使用超過 20 年的傳統老舊 ERP 系統完成自動開單或建檔，完全免除耗時昂貴的 API 串接或資料搬遷。

---

### 35. [AI 資安審查 Agent Skills 精選 (Trail of Bits / Claude Code Security Review)](#-ai-輔助與-agent-相關工具)
* **功能簡介**: 專為 Vibe Coding 與 AI 輔助開發設計的 4 大開源資安稽核套件：
  1. **Trail of Bits Skills ([trailofbits/skills](https://github.com/trailofbits/skills))**: 知名資安團隊 Trail of Bits 官方推出的 Claude Code 技能庫，涵蓋漏洞偵測、靜態程式碼分析 (Static Analysis) 與資安稽核工作流。
  2. **Anthropic Claude Code Security Review ([anthropics/claude-code-security-review](https://github.com/anthropics/claude-code-security-review))**: Anthropic 官方推出的 GitHub Action，在 GitHub PR 發起時自動調用 Claude 深度分析程式碼變更中的安全弱點並留下審查意見。
  3. **Cloudflare Security Audit Skill**: 涵蓋 Recon 偵察 → 漏洞掃描 → 驗證 → 漏洞分級 → 報告產出的完整資安稽核流程。
  4. **GitHub Security Review**: 專注於 PR Code Review，檢查 Prompt/SQL Injection、Secrets 密鑰外洩、Auth 鑑權、依賴漏洞與加密 (Crypto) 等安全風險。

---

### 36. [Claude Code 效率外接三件套 (Graphify / Firecrawl / Gemini Notebook)](#-ai-輔助與-agent-相關工具)
* **功能簡介**: 解決 Claude Code 開發時重複閱讀專案與網頁抓取浪費 Token 的三大利器：
  1. **Graphify**: 將整個專案代碼庫畫成知識地圖/關係圖譜，讓 Claude 查閱地圖導航，免去每次重讀全專案檔案的 Token 消耗。
  2. **Firecrawl**: 將網頁爬蟲資料清洗為乾淨純粹的 Markdown 文字，徹底去除 HTML 標籤與廣告干擾。
  3. **Gemini Notebook (NotebookLM)**: 將大量參考資料餵給 Gemini Notebook 整理成結構化心智圖、報告或摘要影片，供 Claude 直接快速取用。

---

### 37. [Vibe Coding 必備 5 大 Plugins / Skills](#-ai-輔助與-agent-相關工具)
* **功能簡介**: 針對 Claude Code 與 Codex 進行 Vibe Coding 的 5 大核心擴充套件，一次補齊全端開發鏈路：
  1. **Playwright**: 瀏覽器自動化與端到端 (E2E) 測試。
  2. **Supabase**: 資料庫管理、SQL 遷移與後端服務串接。
  3. **Strix**: 程式碼安全掃描與弱點防禦。
  4. **Skill UI**: 前端 UI 元件庫與設計系統自動化。
  5. **Context7**: 即時查詢各大套件庫的最新官方 Documentation，避免 AI 使用過期 API。

---

### 38. [discernment-nudge](https://github.com/anthropics/skills)
* **開發團隊**: Anthropic 官方
* **安裝指令**: `/plugin marketplace add anthropics/skills` 後執行 `/plugin install discernment-nudge@anthropic-agent-skills`
* **功能簡介**: Anthropic 官方 Agent Skills 庫上架的「反思與質疑引導」Skill。當 AI 回答完畢後，會主動在文末附帶 2~3 條針對潛在漏洞、邏輯脆弱處或假設邊界的反問句，方便開發者直接挑選回貼，要求 AI 自我交叉驗證與挑錯，有效防止 AI 幻覺或過度自信。

---

### 39. [Chrome DevTools MCP](https://github.com/ChromeDevTools/chrome-devtools-mcp)
* **開發團隊**: Google Chrome 團隊
* **功能簡介**: Google Chrome 官方出品的 MCP 伺服器，將 Chrome 開發者工具的原生強大能力直接開放給 AI Agent（如 Claude Code 等）：
  * **效能追蹤**: 分析渲染效能瓶頸與卡頓原因。
  * **Network 攔截**: 即時查看與分析 API 請求封包、狀態碼與 Payload。
  * **Console 日誌**: 直接讀取前端報錯日誌與警告。
  * **DOM 操作**: 基於真實 DOM 結構進行分析與修改，非截圖猜測。
  * **Puppeteer 自動化**: 串接 Puppeteer 實現完整的自動化瀏覽與互動測試流程。

---

### 40. [Agent QA](https://github.com/vostride/agent-qa)
* **專案團隊**: Vostride
* **功能簡介**: 以自然語言定義並執行 Web 與行動應用程式的迴歸 QA 工作流，提供 CLI 與 MCP 介面，保留螢幕截圖、DOM、網路及主控台證據，並協助失敗分類。
* **授權與費用**: 目前版本採 FSL-1.1-ALv2 原始碼可用授權；每個版本發布兩年後轉為 Apache-2.0。套件可免費使用，但所設定的模型供應商可能另行收費。

---

### 41. [DeerFlow](https://github.com/bytedance/deer-flow)
* **開發團隊**: 字節跳動 (ByteDance) / BytePlus
* **功能簡介**: 字節跳動開源的超級智慧體運行框架 (SuperAgent Harness)，專為長時間、複雜的多步驟自主任務（如深度研究、代碼編寫、看板生成與複雜報告產出）量身打造。採用 Docker 隔離沙箱環境提供真實的終端機與檔案系統執行能力，內建長期記憶庫、子代理編排 (Sub-Agent Orchestration) 與模組化技能系統，相容任何具備 OpenAI 介面相容之大語言模型。
* **授權**: MIT 開源授權

---

### 42. [WebMCP](https://github.com/ChromeDevTools/devtools-frontend)
* **功能簡介**: 網頁端 AI Agent 互動協議新標準 (Web Model Context Protocol)。解決傳統 Agent 僅能依賴 DOM 爬蟲或截圖猜測操作網頁的痛點，允許網頁前端開發者透過聲明式 API (Declarative HTML Form) 或命令式 API (JavaScript `registerTool()`)，直接向 AI Agent (如 Claude + Chrome DevTools MCP) 暴露標準化結構工具。使同一個網站能同時具備給人類操作的 UI 與給 Agent 直連呼叫的 Tool 介面。

---

### 43. [BitFun](https://github.com/GCWing/BitFun)
* **開發團隊**: GCWing
* **功能簡介**: 基於 Rust 核心與 Tauri v2 打造的開源跨平台桌面 AI Agent 應用 (支援 Windows、macOS 與 Linux)。顛覆純文字對話框限制，當收到任務時能自動為任務生成專屬且具狀態的可操作介面（Mini Apps，如互動圖表、看板、表單與控制面板）。具備 ~98.67% 的極高 KV Cache 命中率與 flashgrep 極速搜尋，支援零知識加密自架中繼伺服器同步與四層深度自訂（Agent、MCP/Skills/Hooks、Mini Apps 至源碼級修改）。

---

### 44. [Archify](https://github.com/tt-a1i/archify)
* **作者 / 團隊**: tt-a1i
* **安裝指令**: `npx skills add tt-a1i/archify -g`
* **功能簡介**: 專為 AI Coding Agent（Claude Code、Cursor、Codex 等）打造的架構視覺化與 Diagrams-as-Code 技能。以數據化 IR (Intermediate Representation) 嚴格校驗架構邏輯，用自然語言即可將專案程式碼結構編譯為美觀、具動態效果、支援深淺色主題切換的獨立互動式 HTML 架構圖、流程圖與序列圖，並支援架構變更對比 (Before/Delta/After Diff) 與高解析度匯出，為傳統 Mermaid 的現代化升級方案。

---

### 45. [Graft](https://github.com/trailhq/Graft)
* **開發團隊**: Trail
* **功能簡介**: 專為 Claude Code 等 Coding Agent 設計的專案脈絡與代碼庫知識地圖層。透過在本地建構持久化的代碼關聯圖譜，讓 Agent 在每次開啟對話時無需重複全盤掃描與重讀專案檔案，大幅降低 Token 消耗達 99% 並提升 3 倍執行速度，使 AI 能夠精準導航於超大型程式庫。

---

### 46. [Orca](https://github.com/stablyai/orca)
* **開發團隊**: Stably AI
* **功能簡介**: 開源的 AI 代理開發環境 (ADE, Agent Development Environment)，專門用於平行管理與調度多個 Coding Agent 艦隊。支援將研究、後端開發、測試撰寫等不同子任務平行分發給多個獨立運行的 Agent，並在統一的儀表板中跨桌面、行動裝置與 VPS 即時監控所有 Agent 的任務執行進度。

---

### 47. [RTK (Rust Token Killer)](https://github.com/rtk-ai/rtk)
* **開發團隊**: rtk-ai
* **安裝指令**: `brew install rtk` 或 `cargo install rtk`
* **功能簡介**: 高效能 Rust 本地 CLI 代理工具，專門攔截並壓縮終端機命令輸出（支援 Git、npm、cargo、pytest、docker、kubectl 等 100+ 種常見開發指令）。透過智慧過濾、分組收納與日誌去重，最高可裁減 60%~90% 的 Bash 終端輸出 Token，有效降低 AI Coding Agent 的上下文讀取負擔與 API 費用。

---

### 48. [CodeGraph](https://github.com/colbymchenry/codegraph)
* **作者**: Colby McHenry (@colbymchenry)
* **安裝與設定**: `npx @colbymchenry/codegraph`（或執行 `codegraph install` 註冊 MCP）
* **授權條款**: MIT License
* **功能簡介**: 專為 AI Coding Agent 打造的本地代碼知識圖譜（Surgical Context）。傳統 Agent 依賴反覆 grep、glob 與 read 逐檔探勘架構，浪費大量 Context 與 API 調用次數；CodeGraph 將專案解析為本地 SQLite 知識圖譜，包含所有符號、函數呼叫關係與相依性網絡。Agent 僅需單次精準查詢即可掌握特定函式全貌與變更影響範圍（Blast Radius），隨專案規模成長其 Token 節省效益呈指數級提升。

---

### 49. [Claudex Loop](https://github.com/chaseai-yt/claudex-loop)
* **作者 / 團隊**: Chase AI (@chaseai-yt)
* **安裝指令**: `npx skills add chaseai-yt/claudex-loop`
* **功能簡介**: 專為 Claude Code 與 Codex CLI 開發的雙模型對抗審查擴充（Loop Engineering Skill）。解決傳統 AI 編程中「單一模型自己批改自己作業」的盲點，採用對抗審查機制：由主模型負責草擬計畫與程式碼，另一個獨立 Frontier 模型（如 Codex）站在反方立場挑錯與交叉辯論。涵蓋四階段 Plan Hardening 工作流（Recon 探勘、Requirements 需求對齊、Plan Review 互審修正、Build & Inspect 構建檢測），在終端機內自主迭代直到完全通過機器測試門檻（Test Gates）為止，實現高可靠度且無需人類反覆干預的自主編程。

---

### 50. [Munder Difflin](https://github.com/chaitanyagiri/munder-difflin)
* **作者**: Chaitanya Giri (@chaitanyagiri)
* **功能簡介**: 本地運行的 Multi-Agent 視覺化調度 Harness（社群暱稱為「AI 人生辦公室」）。將 Claude Code、Codex CLI、Gemini、OpenCode 或本機 Ollama 等多元 CLI Agent 化身為坐於辦公桌前打電腦的虛擬員工，由總協調器（Chief of Staff / Michael）負責解析任務目標、拆解工項、分派合適 Agent 執行並追蹤進度。採用 Local-first 純文字 Git 狀態同步機制與 Markdown 語意記憶層，無需手動切換與管理多個終端機視窗，打造具備遊戲化視覺又兼顧本機隱私的多代理協作環境。

---

### 51. [AI Website Cloner Template](https://github.com/JCodesMore/ai-website-cloner-template)
* **作者 / 團隊**: JCodesMore
* **授權條款**: MIT License
* **使用方式**:
  * Clone 專案：`git clone https://github.com/JCodesMore/ai-website-cloner-template.git`
  * 安裝依賴：`npm install`
  * 配合 Claude Code 執行指令：`/clone-website <target-url>`
* **功能簡介**: 專為 AI Coding Agent 打造的網站逆向工程與克隆模板。只需給予目標網站 URL，即可讓 AI Agent（深度適配 Claude Code + Opus 5，亦支援 Cursor、Codex、OpenCode 等）將任意現有網站重建成架構乾淨、高可維護性的現代 Next.js 應用程式。不同於傳統簡單的靜態 HTML/DOM 抓取，本專案採用完整的工程重構流：包含多模態視覺勘測（截圖比對、響應式斷點與設計令牌分析）、資源萃取，並以 React 19、TypeScript、Tailwind CSS (v4) 與 shadcn/ui 自動編寫元件規格與現代代碼，大幅加速原型開發與前端重構效率。

---

### 52. [desktop-sense](https://github.com/angletech2026-arch/desktop-sense)
* **作者**: angletech2026-arch
* **授權條款**: MIT License
* **功能簡介**: 開源本機端背景常駐程式 (Local Daemon)，專為終端機 AI 程式開發助理（Claude Code、Codex CLI、Gemini CLI）打造，旨在讓 AI 助手能「直接看懂你當前螢幕在做什麼」，免除手動截圖與複製終端錯誤日誌的繁瑣流程。
  * **Prompt 自動附加螢幕上下文 (Live Screen Context)**: 透過命令列工具 Hook 機制（如 Claude Code 的 UserPromptSubmit），在每次發送 Prompt 時自動附帶：當前視窗與應用程式、最近 20 分鐘操作軌跡時間線、可見錯誤訊息及本機最新截圖路徑。
  * **智慧增量傳輸 (極致節省 Token)**: 同輪對話中僅傳送畫面差異變化，首則訊息約耗費數百至 1,500 tokens，後續追問通常低於 200 tokens。
  * **主動式錯誤雷達 (Error Radar)**: 背景即時監測終端機或編輯器中出現的報錯語句（Python Traceback、npm ERR!、error TS...、編譯失敗或重複執行的指令），背景調用輕量模型分析並透過系統桌面通知彈出修復建議。
  * **重複錯誤自動聯網調查 (Auto-research)**: 連續兩次出現相同報錯時，自動前往 GitHub Issues、Stack Overflow、Reddit 等社群抓取類似災情與最佳解法；著手新專案時亦會自動檢索既有開源專案防重複造輪子。
  * **本機隱私與安全機制**: 記錄與文字辨識均在用戶本機執行；具備預設隱私保護（密碼管理器、網銀、無痕視窗預設不記錄），一旦偵測到 API Key 等金鑰截圖也會自動丟棄。
  * **「看著我」串流與控制台支援**: 提供 `ds stream` 即時串流模式配合 Monitor 工具，並提供 `ds` CLI 指令與 `/desk` Skill，隨時按需檢視本機 OCR 辨識文字、畫面截圖與活動歷史。

---

### 53. [browser-use](https://github.com/browser-use/browser-use)
* **開發團隊**: browser-use
* **社群熱度**: ⭐ 30k+ Stars
* **功能簡介**: 開源社群人氣最高、生態最活躍的瀏覽器 AI Agent 框架。
  * **原生 MCP 支援**: 內建 MCP Server，終端 AI 助手無需安裝常駐程式，只需在 Claude / Cursor / Codex 設定中加上 MCP 指令（如 `uvx browser-use`），終端 AI 即可直接獲取標準瀏覽器操作工具（`browser_navigate`、`browser_click`、`browser_screenshot`、`browser_extract_content`）。
  * **精準聚焦與隱私保護**: 截圖操作僅針對網頁視窗本身，完全不會拍到本機桌面的敏感檔案或雜訊，特別適合網頁除錯與瀏覽器工作流自動化。

---

### 54. [Playwright MCP](https://github.com/executeautomation/mcp-playwright)
* **開發團隊**: 微軟 Playwright 標準生態 / ExecuteAutomation
* **功能簡介**: 由微軟官方 Playwright 測試框架延伸的標準 MCP 伺服器生態，專為端到端 (E2E) 自動化測試設計。
  * **工業級測試穩定度**: 具備微軟官方 Playwright 的高度穩定度與跨瀏覽器原生控制力。
  * **深度 Console 與 Network API 攔截**: 能直接監聽瀏覽器主控台日誌 (Console Logs) 與後端網路請求 (Network API，包含 400/500 錯誤與 Payload)。當送出訂單失敗或介面異常時，AI 能直接看到精確的後端回傳錯誤代碼，完全不需要看螢幕截圖猜測。

---

### 55. [Midscene.js](https://github.com/web-infra-dev/midscene)
* **開發團隊**: 字節跳動 (ByteDance / web-infra-dev)
* **社群熱度**: ⭐ 7k+ Stars
* **功能簡介**: 字節跳動開源、專為 UI 測試打造的多模態 AI 自動化測試與視覺檢驗工具。
  * **自然語言撰寫測試**: 支援直接以自然語言撰寫測試腳本（如「點擊開團按鈕」、「檢查購物車商品數量是否為 1」）。
  * **完整視覺對照報告**: 測試執行完成後自動產生完整的視覺化對照報告與檢驗截圖，極度適合在 Next.js / 前端專案建立長期穩定的自動化 UI 驗證工作流。

---

### 56. [Screenpipe](https://github.com/mediar-ai/screenpipe)
* **開發團隊**: mediar-ai
* **社群熱度**: ⭐ 14k+ Stars
* **功能簡介**: 目前開源界最成熟、評價最高的桌面級 AI 記憶與全螢幕感知核心。
  * **Rust 高效能核心**: 採用 Rust 打造，記憶體與 CPU 佔用極低，即使 24/7 背景常駐也不卡頓。
  * **標準介面支援**: 原生提供 REST API 與 MCP Server，跨平台支援 Windows 與 macOS。
  * **全桌面感知與本地 SQLite 索引**: 支援跨應用程式（同時涵蓋 VS Code、終端機、瀏覽器、資料庫 GUI 等）記錄整個螢幕畫面與 OCR 文字，並結構化索引至本地 SQLite，AI 助手可直接透過自然語言查詢「幫我找 10 分鐘前終端機出現的錯誤訊息」。

---

### 57. [M3E Canvas](https://github.com/lnkiai/m3e-canvas)
* **開發團隊**: lnkiai
* **社群熱度**: ⭐ 7k+ Stars (兩週內破 7,000 星標)
* **授權條款**: MIT License
* **功能簡介**: 專為 Material 3 Expressive (M3E) 設計的開源純前端視覺化 UI 畫布。
  * **解決自然語言排版歧義**: 開發者可透過直觀的拖曳操作將按鈕、卡片、導航列等元件排列於畫布上，視覺化規劃空間層級與元件群組。
  * **一鍵產出結構化 Prompt**: 畫布可將排版配置自動編譯為高度結構化的自然語言 Prompt，直接貼入 Claude Code、Cursor、Gemini CLI 等 Coding Agent 即可精準產出語意正確的前端代碼。
  * **零後端純本機架構**: 採 Zero-backend 純前端技術打造，所有資料透過 LocalStorage 儲存於本機端，無伺服器中繼且免登入帳號。

---

### 58. [Everything Claude Code (ECC)](https://github.com/affaan-m/ECC)
* **作者**: Affaan Mustafa (@affaan-m)
* **授權條款**: MIT License
* **功能簡介**: 社群公認最完整、歷時 10 個月精心打造的 Claude Code 生產力設定全集。
  * **模組化工程架構**: 內建完整的專用代理配置 (Agents)、工程級技能庫 (Skills) 與 MCP 伺服器配置範本 (MCP Configs)。
  * **開箱即用頂級環境**: 徹底解決開發者手動調校與設定摸索的繁瑣痛點，一鍵即可將 Claude Code 升級為具備全端開發、架構規劃、代碼審核與自動化測試能力的終端機結對工程師。

---

### 59. [Hindsight](https://github.com/vectorize-io/hindsight)
* **開發團隊**: Vectorize (vectorize-io)
* **社群熱度**: ⭐ 38k+ Stars，GitHub Trending TOP 2
* **授權條款**: MIT License
* **功能簡介**: 專為 AI Agent 打造的「自我進化」長期記憶系統 (Agent Memory That Learns)。
  * **終結重複交代背景**: 基於 Python 打造，徹底解決 AI 助手「每次開啟新對話都要重頭交代背景」的記憶遺忘痛點。
  * **自動化知識提煉**: 在後台自動從 Agent 與使用者的對話歷程、程式碼修改反思與執行回饋中持續提取關鍵知識、偏好與架構決策，使 AI Agent 隨著使用時間不斷進化，越用越聰明。

---

### 60. [Paperclip](https://github.com/paperclipai/paperclip)
* **開發團隊**: Paperclip AI (paperclipai)
* **社群熱度**: ⭐ 87k+ Stars，TypeScript 打造，GitHub 熱門榜 #1
* **授權條款**: MIT License
* **功能簡介**: 專為管理工作場所中 AI 員工團隊設計的開源 Multi-Agent 控制平面 (Control Plane)。
  * **統一代理組織治理**: 能將不同 runtime、不同框架的 AI Agent 納入統一的組織、任務分派與治理架構中。
  * **六大企業級控制維度**: 提供目標拆解 (Goal)、組織架構圖 (Org Chart)、健康心跳監測 (Heartbeat)、算力與 Token 預算控制、關鍵步驟人工審批 (Approval) 以及完整稽核日誌 (Audit Log)，將零散脆弱的單次 AI Session 昇華為具備可觀測性、可恢復性與安全邊界的高可靠企業級自動化團隊。

---

### 61. [mobile-mcp](https://github.com/mobile-next/mobile-mcp)
* **開發團隊**: mobile-next
* **社群熱度**: ⭐ 8.6k+ Stars
* **授權條款**: Apache-2.0 License
* **功能簡介**: 讓 AI Coding Agent（Claude Code、Codex、Gemini CLI）能直接操控 iOS 與 Android 應用程式的開源 MCP 伺服器。
  * **原生無障礙樹定位**: 打破傳統依靠截圖與視覺猜測點擊的耗能模式，直接讀取系統原生無障礙樹 (Accessibility Tree) 獲取精確元件座標，速度極快且大幅節省 Context Token。
  * **全功能自動化操控**: 支援點擊、手勢滑動、鍵盤輸入、安裝 App、即時截圖與錄影，同時相容實體行動裝置與模擬器，開發者無需深入鑽研 XCUITest 或 Espresso，即可讓 AI Agent 自動完成行動端 E2E 測試、自動填表與 App 流程驗證。

---

### 62. [YYLO](https://github.com/yylo-dev/yylo)
* **專案團隊**: yylo-dev
* **授權條款**: MIT License (開源免費)
* **安裝指令**: `npm install --global @yylo/cli@latest`（提供 `yylo` 與 `yy` 命令，或 `ypl` 即時終端代理會話）
* **功能簡介**: 命令列多 AI 編碼代理協調器（CLI Orchestrator for Coding Agents），專為可重複執行的 Agent 工作流程與附帶審計回執（Receipts）的程式庫變更而設計。
  * **Git Worktree 實體環境隔離**: 執行 `task start` 時鎖定受保護的目標 Commit SHA，並為每個 AI 任務自動建立專屬的獨立分支與 `git worktree` 沙箱。徹底根絕多個 Agent 同時修改專案時造成的同檔案異動覆蓋、程式碼競態衝突與 Git `index.lock` 鎖死問題。
  * **型別化驗證與釋出閘門 (Validation & Merge Gates)**: 定義嚴謹的任務生命週期（Task ➔ Validation ➔ Merge ➔ Release-readiness），強制 Agent 編寫的代碼必須在獨立沙箱通過客觀測試驗證後才允許合入主分支。
  * **變更回執與證據鏈 (Receipt-backed Changes)**: 每次變更皆附帶不可竄改的數位回執（Receipts），完整留存修改動機、執行摘要與審計證據。
  * **Git-Native 純文字看板 (YYLO Ledger)**: 任務看板狀態直接以版本化 Markdown 檔案維護於 Git 倉庫內部，免除外部專案管理 SaaS 依賴。
  * **與 herdr 等多 Agent 工具的協同增效**:
    * **分工互補**: `herdr` 負責進程與背景生命週期（守護背景持續運行、電腦休眠不中斷、`herdr agent wait` 非同步等待調度）；`YYLO` 負責檔案系統與狀態隔離（worktree 沙箱、Validation 驗證閘門與 Receipt 回執）。
    * **極致防撞車**: 完美解決在單機背景常駐運行多 Agent（例如前端與後端 Agent 同時作業）時最致命的「骯髒工作目錄 (Dirty Working Tree)」與「同檔案異動污染」痛點。

---

## 💻 大語言模型與本地部署

### 1. [ds4 (Dwarf Star 4)](https://github.com/antirez/ds4)
* **作者**: Salvatore Sanfilippo (antirez, Redis 發明人)
* **功能簡介**: 讓配備 128GB/256GB 記憶體的個人電腦（如 Mac Studio M3 Ultra）能順暢跑起 DeepSeek V4 284b MoE 大模型的本地部署專案。支援 OpenAI 的 Endpoint 標準，於 DGX 上實測可達到 prefill 15 t/s 與輸出 14.8 t/s 的高速度。

---

### 2. [Skywork.ai](https://skywork.ai/) (天工 AI)
* **功能簡介**: 整合了多模態模型與工具（如 Seedance 2.0、VM 版龍蝦與各大通訊軟體串接）的多合一 AI 平台，提供 24 小時在線的 Agent 助理服務，並提供每日免費點數額度。

---

## 📄 文件與資料解析處理工具 (OCR / PDF / 轉檔 / 隱私脫敏)

### 1. [MarkItDown](https://github.com/microsoft/markitdown)
* **開發團隊**: 微軟 (Microsoft)
* **功能簡介**: 一鍵將各種文件格式（PDF、Word、Excel、PPT、HTML、圖片 OCR、音檔語音轉文字）轉換為 AI 看得懂且格式乾淨的 Markdown 格式，能保留標題、清單與表格結構，是建立 RAG 知識庫前進行資料清洗與整理的利器。

---

### 2. [Docling](https://github.com/DS4SD/docling)
* **開發團隊**: IBM
* **功能簡介**: 全地端支援 20+ 種檔案格式解析的開源神器。內建專屬的 **TableFormer** 模型，能完美辨識複雜的合併表格與雙排版排版，將其輸出為帶有標題層級與表格標籤的 Markdown 或 JSON，並原生支援 MCP 協議以供 AI Agent 使用，解決傳統解析工具在 RAG 應用中表格亂碼的痛點。

---

### 3. [Unlimited-OCR](https://github.com/baidu/Unlimited-OCR)
* **開發團隊**: 百度 (Baidu)
* **功能簡介**: 專門為極長 PDF 設計的文檔解析模型。引入了 **R-SWA 機制**（滑動窗口），讓快取大小維持在常數級，避免傳統視覺語言模型在處理長文件時顯卡記憶體（VRAM）暴增與解析變慢的問題，能以極速解析幾十頁的長文檔。

---

### 4. [PDFCraft](https://github.com/PDFCraftTool/pdfcraft)
* **功能簡介**: 主打「絕對隱私」、純前端 WebAssembly 技術運行的開源 PDF 工具箱。內建超過 90 種處理工具（如合併、分割、轉檔、加密、浮水印），所有運算都在使用者瀏覽器本機端完成，保證檔案不外傳。支援拖拽式視覺化工作流以進行批次自動化處理。

---

### 5. [jt-doc-tools](https://github.com/jasoncheng7115/jt-doc-tools)
* **作者**: Jason Cheng
* **功能簡介**: 辦公室文件工具箱。支援批次 PDF 解除密碼功能，並特別為台灣通勤族設計「高鐵模式」，拖入高鐵電子乘車證明 PDF 即可自動解密並重新命名為乘車日期，方便差旅報銷整理。

---

### 6. [anydoc](https://github.com/firecrawl/anydoc)
* **開發團隊**: Firecrawl
* **功能簡介**: 開源的萬能文件轉檔 CLI 工具。能將 PDF、Word、Excel、PowerPoint、EPub、ZIP、HTML 及專案代碼等各式檔案，快速轉成乾淨且結構化的 Markdown 格式，支援本機離線運作與遠端 API 模式。

---

### 7. [EduShield](https://github.com/oas114/EduShield)
* **作者**: oas114
* **功能簡介**: 教育與公務隱私保護系統——零信任架構的去識別化與還原工具。採用純靜態單一 HTML 設計，所有資料運算皆在瀏覽器本機端完成，確保公文、學生或機密資料完全不落地。在將資料交給外部 AI 分析前，先自動去識別化姓名、電話、身分證等敏感個資，處理完畢後可於本地一鍵無損還原。

---

### 8. [Microsoft Presidio](https://github.com/microsoft/presidio)
* **開發團隊**: 微軟 (Microsoft)
* **功能簡介**: 微軟開源的敏感個人資料 (PII) 自動識別與去識別化防禦引擎。結合 NLP/NER 實體辨識模型與正規表示式雙引擎，精準辨識上下文中的真實姓名、地址、電話、身分證與信用卡等個資；支援字元遮罩 (Masking)、雜湊加密 (Hashing)、假資料替換 (Redact) 及部分保留等多種脫敏策略。提供 Python SDK、REST API 與 Docker 容器，是構建 LLM / RAG 資料前置清洗防線的標準利器。

---

### 9. [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)
* **開發團隊**: 百度飛槳 (PaddlePaddle)
* **社群熱度**: ⭐ 90k+ Stars
* **授權條款**: Apache-2.0 License
* **功能簡介**: 工業級開源多模態光學字元辨識 (OCR) 工具包，專門用於將複雜 PDF 文件、掃描報告與各式圖片轉化為大語言模型 (LLM) 易於讀取的結構化 JSON 與 Markdown 格式。
  * **輕量級端到端模型**: 內建輕量級 PaddleOCR-VL-1.6 (0.9B) 視覺語言模型與 PP-OCRv6，兼具高辨識率與極速推論。
  * **50+ 種跨語言支援**: 原生支援繁中、簡中、英、日以及 46 種拉丁語系語言（總計 50 種語言），在處理跨國、多語系文件時完全不需頻繁切換模型，精準萃取文字內容、表格結構與排版資訊。

---

## 🌐 網路爬蟲與資料擷取

### 1. [Crawl4AI](https://github.com/unclecode/crawl4ai)
* **功能簡介**: 專門為大型語言模型 (LLM) 與 AI Agent 量身打造的開源非同步網頁爬蟲。速度極快，能輸出乾淨且具備語意結構的 Markdown 內容，支援執行 JavaScript、處理動態載入頁面、模擬使用者操作以及抽取結構化 JSON 資料。

---

### 2. [Camofox](https://github.com/daijro/camoufox)
* **功能簡介**: 基於 Firefox 核心改造的開源匿蹤防爬瀏覽器。專門針對反爬蟲偵測機制（如 Cloudflare Turnstile、Akamai 等）進行硬體指紋偽裝與行為模擬，可大幅降低自動化爬蟲被阻擋的機率。

---

## ⚡ 實用與效能優化工具

### 1. [Winhance](https://github.com/memstechtips/Winhance)
* **功能簡介**: Windows 11 系統最佳化與瘦身工具。提供直觀圖形化介面，可一鍵關閉微軟遙測追蹤、禁用廣告、移除內建臃腫軟體 (Bloatware)、關閉 Copilot 與 Recall 等背景 AI 服務，並提升系統隱私與遊戲運行效能。

---

### 2. [NetCheckMonitor](https://ahui3c.com/159828/netcheckmonitor)
* **作者**: 3C 達人 廖阿輝 (ahui3c)
* **功能簡介**: 網路連線狀態即時監控小工具。專門用於家中或公司網路不穩定時自動監控連線並記錄斷線日誌，方便後續向電信業者報修。支援即時產出 PDF 統計報表與 CSV 明細，並具備每日自動上傳備份至 Google Drive 的功能。

---

### 3. [DesktopOK](https://www.softwareok.com/?seite=Freeware/DesktopOK)
* **功能簡介**: 解決 Windows 桌面圖示排列紊亂問題的經典實用工具。能精確儲存與一鍵還原桌面圖示的位置與佈局，防止因變更螢幕解析度、更換多螢幕或重開機時圖示位置跑位。

---

### 4. [openings-mcp](https://github.com/amikai/openings-mcp)
* **作者**: amikaiii
* **功能簡介**: 支援多國平台與企業的開源職缺搜尋 MCP 工具。讓 AI Agent 能直接檢索 LinkedIn、Indeed、台灣（104、Cake.me）、日本、丹麥（Jobindex）以及 TSMC、Apple、Google、Amazon、Meta、NVIDIA 等 10,000+ 家科技巨頭與企業的最新職缺。

---

### 5. [Career-Ops](https://github.com/santifer/career-ops)
* **功能簡介**: 用 AI 反向篩選職缺的求職神器。能在本地掃描招聘平台並根據用戶自定義的 10 個維度對職缺進行 A-F 精準打分，篩選出高品質工作，並自動生成針對該 Job Description (JD) 優化的專屬 PDF 履歷以通過企業的 ATS 系統篩選。

---

### 6. [remove-ai-watermarks](https://github.com/wiltodelta/remove-ai-watermarks)
* **功能簡介**: 去除 AI 隱藏浮水印與中介數據（如 C2PA 協議、Google SynthID 等）的工具，實測在拿掉 C2PA 時能完全不損畫質，適合用來清理 AI 產圖的追蹤浮水印。

---

### 7. [jt-gelflow](https://github.com/jasoncheng7115/jt-gelflow)
* **作者**: Jason Cheng
* **功能簡介**: 網路流量即時監控視覺化工具。接收 Graylog 資料流，在前端以動態流量圖、2D地圖、3D地球以及最新版本加入的「桑基圖 (Sankey)」呈現，讓 IT 管理者能對公司的網路流量去向一目了然。

---

### 8. [IPTV](https://github.com/iptv-org/iptv) (7 大爆紅 Skill 之一)
* **功能簡介**: 全球免費網路電視頻道的超級懶人包。由社群驅動，收集世界各地公開免費播放的直播串流連結，並整理為標準的 M3U 播放清單，方便使用者直接匯入各種播放器中免費收看全球電視。

---

### 9. [AI Quota Deck](https://github.com/JoshuaWang2211/ai-quota-deck)
* **作者**: Joshua Wang (JoshuaWang2211)
* **功能簡介**: Windows 系統匣與工作列的 AI 用量額度監控儀表板。可同時即時追蹤 Claude Code、Codex、Gemini 與 Grok 的 Session 與週期使用配額，支援多種顯示模式並能直接鎖定於 Windows 工作列左側空白處。同時提供專屬 Chrome 瀏覽器擴充功能。

---

### 10. [Public APIs](https://github.com/public-apis/public-apis)
* **功能簡介**: GitHub 上超過 46 萬星標的免費公開 API 超級懶人包。收錄超過 1,000+ 個真正免費的 Public API（涵蓋天氣、金融股票、加密貨幣、AI、地圖圖資、各類公用資訊等），詳細標註鑑權方式 (Auth)、HTTPS 支援與 CORS 狀態，開箱複製貼上即可在各類專案中調用。

---

### 11. [just-a-launcher](https://github.com/hungmi/just-a-launcher)
* **作者**: hungmi (gn01189425)
* **功能簡介**: 專為 Android TV / Google TV 投影機與電視設計的超極簡 Launcher 桌面。徹底解決內建 Google TV 系統因廣告輪播與聚焦動畫導致 CPU 常駐飆破 80%+、RAM 吃緊及劇烈卡頓的痛點；去除所有動態效果、推薦列與常駐服務，將 CPU 佔用壓至近 0%、常駐 RAM 僅約 35MB。讓 2GB 記憶體設備也能秒切 Netflix、YouTube 與巴哈姆特動畫瘋不被系統殺掉後台，並提供一鍵 ADB 腳本與 Agent 自動安裝支援。
* **安裝方式**: 透過 ADB 腳本一鍵安裝 `curl -LO https://github.com/hungmi/just-a-launcher/releases/latest/download/install.sh && bash install.sh`，或至 Releases 下載 APK 手動安裝。
* **授權協議**: MIT License

---

### 12. [Tusk](https://github.com/alpcanaydin/tusk)
* **作者**: Alpcan Aydın (@alpcanaydin)
* **授權條款**: MIT License
* **功能簡介**: 專為 macOS 打造的高效能原生鍵盤驅動資料庫客戶端。
  * **支援 20+ 種資料庫**: 支援連接 PostgreSQL、MySQL、SQLite、Redis、MongoDB 等 20 種常見資料庫。
  * **內建安全 AI 助手**: 搭載本機 AI 查詢助手，僅協助起草 SQL 查詢語句，絕不擅自執行任何操作，完全由使用者掌控確認。
  * **極致隱私保護**: 全程本機運作、無須註冊帳號、絕不回傳連線密鑰或資料庫內容，完全免費且開源，終結商業工具高昂的訂閱費用。

---

## 📈 金融、交易與生活助手

### 1. [Fincept Terminal](https://github.com/Fincept-Corporation/FinceptTerminal)
* **功能簡介**: 開源版的金融研究工作站（Bloomberg Terminal 替代方案）。整合了股票、總體經濟、新聞、加密貨幣等金融資料，並內建 AI Agent 來協助研究與摘要，專案使用 C++20、Qt6 與 Python 開發，在 GitHub 上已獲 23k+ 星標。

---

### 2. [Vibe-Trading](https://github.com/HKUDS/Vibe-Trading)
* **開發團隊**: HKUDS
* **功能簡介**: 個人交易 AI Agent 工作台。具備六大核心能力：自然語言交易研究、自動策略生成與回測、多格式程式碼輸出（TradingView Pine Script / MT5 等）、多 Agent 協作（研究、策略、風控）、交易紀錄行為模式診斷，以及能回放真實交易以量化交易紀律的 **Shadow Account** 影子帳戶功能。

---

### 3. [財伴 oSave](https://www.finctory.com/)
* **開發團隊**: finctory
* **功能簡介**: 結合 AI 輔助的存錢與理財記帳助手 App。支援 iOS 與 Android 雙平台，主打精準記帳、資產與財務分析，並提供個性化的儲蓄計畫與投資本金累積建議。

---

### 4. [HealthWorkbench](https://github.com/notoriouslab/health-workbench)
* **開發團隊**: NotoriousLab
* **功能簡介**: 免費開源的個人與家庭健康資料工作台桌面 App (支援 macOS 與 Windows)。解決健保「健康存摺」僅保留近三年紀錄以及 Apple 健康匯出檔龐大難讀的痛點；支援直接拖入健保存摺下載檔、Apple 健康匯出檔與睡眠呼吸器 SD 卡資料，自動解析格式、去除重複並建立跨越三年的完整終身健康紀錄。提供就醫時間軸、用藥清單（附成分與仿單連結）、檢驗趨勢圖與呼吸器 AHI 整合圖表。全程本機運作不上雲、無帳號、無追蹤，並支援一鍵匯出單檔 HTML 或 EPUB 方便回診時與醫師討論。

---

### 5. [Capafy (Alpha Consensus)](https://capafy.ai/)
* **開發團隊**: Capafy AI
* **功能簡介**: 結合 AI Skills 市場機制的金融市場洞察與交易情報平台。
  * **Alpha Consensus 核心技能**: 專門追蹤與聚合 X (Twitter) 等社群網路上頂尖交易員、機構與分析師的投資言論、消息發布與資金流向。
  * **多空共識看板 (Consensus Dashboard)**: 自動產生「市場共識看板」（如 DJT Radar），將散亂的股票討論結構化標記為看多或看空理由，並深度交叉比對消息發布前後的股價走勢，協助投資者洞察市場主線與機構資金預期。

---

## 🎬 影音與串流工具

### 1. [Invidious](https://github.com/iv-org/invidious)
* **功能簡介**: 100% 開源且保護隱私的 YouTube 替代前端。完全無廣告、支援行動裝置背景播放音訊、免登入 Google 帳號即可訂閱與觀看、無廣告追蹤像素。載入速度極快，可一鍵匯入 YouTube 訂閱頻道，並能搭配 Privacy Redirect 擴充套件自動重新導向。

---

### 2. [StreameX](https://streamex.ws/)
* **功能簡介**: 開源的跨平台影視影音串流瀏覽與播放應用。具備現代化 UI 介面，支援搜尋電影、電視影集 (TV Shows)、熱門榜單瀏覽與流暢串流播放體驗。

---

### 3. [分鏡快拆 (Story Cut) 與 GridyClip](https://gridyclip.com)
* **作者**: 異鄉人經紀小葉 (ayeh821) / 嚴曇 (GridyClip)
* **功能簡介**: 專為影像導演、剪接師與行銷過稿設計的影片分鏡自動拆解工具。只需將影片拖入網頁，即可自動偵測畫面切點完成分鏡拆解，支援時間軸微調、每格鏡頭備註分析，並可一鍵輸出分鏡大圖、Excel、PDF 或打包下載所有高清截圖。影片全程於本機瀏覽器內運算不需上傳伺服器，確保未公開影音素材的商業機密。

---

### 4. [video-autopilot-kit](https://github.com/Hao0321/video-autopilot-kit)
* **作者**: Hao0321 (HAO0321 Studio)
* **功能簡介**: 台灣創作者開源的 YouTube / 短影音自動化剪輯框架。結合剪映 (CapCut) JSON 軌道數據處理與 ffmpeg 工具鏈，讓創作者只需填入結構化資料（文案、素材路徑），即可全自動化批量產出短影音，作者持續每週維護更新。

---

### 5. [JojoNowhere AI Edit Kit](https://github.com/jojonowhere/jojonowhere-ai-edit-kit)
* **作者**: Jojo (揪揪漫遊 / JojoNowhere)
* **功能簡介**: 用 Claude 打造 AI 影片自動剪輯工作流程的實況開源資源包。提供一鍵 `bash setup.sh` 安裝環境，整合了 git、uv、node、ffmpeg、video-use 剪輯引擎、思源黑體 TW 繁體字幕字體、watch@claude-video 外掛以及 ElevenLabs API 逐字稿語音轉寫，是探索 AI 輔助短影音後製的絕佳起點。

---

### 6. [Remotion](https://github.com/remotion-dev/remotion)
* **開發團隊**: Remotion
* **安裝指令**: `npm init video` 或 `npx create-video`
* **功能簡介**: 以 React 程式碼驅動的現代化影片製作與動畫開發框架。將影片時間軸、動態視覺與畫面場景完全拆解為可高度重用的 React 元件，支援使用 CSS / Canvas / SVG 進行精確到影格 (Frame-by-Frame) 的排版與運鏡。支援透過程式碼動態傳入參數批次渲染大量個人化影片，是將 AI 生成內容與影片自動化流程無縫結合的核心利器。

---

### 7. [OpenMontage](https://github.com/calesthio/OpenMontage)
* **開發團隊**: Calesthio
* **功能簡介**: 首個端到端開源的 Agentic 影音製作系統，將 Claude Code、Cursor 等 Coding Agent 直接轉化為具備全流程製作能力的影片工作室。內建 12 種專業製作 Pipeline（包含動畫解說、紀錄短片、電影級預告片與產品廣告）及 50+ 種工具（整合 FFmpeg 與 Remotion），Agent 能自主完成選題研究、腳本撰寫、素材生成、剪輯組合到最終渲染。

---

### 8. [ChatCut](https://chatcut.io/)
* **功能簡介**: 自然語言對話驅動的 AI 影片剪輯應用。只需將影片檔案拖入並以口語化指令對話，AI 即能自動分析影音內容完成修除贅詞口誤、精準對齊字幕、添加轉場與動畫特效；更支援將文字研究報告、PDF 或 Excel 數據一鍵自動生成為流暢的動畫短影音，同時保留多軌時間軸供創作者後續手動細調。

---

## 🔄 工作流自動化

### 1. [n8n](https://github.com/n8n-io/n8n)
* **功能簡介**: 強大的節點式工作流自動化工具。學習歷程涵蓋 Trigger 觸發器、Gmail / Google Sheets 串接、RAG AI 機器人、MCP 協議結合以及將 n8n 作為輕量化網站後端等應用。在 Agent 時代，配合 n8n 跑固定流程是極具性價比（省 Token 與高穩定度）的自動化方案。

---

## 📚 AI 學習資源、電子書與認證指南

### 1. [深入理解 AI Agent：設計原理與工程實踐](https://github.com/bojieli/ai-agent-book)
* **作者**: 李博傑 (bojieli) 等
* **功能簡介**: 免費開源的 AI Agent 完整電子書。以「Agent = LLM + 上下文 + 工具」為核心架構，全書共 10 章並附帶 92 個配套實驗（其中 70+ 個可獨立執行）。支援正體中文、簡體中文、英文等 7 種語言，並提供 PDF/EPUB 離線下載與線上閱讀。

---

### 2. 科技巨頭免費 AI 認證路徑指南
* **彙整內容**: 履歷上具備鑑別度的四大科技巨頭免費 AI 認證方案：
  * **Microsoft Applied Skills**: 全程免費，1-2 小時實作考，開書不監考且證書不失效。
  * **Google Cloud Skills Boost / Innovators**: 免費參與 Google Cloud Innovators 每月贈送 35 點 credits，可用於完成計時實作 Lab 技能徽章。
  * **AWS Skill Builder**: 提供 600+ 門免費課程與數位徽章。
  * **IBM SkillsBuild**: AI Fundamentals 等基礎課程與 Credly 官方數位認證徽章全免費。

---

### 3. AI 策展實證線上課程案例
* **案例分享**: 林協霆
* **功能簡介**: 示範如何運用 AI 結合 YouTube 高讚影片與醫學實證資料庫（PubMed、OpenEvidence），以常見線上課程的 UX/UI 框架與 iframe 嵌入，快速低成本策展出一套高品質、附帶收錄理由與實證依據的免費健身線上課程。

---

### 4. [awesome-agentic-ai-zh](https://github.com/WenyuChiou/awesome-agentic-ai-zh)
* **作者**: Wenyu Chiou
* **功能簡介**: 台灣開發者整理的開源 Agentic AI 結構化學習地圖。不同於一般無序的資源列表，本專案將 240+ 個 AI 專案、77+ 個 MCP / Skills 與 23 個實作案例，結構化整理為 8 大學習階段，並明確拆分出兩條清晰路徑：
  * **路線 A：CLI Power User (8-10 週)**：著重於將現成 Agent CLI（Claude Code、Codex、Gemini CLI 等）與 Skills 運用到極致。
  * **路線 B：Agent Builder (16-22 週)**：從 LLM 原理、Prompt、Tool Use 一路深入到 RAG、Memory、MCP、Multi-Agent 編排與 Computer Use，引導開發者親手打造專屬 Agent 系統。
