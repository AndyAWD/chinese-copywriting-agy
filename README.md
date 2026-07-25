# Chinese Copywriting Guidelines for Antigravity CLI

一個 [Antigravity CLI (agy)](https://antigravity.google) 的外掛程式（Plugin）與技能（Skill），讓 Antigravity 在撰寫或校對中文文件時，自動遵守中文文案排版規範（中英數空格、全形標點、專有名詞大小寫等）。

---

## 致謝與來源

本外掛程式與技能的規則內容改編自 [**sparanoid/chinese-copywriting-guidelines**](https://github.com/sparanoid/chinese-copywriting-guidelines) —— 由 [@sparanoid](https://github.com/sparanoid) 整理維護的「中文文案排版指北」。

原始專案採 [MIT License](https://github.com/sparanoid/chinese-copywriting-guidelines/blob/master/LICENSE.md)，本專案沿用相同授權。感謝原作者將這份寶貴的中文排版規範開源分享。

---

## 這是什麼

一份把 sparanoid 的中文排版指北封裝成 **Antigravity Plugin / Skill** 的套件。安裝後，當你請 Antigravity 撰寫或校對中文文件時，AI 會自動套用這些規則：

- 中文與英文、數字之間補上半形空格
- 中文語境下使用全形標點（`，。！？「」`）
- 專有名詞使用正確拼寫（`GitHub`、`iPhone`、`macOS`、`TypeScript`⋯）
- 不重複使用標點、不使用不道地的縮寫

## 誰適合用

- 部落客、技術寫作者：讓 Antigravity 幫你產出的 README、部落格文章、技術文件自動符合規範
- 開源專案維護者：維持 `.md` 文件排版一致性
- 團隊協作：讓 AI 產出的中文內容有統一風格

## 安裝方式

### 方法一：外掛程式目錄安裝（Plugin）

將此專案複製（clone）至 Antigravity 外掛程式目錄：

```bash
git clone https://github.com/AndyAWD/chinese-copywriting-guidelines-agy.git ~/.gemini/config/plugins/chinese-copywriting-guidelines
```

### 方法二：技能目錄安裝（Skill）

若僅需載入技能，可將 `skills/chinese-copywriting-guidelines` 複製至 Antigravity 技能目錄：

```bash
mkdir -p ~/.gemini/skills
cp -r skills/chinese-copywriting-guidelines ~/.gemini/skills/
```

安裝完成後，Skill 會在處理校對中文、加空格、格式化 Markdown 文件等請求時自動觸發。

## 使用範例

**範例 1：明確請求校對**

> 幫我校對這段中文：今天買了iPhone12花了3萬元，用github登入。

Antigravity 會回覆：

> 今天買了 iPhone 12 花了 3 萬元，用 GitHub 登入。

**範例 2：撰寫 README**

> 幫我寫一段 Node.js 專案的中文 README 簡介。

Antigravity 會產出符合排版規範的內容，例如：「這是一個以 Node.js 撰寫的 CLI 工具，支援 macOS、Linux 與 Windows。」

**範例 3：不觸發**

> 幫我寫一段 Python for loop 的註解。

Skill 不會觸發 —— 程式碼註解、code comments 屬於排除情境。

## 規則摘要

| 規則 | 範例 |
|------|------|
| 中英文之間加空格 | 在 GitHub 上發表文章 |
| 中文與數字之間加空格 | 花了 3000 元 |
| 數字與單位之間加空格 | 20 TB 硬碟（`°`、`%` 例外：`26°C`、`78%`）|
| 中文用全形標點 | 你好，世界！ |
| 專有名詞正確大小寫 | iPhone、macOS、TypeScript |
| 不重複使用標點 | 太厲害了！（❌ 太厲害了！！！！）|

完整規則與邊界情況請見 [`skills/chinese-copywriting-guidelines/SKILL.md`](skills/chinese-copywriting-guidelines/SKILL.md)。

## 授權

[MIT License](LICENSE) —— 與上游 [sparanoid/chinese-copywriting-guidelines](https://github.com/sparanoid/chinese-copywriting-guidelines) 一致。
