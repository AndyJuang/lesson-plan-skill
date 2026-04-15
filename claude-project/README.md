# 教案生成 Skill — Claude Project 版本

> 給**沒有安裝 Claude Code**、只用 **claude.ai 網頁版**的老師使用。
> 把本 Skill 打包成一個 Claude Project，邀請多位老師共用一套教案生成能力。

---

## 🎯 為什麼要用 Claude Project 版本？

| 情境 | 適用版本 |
|---|---|
| 老師會用終端機、想自己寫 Skill | ✅ Claude Code 版（主 repo） |
| 老師只會用瀏覽器、要最低門檻 | ✅ **Claude Project 版（本資料夾）** |
| 多位老師要共用、但不想每人安裝 | ✅ **Claude Project 版** |
| 需要把產出自動寫入本機檔案 | ❌ 必用 Claude Code 版 |

**一句話**：Claude Project 版適合把 Skill「分享給整個學年團隊」，所有人開同一個 Project，內容統一、升級統一。

---

## ⚙️ 5 分鐘設定流程（由 Project 擁有者操作）

### Step 1. 建立 Claude Project

1. 登入 [claude.ai](https://claude.ai)（需要付費方案才能建 Project，免費方案老師請看下方「免費替代方案」）。
2. 左側選單點 **「Projects」→「Create project」**。
3. 命名：`教案生成-東澳國小` 或 `AI 備課助手`。

### Step 2. 貼入自訂指令（系統提示詞）

1. 在 Project 設定頁找到 **「Custom instructions」** 區塊。
2. 打開本資料夾的 [`system-prompt.md`](system-prompt.md)。
3. **複製該檔「---SYSTEM PROMPT START---」與「---SYSTEM PROMPT END---」之間的全部內容**。
4. 貼進 Custom instructions 輸入框 → 儲存。

### Step 3. 上傳 Project Knowledge

1. 在 Project 頁面找到 **「Project knowledge」** 區塊。
2. 依 [`upload-checklist.md`](upload-checklist.md) 依序上傳 6 份範本檔案。
3. 每份檔案上傳後，Claude 就能「讀得到」這些範本。

### Step 4. 邀請老師加入

1. Project 頁面右上角 **「Share」**。
2. 輸入老師的 Anthropic 帳號 email（需已註冊 claude.ai）。
3. 選擇權限：**Editor**（可對話、可修改 Project）或 **Viewer**（只可對話）。
4. 建議：學年主任給 **Editor**，其他老師給 **Viewer**。

### Step 5. 測試：跑一份示範教案

在 Project 聊天室輸入：

```
我要做一份教材。

來源資料：我等一下會把課本單字表貼上來。
授課需求：
  - 學科：英語
  - 單元：Animals（動物）
  - 年級：三年級 / CEFR Pre-A1
  - 時長：40 分鐘
  - 文化錨點：泰雅雲豹傳說
  - 特殊要求：雙語對照
```

然後把單字表貼進下一則訊息。Claude 會依 5 階段流程產出 7 份內容，老師複製貼到自己的 Google Drive 即可。

---

## 💡 免費方案替代：Custom GPTs 式的「專案對話」

若老師沒有 Claude 付費方案、無法建 Project，可以用以下兩種替代：

### 替代 A：單次對話 + 上傳檔案

1. 老師開啟 claude.ai 新對話。
2. 把 `system-prompt.md` 的內容（去除開頭標記）**貼在對話第一則**。
3. 把 6 份範本檔案**一次性上傳**（點「附件」）。
4. 第二則訊息開始下單——體驗跟 Project 版差不多，只是每次要重新上傳。

### 替代 B：用 ChatGPT Custom GPT

若老師熟悉 ChatGPT：建立一個 Custom GPT，把 `system-prompt.md` 當 Instructions，6 份範本上傳到 Knowledge。成果與 Claude Project 版近乎相同。

---

## 🎓 教學使用建議

### 給個別老師用

1. 每位老師都建一個自己的 Claude Project（如上 Step 1–3），完全獨立。
2. 適合習慣獨自備課、風格強烈的老師。

### 給學年／科任共用

1. 學年主任建一個 Project，邀請同學年老師當 Viewer。
2. 每位老師在同一 Project 內下不同單元指令，產出會存在各自對話串。
3. 遇到共通問題，可在 Project 內公開討論。

### 給師培講師用

1. 講師建一個「示範 Project」並**公開分享連結**（若付費方案允許）。
2. 課堂上老師觀察講師 Demo，課後自己建一個 Project 依樣操作。
3. 講師更新範本時，老師的 Project 不會自動同步——需個別通知。

---

## ⚠️ Claude Project 版與 Claude Code 版的差異

| 項目 | Claude Code 版 | Claude Project 版 |
|---|---|---|
| 產出到檔案 | ✅ 自動寫入本機 `.md` 檔 | ❌ 需手動複製 |
| 繁中潤稿 (zhtw-mcp) | ✅ 自動跑 | ❌ 需自行用其他工具 |
| TaskCreate 任務追蹤 | ✅ 有 | ❌ 無 |
| 多檔平行產出 | ✅ 一次訊息產多檔 | ⚠️ 單次對話可產，但在同一回應內 |
| 多人協作 | ❌ 單人 | ✅ Project 可邀請 |
| 門檻 | 需裝 CLI、懂終端機 | 只需瀏覽器 |
| 成本 | 免費（有額度） | 需 Claude Pro（$20/月） |

---

## 🔄 如何同步更新？

當主 repo 更新範本：

1. Project 擁有者到 Project knowledge 區。
2. 刪除舊版範本檔案。
3. 從 GitHub repo 下載最新範本，重新上傳。
4. （可選）通知同 Project 的老師「範本已更新」。

建議每 1–2 個月檢查一次主 repo 是否有更新。

---

## 📁 本資料夾檔案

| 檔名 | 用途 |
|---|---|
| [`README.md`](README.md) | 本說明檔 |
| [`system-prompt.md`](system-prompt.md) | Project 自訂指令內容（複製貼上用） |
| [`upload-checklist.md`](upload-checklist.md) | 上傳檔案清單與順序 |
| [`teacher-quickstart.md`](teacher-quickstart.md) | 發給老師的使用速查表（A4 一頁） |
