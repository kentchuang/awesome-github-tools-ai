# 🛠️ Awesome GitHub Tools & AI Catalog

歡迎來到 **awesome-github-tools-ai**！本專案致力於精選並收錄高生產力、極具實用價值的 **GitHub 開源工具、AI Agent 代理應用、MCP 伺服器、Token 節省神器與精選學習資源**。

為了滿足不同閱讀場景的需求，本專案提供 **純文字極速版** 與 **含截圖視覺版** 雙目錄架構，並將所有圖片統一收納於 `images/` 目錄中，維持專案結構嚴謹整潔。

---

## 📖 目錄版本選擇

| 目錄版本 | 特色說明 | 快速連結 |
| :--- | :--- | :--- |
| 📄 **純文字快速目錄** | 適合終端機、低頻寬或快速查找文字與安裝指令 | 👉 **[GitHub_實用工具與AI應用目錄.md](./GitHub_實用工具與AI應用目錄.md)** |
| 🖼️ **含截圖預覽目錄** | 包含每款工具的 UI 截圖、操作流程圖與實測範例 | 👉 **[GitHub_實用工具與AI應用目錄_含截圖預覽.md](./GitHub_實用工具與AI應用目錄_含截圖預覽.md)** |

---

## 💡 涵蓋主題分類索引 (收錄 100+ 精選工具)

1. **🤖 AI 輔助與 Agent 相關工具**
   * **本機 Agent & 桌面操作與螢幕感知**：desktop-sense (本機背景常駐程式、Live Screen Context 與錯誤雷達)、Screenpipe (Rust 打造 24/7 桌面 AI 記憶與 OCR 結構化檢索)、DeerFlow (字節跳動超級智慧體運行框架)、BitFun (桌面 Mini Apps 智慧體)、Hermes AI Agent、OpenWorker (吳恩達團隊)、Munder Difflin (AI 人生辦公室多 Agent 視覺化調度)、AI Office Dollhouse (2.5D 像素辦公室)、OfficeCLI (免裝 Office API 操作)、HermesOffice。
   * **多 Agent 編排、治理與背景執行**：YYLO (Git Worktree 實體環境隔離與回執協調器，可搭配 herdr 背景防衝撞)、Paperclip (87k+ Stars 開源 Multi-Agent 控制平面與企業治理架構)、Orca (Agent 開發環境與艦隊平行管理)、AWS Kiro Crew (3.9 萬人使用)、herdr (多 Agent 協同閉環)、Agenvoy (台灣自研純 Go 單一 Binary Harness)、Nario AI (直連傳統 ERP)。
   * **Token 極致節省、脈絡地圖與長期記憶**：Hindsight (38k+ Stars 自我進化長期記憶系統)、RTK (Rust Token Killer，終端輸出壓縮 90%)、CodeGraph (本地代碼知識圖譜與精準脈絡)、Graft (Claude Code 專案知識圖譜與導航)、Caveman (山頂洞人輸出壓縮)、Headroom (輸入上下文可逆壓縮)、pxpipe (程式碼轉圖片省 50% Token)。
   * **開發工程、環境設定與視覺化**：M3E Canvas (7k+ Stars Material 3 純前端畫布，一鍵轉結構化 Prompt 給 Coding Agent)、Everything Claude Code (ECC，10 個月打造全套 Agents/Skills/MCP 設定)、AI Website Cloner Template (給 URL 一鍵讓 AI 重構 Next.js 現代網站)、Archify (AI 架構圖生成與 Diagrams-as-Code)、github/spec-kit (規格驅動 SDD)、mattpocock/skills (需求訪談/問卷/TDD)、Claude Code 知識三件套 (Graphify / Firecrawl / Gemini Notebook)、Vibe Coding 必備 5 大外掛。
   * **程式碼與安全審查**：Claudex Loop (雙模型對抗審查與自主循環)、Trail of Bits 官方安全 Skills、Anthropic Claude Code Security Review、阿里 open-code-review、OpenAI codex-plugin-cc、reverse-skill 白帽滲透測試、SkillSpector (NVIDIA 技能安全掃描器)、Agent QA (自然語言 Web/Mobile 迴歸測試與 MCP)。
   * **Web 標準、瀏覽器/行動端 Agent 與測試**：mobile-mcp (8.6k Stars 讀無障礙樹直接操控 iOS/Android 裝置與 App 測試)、browser-use (30k+ Stars 瀏覽器 AI Agent 框架與原生 MCP)、Playwright MCP (微軟官方測試協議生態、Console/Network 深度監聽)、Midscene.js (字節跳動開源自然語言 UI 測試與視覺化報告)、WebMCP (網頁端 AI Agent 互動標準)、Chrome DevTools MCP (Google 官方開發者工具 MCP)、Webwright (微軟瀏覽器自動化)、Index (Laminar 瀏覽器 Agent)、Ego-lite (人機協同瀏覽器)、Multi-AI-Chat-Desktop、linebot-multimodal-rag、rag-anything MCP、說人話 speak-human-tw、cangjie-skill。

2. **💻 大語言模型與本地部署**
   * ds4 (antirez 打造，在 Mac 上跑 DeepSeek V4 284b MoE)、天工 AI (Skywork.ai)。

3. **📄 文件與資料解析處理工具 (OCR / PDF / 轉檔 / 隱私脫敏)**
   * 百度飛槳 PaddleOCR (90k+ Stars 工業級多模態 OCR 與 50+ 語言文件轉 Markdown/JSON)、微軟 MarkItDown、IBM Docling (TableFormer 表格解析)、百度 Unlimited-OCR (極長 PDF 滑動窗口)、PDFCraft (純前端 WebAssembly)、anydoc (Firecrawl 萬能轉檔)、jt-doc-tools (高鐵解密模式)、EduShield (教育零信任脫敏還原)、微軟 Presidio (PII 敏感個資識別與脫敏引擎)。

4. **🌐 網路爬蟲與資料擷取**
   * Crawl4AI (LLM 專用非同步爬蟲)、Camofox (Firefox 匿蹤防爬瀏覽器)。

5. **⚡ 實用與效能優化工具**
   * Tusk (macOS 原生鍵盤驅動資料庫客戶端，支援 20+ 資料庫與本地安全 AI)、Winhance (Win11 瘦身優化)、NetCheckMonitor (阿輝 3C 網路連線監控)、DesktopOK (桌面圖示佈局備份)、Career-Ops (AI 反向篩選職缺與 ATS 履歷)、openings-mcp (萬家科技企業職缺搜尋)、AI Quota Deck (多 AI 額度工作列監控)、Public APIs (1000+ 免費 API 寶庫)、just-a-launcher (Google TV 超極簡桌面，CPU 降至近 0%、常駐 RAM 僅 35MB 拯救卡頓電視)、remove-ai-watermarks (去除 C2PA/SynthID 浮水印)、jt-gelflow (流量桑基圖視覺化)、IPTV 全球電視。

6. **📈 金融、交易與生活助手**
   * Capafy (Alpha Consensus 交易員言論與市場多空情緒看板)、Fincept Terminal (開源彭博終端)、Vibe-Trading (交易 Agent 與影子帳戶)、財伴 oSave (AI 記帳助手)、HealthWorkbench (個人與家庭健康存摺工作台)。

7. **🎬 影音與串流工具**
   * Invidious (無廣告隱私 YouTube 前端)、StreameX (開源跨平台串流)、Remotion (React 程式化影片開發框架)、OpenMontage (端到端 Agent 影音製作工作室)、ChatCut (對話式 AI 影片剪輯)、分鏡快拆 (Story Cut / GridyClip 影片自動拆分鏡)、video-autopilot-kit (CapCut JSON + ffmpeg 自動剪片)、JojoNowhere AI Edit Kit (Claude 剪片工作流資源包)。

8. **🔄 工作流自動化**
   * n8n (開源節點式自動化與 AI Agent 串接)。

9. **📚 AI 學習資源、電子書與認證指南**
   * 《深入理解 AI Agent》開源電子書、awesome-agentic-ai-zh (台灣開發者 Agent 學習地圖)、四大科技巨頭 (MS/Google/AWS/IBM) 免費 AI 認證指南、AI 策展健身線上課程案例。

---

*本專案持續更新中，由 [kentchuang](https://github.com/kentchuang) 整理維護。歡迎提 Issue 或 PR 推薦更多好用的開源工具！*
