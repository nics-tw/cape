# CAPE 團隊網站 / CAPE Team Site

## Hugo 主題 / Hugo Theme

使用的主題：Hextra: https://github.com/imfing/hextra

The theme we use: Hextra: https://github.com/imfing/hextra

### 相關文件 / Documentation

主題文件：https://imfing.github.io/hextra/docs/

Theme Documentation: https://imfing.github.io/hextra/docs/

Hugo 文件：https://gohugo.io/documentation/

Hugo Documentation: https://gohugo.io/documentation/

### 功能特色 / Features

- [檔案組織](https://imfing.github.io/hextra/docs/guide/organize-files/)
- [Markdown 語法](https://imfing.github.io/hextra/docs/guide/markdown/)，支援 `GitHub 樣式提示框`
- [程式碼高亮](https://imfing.github.io/hextra/docs/guide/syntax-highlighting/)
- [LaTeX 數學公式](https://imfing.github.io/hextra/docs/guide/latex/)，基於 `KaTeX`
- [圖表繪製](https://imfing.github.io/hextra/docs/guide/diagrams/)，目前僅支援 `Mermaid`
- [短代碼](https://imfing.github.io/hextra/docs/guide/shortcodes/)，包含：
  - Callout（標註提示）
  - Cards（卡片）
  - Details（詳細資訊）
  - FileTree（檔案樹）
  - Icon（圖示）
  - Steps（步驟）
  - Tabs（分頁）
  - Jupyter Notebook（測試版）
  - 其他（Badge、YouTube、PDF）
- [自訂 Hextra](https://imfing.github.io/hextra/docs/advanced/customization/)，包含：
  - 自訂 CSS
  - 自訂腳本
  - 自訂版面

---

- [Organize Files](https://imfing.github.io/hextra/docs/guide/organize-files/)
- [Markdown](https://imfing.github.io/hextra/docs/guide/markdown/), supports `GitHub-style alerts`
- [Syntax Highlighting](https://imfing.github.io/hextra/docs/guide/syntax-highlighting/)
- [LaTeX](https://imfing.github.io/hextra/docs/guide/latex/), based on `KaTeX`
- [Diagrams](https://imfing.github.io/hextra/docs/guide/diagrams/), currently only supports `Mermaid`
- [Shortcodes](https://imfing.github.io/hextra/docs/guide/shortcodes/), including:
  - Callout
  - Cards
  - Details
  - FileTree
  - Icon
  - Steps
  - Tabs
  - Jupyter Notebook (alpha)
  - Others (Badge, YouTube, PDF)
- [Customizing Hextra](https://imfing.github.io/hextra/docs/advanced/customization/), including:
  - Custom CSS
  - Custom Scripts
  - Custom Layouts

## 新增文章步驟 / Steps to Add New Posts

### 1. 建立新內容 / Create New Content

使用指令建立新的內容分支：`hugo new content/_index.md`、`hugo new content/docs/_index.md` 等。

Create new branches for new contents via `hugo new content/_index.md`, `hugo new content/docs/_index.md` etc.

### 2. 圖片優化 / Image Optimization

使用 [Clop](https://github.com/FuzzyIdeas/Clop) 優化圖片，並存放在 `static/images` 目錄。

Optimize images via [Clop](https://github.com/FuzzyIdeas/Clop) and store them in `static/images`.

### 3. 目錄與圖片注意事項 / Notes for TOC and Images

#### 目錄 (TOC) / Table of Contents

`Hextra` 會根據標題產生目錄，H1 用於文章標題且不會顯示在目錄中。目錄只會顯示 H2 及以下的標題。

`Hextra` generates TOC based on headings. H1 is used for post title and won't show up in TOC. TOC only shows H2 and below.

#### 圖片路徑 / Image Paths

由於我們的網站網址不是基礎網址（例如 `https://nics-tw.github.io/`），而是相對網址（例如 `https://nics-tw.github.io/cape/`），因此在插入圖片時需要加上 `/cape/`：

Since our website URL is not base URL (e.g. `https://nics-tw.github.io/`), but relative URL (e.g. `https://nics-tw.github.io/cape/`), we need to add `/cape/` when inserting images:

- Markdown 格式 / Markdown style: `![some pic](/cape/images/aaa.bbb)`
- HTML 格式 / HTML style: `<p align="center"><img src="/cape/images/aaa.bbb"></p>`

### 4. 前置資料 / Front Matter

- [版面配置 / Layouts](https://imfing.github.io/hextra/docs/guide/organize-files/#layouts)
- [側邊欄導覽 / Sidebar Navigation](https://imfing.github.io/hextra/docs/guide/organize-files/#sidebar-navigation)
- [麵包屑導覽 / Breadcrumb Navigation](https://imfing.github.io/hextra/docs/guide/organize-files/#breadcrumb-navigation)
- [LaTeX 支援 / LaTeX](https://imfing.github.io/hextra/docs/guide/latex/)
- [Hugo 原生支援 / Hugo Native](https://gohugo.io/content-management/front-matter/)
- `next`: 文末的下一篇文章按鈕 / Next post button at the end of the post (例如 / e.g. `next: docs/usage/`)
- `prev`: 文末的上一篇文章按鈕 / Previous post button at the end of the post (例如 / e.g. `prev: docs/`)

### 5. 本地預覽 / Local Preview

執行以下指令在本地預覽網站：

Preview the site locally with the following command:

```bash
hugo server --gc --disableFastRender
```

**注意**：由於本地網址是基礎網址，圖片可能無法正常顯示。

**Note**: Images won't show properly since local URL is base URL.
