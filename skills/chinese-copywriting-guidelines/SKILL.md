---
name: chinese-copywriting-guidelines
description: 套用 sparanoid/chinese-copywriting-guidelines 的中文文案排版規則 —— 中英文與數字之間補空格、使用全形中文標點、專有名詞正確大小寫（如 GitHub、iPhone、TypeScript、macOS）。當使用者明確請求「校對中文」「套用中文排版」「加空格」「pangu」「中文格式化」，或是 Antigravity (含 agy CLI, Antigravity IDE, Antigravity Backup/Desktop) 在撰寫、編輯 .md、.mdx、.txt、.rst 等文件檔的中文內容時，務必觸發此 skill。程式碼、code comments、字串常數、URL、檔名、以及純英文內容不套用。
---

# 中文文案排版指北（Chinese Copywriting Guidelines）

這份 skill 讓 Antigravity 全系列產品（包含 Antigravity CLI `agy`、Antigravity IDE、Antigravity Backup/Desktop）在撰寫或校對中文文件時，自動遵守 [sparanoid/chinese-copywriting-guidelines](https://github.com/sparanoid/chinese-copywriting-guidelines) 的排版規範。核心目的是讓混合中文、英文、數字的內容讀起來更清爽、更專業。

## 何時使用（When to use）

在以下情境套用：

- 使用者明確要求：「幫我校對中文」「加空格」「套用中文排版」「pangu 一下」「中文格式化」
- 撰寫或編輯 `.md`、`.mdx`、`.markdown`、`.txt`、`.rst`、`.asciidoc` 等文件檔，且內容含中文
- 產出 README、部落格文章、技術文件、Release Notes、Changelog、簡報講稿

## 何時不使用（When NOT to use）

以下情境**不套用**規則，因為會破壞語意或格式：

- 程式碼本體（`.py`、`.js`、`.ts`、`.go` 等）—— 變數名、函式名、字串常數不動
- 程式碼區塊內（Markdown 的三個反引號區塊，或行內 `code`）
- 檔名、URL、路徑、指令
- 純英文或純中文內容（沒有混排就不需要空格）
- 引用他人原文、詩詞、法律條文 —— 保留原樣
- 使用者明確要求「不要加空格」或「保持原樣」時

## 規則詳解

### 一、空格規則

#### 1.1 中英文之間加一個半形空格

- 正確：在 LeanCloud 上，資料儲存是圍繞 `AVObject` 進行的。
- 錯誤：在LeanCloud上，資料儲存是圍繞`AVObject`進行的。

#### 1.2 中文與數字之間加一個半形空格

- 正確：今天出去買菜花了 5000 元。
- 錯誤：今天出去買菜花了5000元。

#### 1.3 數字與單位之間加一個半形空格

- 正確：我家的光纖寬頻有 10 Gbps，SSD 一共有 20 TB。
- 錯誤：我家的光纖寬頻有10Gbps，SSD一共有20TB。

**例外**：度數（`°`）與百分比（`%`）緊貼數字，不加空格。

- 正確：今天氣溫 26°C，濕度 78%。
- 錯誤：今天氣溫 26 °C，濕度 78 %。

#### 1.4 全形標點與其他字元之間不加空格

全形標點（如 `，。！？「」`）已經有視覺留白，兩側**不要**再加空格。

- 正確：剛剛買了一部 iPhone，好開心！
- 錯誤：剛剛買了一部 iPhone ，好開心！

### 二、標點符號規則

#### 2.1 不重複使用標點符號

情緒可以用文字傳達，不要靠標點灌水。

- 正確：德國隊竟然戰勝了巴西隊！
- 正確：她竟然對你說「喵」？！
- 錯誤：德國隊竟然戰勝了巴西隊！！！！！！！！

### 三、全形與半形

#### 3.1 中文內容使用全形標點

`，。！？；：「」『』（）` 這類標點在中文語境中一律使用全形。

- 正確：嗨！你知道嗎？今天前台的小妹跟我說「喵」了哎！
- 錯誤：嗨! 你知道嗎? 今天前台的小妹跟我說 "喵" 了哎!

#### 3.2 數字一律使用半形

- 正確：這件蛋糕只賣 1000 元。
- 錯誤：這件蛋糕只賣 １０００ 元。

#### 3.3 英文整句、英文引用內部使用半形標點

當引用整段英文或英文句子時，句內標點跟著英文走。

- 正確：賈伯斯那句話是怎麼說的？『Stay hungry, stay foolish.』
- 錯誤：賈伯斯那句話是怎麼說的？『Stay hungry，stay foolish。』

### 四、專有名詞大小寫

品牌名、產品名、技術名詞務必使用官方的正確拼寫與大小寫。這是對品牌的尊重，也讓讀者一眼看出你懂行。

#### 常見對照表

| 正確 | 常見錯誤 |
|------|----------|
| GitHub | github、GITHUB、Github |
| iPhone | iphone、IPhone、Iphone |
| iPad | ipad、IPad |
| macOS | Mac OS、MacOS、mac os |
| iOS | ios、IOS |
| JavaScript | Javascript、javascript、JAVASCRIPT |
| TypeScript | Typescript、typescript |
| Node.js | NodeJS、nodejs、Nodejs |
| npm | NPM、Npm |
| Vue.js | VueJS、vuejs |
| Next.js | NextJS、nextjs |
| React | react、REACT |
| PostgreSQL | postgresql、Postgres SQL |
| MySQL | mysql、Mysql |

#### 不使用不道地的縮寫

- 正確：熟悉 TypeScript、HTML5，至少了解一種框架（如 React、Next.js）。
- 錯誤：熟悉 Ts、h5，框架如 RJS、nextjs 的 FED。

碰到不確定的名詞時，優先查官方網站的寫法，不要憑印象。

## 邊界情況與判斷原則

### 什麼要改

- 中文段落中的英文單字、產品名、技術名詞
- 中文段落中的阿拉伯數字
- 半形標點誤用在中文語境（`,` → `，`；`?` → `？`）

### 什麼不要改

- Markdown 的 ` ``` ` 程式碼區塊內容
- Markdown 的行內 `` `code` ``
- 連結文字內的技術符號：`[hello_world.py](./hello_world.py)` 中的檔名
- URL 本身
- YAML frontmatter 內的技術欄位值
- 使用者引用的原文（詩、歌詞、法條、他人文章）

### 判斷原則

當不確定時，優先考慮：

1. **可讀性優先**：加了空格如果讓句子更難讀（如緊密的技術術語 `TCP/IP`），保留原樣。
2. **語意優先**：不要為了排版改變原意，尤其是引用他人內容時。
3. **一致性優先**：同一份文件內規則要一致，不要一段有空格一段沒有。

## 套用時的具體做法

當使用者請求校對或格式化中文文件時：

1. **先讀完整段內容**，判斷是文件、程式碼、還是混合內容
2. **逐條套用規則**，特別注意中英數之間的空格與全形標點
3. **保留原本語意與段落結構**，只調整排版
4. **修正後的檔案要能直接使用**，不要留下 `<!-- TODO -->` 之類的標記
5. **修改幅度較大時，簡短說明改了什麼**（例如「已修正 12 處中英文空格、3 處全形標點」），方便使用者確認

## 致謝

規則內容改編自 [sparanoid/chinese-copywriting-guidelines](https://github.com/sparanoid/chinese-copywriting-guidelines)（MIT License），感謝原作者 [@sparanoid](https://github.com/sparanoid) 的整理。
