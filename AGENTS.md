# Momobear_crochet 專案行為準則 (AGENTS.md)

本檔案為此專案（Momobear_crochet 毛線手作社群內容與 AI 視覺工作台）的專屬開發與行為準則，補充全域準則。

---

## 1. 專案概述與架構

- **專案名稱**：Momobear_crochet 社群工作台 (my-studio)
- **遠端倉庫**：`jackwxhuang093/my-studio` (GitHub)
- **主要檔案結構**：
  - `index.html`：單檔案整合式 Web 應用程式（含前端 UI、樣式、貼文生成引擎、Canvas 即時疊字與 OpenRouter / Gemini AI 生圖整合）。
  - `品牌規格.md`：Momobear_crochet 品牌風格手冊、各平台篇幅與禁忌清單。
  - `品牌卡.md`：品牌核心價值與識別設定。
  - `0_學生任務單.html`：實作與教學練習指引。
- **技術棧**：原生 HTML5、CSS3、Vanilla JavaScript（無外部打包依賴，強調輕量、零建置成本）。

---

## 2. 影像與 AI 視覺工作坊規範

1. **雙模式架構**：
   - **⚡ 快速推薦風格 (Quick Mode)**：提供高頻優選場景（日系午後窗光、簡約純淨棉麻、溫潤職人工作桌、北歐針織家居沙發），供快速一鍵出圖。
   - **🎨 自由客製工坊 (Custom Studio)**：支援提示詞積木（Prompt Chips）、自由新增自訂標籤、多張輪播分張微調頁籤（Per-Image Controls）與即時雙向提示詞編輯器（`#imagePromptInput`）。
2. **生圖提示詞防護底線**：
   - **外觀鎖定**：嚴格保持產品本體針目紋理、織法細節與立體造型。
   - **構圖規範**：主體完整置於畫面中央 75% 正方形安全區，四周預留 20%~25% 緩衝留白，以兼顧 FB/LINE 1:1 與 IG 4:5 跨平台適配。
   - **商業特寫限制**：單一鏡頭特寫滿版攝影，背景柔焦景深，嚴禁多格照片分割或九宮格拼貼。

---

## 3. 品牌調性守則（文字與文案生成）

- 依循 [`品牌規格.md`](file:///d:/Antigravity/毛線社群平台/品牌規格.md)：
  - **稱呼原則**：一律使用親切溫暖的「你」，不用「您」或「親愛的」。
  - **標點限制**：一篇貼文最多使用 1 個驚嘆號（！），嚴禁連續驚嘆號（！！！）。
  - **精神句收尾**：「一針一線，織進溫暖與日常。」
  - **紅線詞禁絕**：不得出現網美浮誇詞（爆表、美哭、此生必收）或促銷賤價詞（CP值超高、破盤價、超划算）。

---

## 4. Git 與推送流程 (Git Workflow)

1. **檔案 Stage 規則**：
   - 嚴禁執行無差別 `git add .` 或 `git add -A`。
   - 僅允許明確指定檔案：`git add <specific_file>`。
2. **Commit 訊息格式**：
   - 必須遵循 Conventional Commits 格式，訊息使用 English，例如：
     - `feat(images): add dual-mode prompt studio for image beautification`
     - `docs(agents): add project-level AGENTS.md guidelines`
3. **推送規則**：
   - 推送至遠端 GitHub 儲存庫：`git push origin main`。
   - 推送前確認 `git status` 與 `git diff`，絕不將 `.env`、API Key 或任何敏感金鑰推送至 Git。
