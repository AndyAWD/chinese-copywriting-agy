# 中文文案排版指北 —— Antigravity 生態系外掛程式 (chinese-copywriting-agy)

一個適用於 [Antigravity 生態系](https://antigravity.google)（包含 **Antigravity CLI (`agy`)**、**Antigravity IDE** 與 **Antigravity Desktop**）的外掛程式（Plugin）與技能（Skill），讓 AI 在撰寫或校對中文文件時，自動遵守中文文案排版規範（中英數空格、全形標點、專有名詞大小寫等）。

---

## 致謝與來源

本外掛程式與技能的規則內容改編自 [**sparanoid/chinese-copywriting-guidelines**](https://github.com/sparanoid/chinese-copywriting-guidelines) —— 由 [@sparanoid](https://github.com/sparanoid) 整理維護的「中文文案排版指北」。

原始專案採 [MIT License](https://github.com/sparanoid/chinese-copywriting-guidelines/blob/master/LICENSE.md)，本專案沿用相同授權。感謝原作者將這份寶貴的中文排版規範開源分享。

---

## 這是什麼

一份把 sparanoid 的中文排版指北封裝成 **Antigravity Plugin / Skill** 的套件。安裝後，當你請 Antigravity（`agy` CLI / IDE / Desktop）撰寫或校對中文文件時，AI 會自動套用這些規則：

- 中文與英文、數字之間補上半形空格。
- 中文語境下使用全形標點（`，。！？「」`）。
- 專有名詞使用正確拼寫（`GitHub`、`iPhone`、`macOS`、`TypeScript`⋯）。
- 不重複使用標點、不使用不道地的縮寫。

---

## 安裝方式

### 方法一：使用 `agy` CLI 指令安裝（Plugin 模式，推薦）

執行 `agy` CLI 內建的外掛程式安裝指令：

```bash
agy plugin install https://github.com/AndyAWD/chinese-copywriting-agy
```

> CLI 會將外掛程式自動放置於 `~/.gemini/antigravity-cli/plugins/chinese-copywriting-agy/`，`agy` CLI、Antigravity IDE 與 Desktop 均可自動載入。

### 方法二：Git Clone 全域外掛程式目錄安裝

亦可手動複製此專案至全域外掛程式目錄：

```bash
git clone https://github.com/AndyAWD/chinese-copywriting-agy.git ~/.gemini/config/plugins/chinese-copywriting-agy
```

### 方法三：全域技能目錄安裝（Skill 模式）

若僅需單獨載入技能（Skill）：

```bash
mkdir -p ~/.gemini/skills
cp -r skills/chinese-copywriting-guidelines ~/.gemini/skills/
```

### 方法四：專案工作區安裝（Workspace 模式）

複製至當前專案根目錄下的 `.agents/skills/` 資料夾，即可僅針對該專案生效：

```bash
mkdir -p .agents/skills
cp -r skills/chinese-copywriting-guidelines .agents/skills/
```

---

## 使用範例

### 1. 斜線指令（Slash Command）觸發

在 `agy` CLI 中可以直接使用斜線指令呼叫技能：

```text
/chinese-copywriting-guidelines 幫我校對這段中文：今天買了iPhone12花了3萬元，用github登入。
```

### 2. 自然語言對話自動觸發

> **使用者**：幫我校對這段中文：今天買了iPhone12花了3萬元，用github登入。

Antigravity 會自動套用技能並回覆：

> **Antigravity**：今天買了 iPhone 12 花了 3 萬元，用 GitHub 登入。

### 3. 撰寫 README 與文件

> **使用者**：幫我寫一段 Node.js 專案的中文 README 簡介。

Antigravity 會產出符合排版規範的內容，例如：「這是一個以 Node.js 撰寫的 CLI 工具，支援 macOS、Linux 與 Windows。」

---

## 規則摘要

| 規則種類 | 範例 |
| :--- | :--- |
| **中英文之間加空格** | 在 GitHub 上發表文章 |
| **中文與數字之間加空格** | 花了 3000 元 |
| **數字與單位之間加空格** | 20 TB 硬碟（`°`、`%` 例外：`26°C`、`78%`）|
| **中文使用全形標點** | 你好，世界！ |
| **專有名詞正確大小寫** | iPhone、macOS、TypeScript |
| **不重複使用標點** | 太厲害了！（❌ 太厲害了！！！！）|

完整規則與邊界情況請見 [`skills/chinese-copywriting-guidelines/SKILL.md`](skills/chinese-copywriting-guidelines/SKILL.md)。

---

## 授權

[MIT License](LICENSE) —— 與上游 [sparanoid/chinese-copywriting-guidelines](https://github.com/sparanoid/chinese-copywriting-guidelines) 一致。
