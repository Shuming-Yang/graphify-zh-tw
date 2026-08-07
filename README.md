# graphify-zh-tw · Graphify 繁體中文教學站

[Graphify](https://github.com/Graphify-Labs/graphify) 的**非官方**繁體中文教學站。把 Graphify 整個 repo（程式碼、文件、技能、測試、實作案例）做成中英對照的解說內容，並提供一個收錄真實 graphify 產出的互動知識圖譜示範。

> **免責聲明**：本站為第三方社群教學站，**與 Graphify Labs 無關**，不代表 Graphify 官方立場。Graphify 為 Graphify Labs（YC S26）的商標。

## 本站內容

- 首頁（index.html）— 概念總覽與入口
- 概念地圖（map.html）— node / edge / community / god-node 等核心概念
- 學習路線（learning-path.html）— 從安裝到讀源碼的分層路線
- 安裝指南（install.html）— OpenCode 等 17 平台安裝
- 文件教學（docs/）— 翻譯並解說 `docs/`、`ARCHITECTURE.md`、`BENCHMARKS.md`、`SECURITY.md` 等
- 程式碼對照（docs/code/）— `/graphify` 主程式、`/tools`、`/scripts`、`/tests` 逐函數講解（`<details>` 收縮）
- 實作案例（docs/worked.html）— `/worked` 五個案例 + 雙版本互動圖（英文 / 中文界面）

## 授權

本站內容以 Apache License 2.0 授權釋出（與上游相同），並保留上游的 `NOTICE` 與 `LICENSE-MIT`。

- 上游：<https://github.com/Graphify-Labs/graphify>（Apache-2.0，© 2026 Safi Shamsi and the Graphify contributors）
- 本站：<https://github.com/Shuming-Yang/graphify-zh-tw>
- 上線：<https://shuming-yang.github.io/graphify-zh-tw/>

## 開發

靜態站，純 HTML + CSS + JS，部署於 GitHub Pages（`main` 根目錄）。

```bash
python3 -m http.server 8000   # 本機預覽
```

### 啟用 GitHub Pages（一次性）

本站已 push 到 `main`，只需用 **repo 擁有者帳號**（`Shuming-Yang`，需 admin 權限）做一次設定：

1. 到 <https://github.com/Shuming-Yang/graphify-zh-tw/settings/pages>
2. **Source** 選 **Deploy from a branch**
3. **Branch** 選 `main`、資料夾 `/`（root）
4. Save → 等 1-2 分鐘建置 → 網址 `https://shuming-yang.github.io/graphify-zh-tw/`

（`check-upstream.yml` 每月自動檢查上游 v8 版本並更新版本徽章。）
