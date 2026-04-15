# Project Knowledge 上傳清單

> 在 Claude Project 設定頁的「Project knowledge」區，依下列順序上傳 6 份範本檔案。Claude 會在收到老師任務時，自動參考這些範本填空產出。

---

## 📋 上傳清單

從主 repo 的 `templates/` 資料夾下載以下 6 個檔案：

| 順序 | 檔名 | 大小 | 用途 |
|---|---|---|---|
| 1 | [`01_teacher_notes.md`](../templates/01_teacher_notes.md) | 約 3KB | 教師手冊範本 |
| 2 | [`02_slides_outline.md`](../templates/02_slides_outline.md) | 約 4KB | 10 頁簡報大綱範本 |
| 3 | [`03_worksheet.md`](../templates/03_worksheet.md) | 約 3KB | 學習單範本 |
| 4 | [`04_quiz.md`](../templates/04_quiz.md) | 約 4KB | 測驗題目範本 |
| 5 | [`05_image_prompts.md`](../templates/05_image_prompts.md) | 約 5KB | 12 組英文圖像提示詞範本 |
| 6 | [`06_dialogue_script.md`](../templates/06_dialogue_script.md) | 約 5KB | 雙語對話腳本範本（僅語言科） |

**總檔案大小**：約 24KB，遠低於 Claude Project Knowledge 上限。

---

## 📥 下載方式

### 方式 A：從 GitHub 直接下載

1. 到主 repo：[github.com/AndyJuang/lesson-plan-skill](https://github.com/AndyJuang/lesson-plan-skill)
2. 點 `Code` → `Download ZIP`。
3. 解壓後，`templates/` 資料夾內的 6 個 `.md` 檔案即為上傳對象。

### 方式 B：逐檔下載

1. 點 [templates/01_teacher_notes.md](https://github.com/AndyJuang/lesson-plan-skill/blob/main/templates/01_teacher_notes.md)。
2. 點右上角 `Raw` 按鈕。
3. 右鍵「另存新檔」，存成 `01_teacher_notes.md`。
4. 對其他 5 個檔案重複步驟 1–3。

### 方式 C：用 git（適合有終端機經驗者）

```bash
git clone https://github.com/AndyJuang/lesson-plan-skill.git
cd lesson-plan-skill/templates
# 6 個檔案已在此資料夾
```

---

## 📤 上傳到 Claude Project

1. 登入 [claude.ai](https://claude.ai)。
2. 進入你建立的 Project。
3. 在 Project 頁面找 **「Project knowledge」** 區塊，點 `Add content` 或拖曳檔案進去。
4. **依清單順序**上傳 6 個 `.md` 檔案。
5. 確認每個檔案都顯示成功 icon。

---

## ✅ 上傳後測試

在 Project 聊天室輸入：

```
請列出你目前 Project knowledge 中有哪些範本檔案？
```

Claude 應該回覆 6 個檔名。若少於 6 個，請回 Project knowledge 區確認是否有檔案未上傳成功。

---

## 🔄 更新範本（主 repo 有新版本時）

1. 到 Project knowledge 區。
2. 刪除舊版的對應檔案。
3. 從主 repo 下載新版。
4. 重新上傳。

**建議**：每季或每學期檢查一次主 repo `CHANGELOG.md`（若有）或 release tag，確認是否有升級。

---

## ⚠️ 注意事項

- 上傳後如果修改了**本機檔案**，不會自動同步到 Project——需手動重傳。
- Project knowledge 有**版本限制**（依方案而定），保留 6 個範本檔無虞。
- 若有自行新增的「校本客製化範本」，建議命名為 `07_校本_XXX.md` 避免與主範本衝突。
