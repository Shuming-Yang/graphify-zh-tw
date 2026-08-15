# graphify-zh-tw · Graphify 繁體中文教學站

[Graphify](https://github.com/Graphify-Labs/graphify) 的**非官方**繁體中文教學站。把 Graphify 整個 repo（程式碼、文件、技能、測試、實作案例）做成中英對照的解說內容，並收錄真實 graphify 產出的**可操作互動知識圖譜**示範。

> **免責聲明**：本站為第三方社群教學站，**與 Graphify Labs 無關**，不代表 Graphify 官方立場。Graphify 為 Graphify Labs（YC S26）的商標，本站僅在描述性／教學語境下使用該名稱。

**上線網站：<https://shuming-yang.github.io/graphify-zh-tw/>**

## 目錄

- [網站亮點](#網站亮點)
- [網站地圖](#網站地圖)
- [實作案例總覽](#實作案例總覽)
- [我們怎麼跑的](#我們怎麼跑的)
- [授權](#授權)
- [上游同步](#上游同步)
- [開發](#開發)
- [如何新增一個案例](#如何新增一個案例)
- [已知限制](#已知限制)
- [回饋與貢獻](#回饋與貢獻)

---

## 網站亮點

1. **中英對照** — 中文口語解說為主文，英文原文與程式碼保留上游原貌。文件頁用「可展開的英文原文」，程式碼頁用「附中文註解的原始碼」。
2. **程式碼逐函數講解** — 每個函數一個 `<details>` 收縮塊（signature + 中文用途 + 關鍵邏輯），核心函數附逐行中文註解；短函數用段落式說明。
3. **策展式教學而非鏡像** — 700+ 檔案的 repo 不逐檔翻譯，挑「值得教學」的文件與程式碼深入講解。
4. **實機互動圖** — 收錄 6 個真實 graphify 產出的知識圖譜，每個都有英文／中文界面雙版本，訪客可直接拖曳、搜尋、點節點。
5. **版本釘選** — 上游對齊 `v8 @ 9f25a3a`；OpenCode 案例釘選 `opencode@1.18.15 @ fe82a1b6`，數據可追溯。

## 網站地圖

純靜態站（HTML + CSS + JS），GitHub Pages 部署於 `main` 根目錄。

```
graphify-zh-tw/
├── index.html            首頁：Graphify 是什麼、三大亮點、入口卡
├── map.html              概念地圖：24 個可點概念節點（node/edge/community/god-node…）
├── learning-path.html    學習路線 L0→L4：19 張可點卡片
├── install.html          安裝指南：17 平台指令、延伸套件、疑難排解
├── about.html            授權、方法、免責聲明
├── docs/
│   ├── index.html        文件教學入口（hub）
│   ├── how-it-works.html 運作原理（三遍處理／Leiden／信任標籤／token 經濟）
│   ├── architecture.html 架構總覽（七階段 pipeline／14 模組職責表／新增語言）
│   ├── benchmarks.html   效能基準（LOCOMO／LongMemEval-S／ERPNext）
│   ├── security.html     安全模型（威脅面逐條解析）
│   ├── incremental.html  增量更新 + 實體去重（設計 + 實作計劃）
│   ├── node-summaries-rfc.html  RFC 講解（Option A vs B）
│   ├── docker-mcp-sqlite.html  Docker MCP + SQLite runbook
│   ├── skill-files.html  技能檔結構拆解（SKILL.md + references/ + skillgen）
│   ├── changelog-summary.html  版本演進摘要
│   ├── worked.html       實作案例入口（6 張案例卡）
│   ├── case/             六個案例頁（中文解說 + 互動圖 + 本站跑的數字）
│   └── code/             程式碼對照（9 頁，逐函數 <details>）
│       ├── index.html    入口
│       ├── pipeline.html     detect + extract + build + cluster
│       ├── extractors.html   extractors/ 語言抽取器
│       ├── analysis.html     analyze + report
│       ├── export.html       export + exporters
│       ├── ops.html          cache / dedup / ingest / watch / serve / security / validate
│       ├── cli.html          cli.py 指令層
│       ├── skillgen.html     tools/skillgen
│       ├── gen-demo-path.html scripts/gen_demo_path.py
│       └── tests.html        tests 測試策略
├── worked/               六案例的互動圖與報告（每個含 graph.html + graph-zh.html + GRAPH_REPORT.md）
└── assets/                site.css / favicon.svg / 官方 docs 資產
```

## 實作案例總覽

每個案例都是「中文解說 + 互動圖（EN/ZH 界面）+ 本站跑的數字 + 重現步驟」。

| 案例 | 語料 | 來源方式 | 本站數字 | 互動圖 |
|---|---|---|---|---|
| [**OpenCode**](docs/case/opencode.html) | `anomalyco/opencode` 的 `packages/opencode`，363 個 TypeScript 檔 | **本站實跑** `--code-only`，**版本釘選 `1.18.15 @ fe82a1b6`** | 3903 節點 / 8701 邊 / 159 社群 | ✅ 雙版本 |
| [rsl-siege-manager](docs/case/rsl-siege-manager.html) | 真實全棧 monorepo（Python + TS） | 上游完整抽取產出（沿用） | 1886 節點 / 3876 邊 / 141 社群 | ✅ 雙版本 |
| [karpathy-repos](docs/case/karpathy-repos.html) | nanoGPT / minGPT / micrograd + 論文 + 圖片 | 上游圖資料，本站重新分群 | 177 節點 / 246 邊 / 16 社群 | ✅ 雙版本 |
| [httpx](docs/case/httpx.html) | 6 個純 Python 檔的合成函式庫 | **本站全跑**（零 API key） | 193 節點 / 456 邊 / 6 社群 | ✅ 雙版本 |
| [mixed-corpus](docs/case/mixed-corpus.html) | Python + markdown 論文 + 圖片 | 上游圖資料，本站重新分群 | 22 節點 / 38 邊 / 4 社群 | ✅ 雙版本 |
| [example](docs/case/example.html) | 最小文件管線 | **本站跑** `--code-only`（文件部分標註略過） | 73 節點 / 134 邊 / 5 社群 | ✅ 雙版本 |

> 所有案例的圖都是**真實 graphify 產出**，不是示意圖。OpenCode 案例是「用 OpenCode 建站、順便用 graphify 分析 OpenCode」的 meta 示範。

## 我們怎麼跑的

本站所有案例數字都是用**本機 graphify CLI** 實際跑的（`graphify 0.9.36`）：

```bash
# 0. 安裝（PyPI 套件名是 graphifyy，雙 y）
uv tool install graphifyy

# 1. 純程式碼語料：code-only 抽取（零 API key、純本機 AST）
graphify extract <corpus> --code-only

# 2. 分群 + 生成 GRAPH_REPORT.md 與 graph.html
graphify cluster-only <corpus>

# 3. 互動圖中文化：把 graph.html 的 UI 字串轉成繁體中文
#    （節點 label 是程式識別符，保持英文）→ graph-zh.html
```

- **有 LLM key 時**可跑完整抽取（文件／PDF／圖片也能進圖）；本站因無 key，程式碼部分全程零成本。
- **從上游 graph.json 重現**（karpathy / mixed）：載入已提交的圖資料 → 重新分群 → 生成互動圖，保留論文與圖片節點。
- 中文化互動圖的做法：對 `graph.html` 做 UI 字串替換（搜尋框、節點資訊、社群圖例、統計列、`lang="zh-Hant"`），節點名稱保留英文。

## 授權

- 本站內容以 **Apache License 2.0** 釋出（與上游相同），並照抄上游的三份授權檔：
  - [`LICENSE`](LICENSE) — Apache-2.0 全文
  - [`LICENSE-MIT`](LICENSE-MIT) — 重新授權前以 MIT 貢獻的部分（© 2026 Safi Shamsi）
  - [`NOTICE`](NOTICE) — "Graphify Copyright 2026 Safi Shamsi and the Graphify contributors"
- **商標**：Graphify 為 Graphify Labs（YC S26）的商標。Apache-2.0 授權不含商標授權；本站僅在「描述性／教學」語境使用該名稱，並於全站 footer 標示「與 Graphify Labs 無關」。
- **為何不翻譯技能檔**：`graphify/skill*.md` 與 `references/` 是 skillgen 程式化產出的 generated artifacts（`tools/skillgen/`），翻譯會破壞其 round-trip 校驗與功能。本站以「中文講解」方式處理技能檔，而非翻譯可安裝版本。
- 官方 `docs/graph-hero.png` 與 `docs/demo-path.svg` 為上游 docs 資產，本站引用並標註出處；未使用官方 logo 作為網站視覺。

## 上游同步

- 本站對齊上游分支 **`v8`**，釘選 commit **`9f25a3a`**（圖形內容隨上游演進）。
- `.github/workflows/check-upstream.yml` **每月自動**（每月 1 日 00:00 UTC + 手動觸發）檢查上游最新 SHA，並更新首頁的版本徽章。
- OpenCode 案例另釘選 `opencode@1.18.15 @ fe82a1b6`，分析日期 2026-08-08。

## 開發

靜態站，純 HTML + CSS + JS，無框架、無建置步驟。

```bash
python3 -m http.server 8000   # 本機預覽
```

### 目錄結構速查

- `assets/site.css` — 全站樣式（深色 × 霓虹設計語言，承襲 mattpocock-skills-zh-tw）
- 每個 HTML 頁都是自含檔案（head 引入 site.css + Google Fonts）
- `worked/<slug>/` — 案例的 `graph.html`（英文）、`graph-zh.html`（中文界面）、`GRAPH_REPORT.md`

## 如何新增一個案例

1. **準備語料**：`mkdir raw && git clone <repo> raw/<name>`（或直接指一個資料夾）。
2. **抽取**：`graphify extract ./raw --code-only`（純程式碼零 key）；有 LLM key 則可跑完整版。
3. **分群 + 產出**：`graphify cluster-only ./raw` → 得到 `graph.html`、`GRAPH_REPORT.md`、`graph.json`。
4. **中文化**：複製 `graph.html` → 替換 UI 字串 → `graph-zh.html`（見 [我們怎麼跑的](#我們怎麼跑的)）。
5. **收錄**：把三樣東西放進 `worked/<slug>/`。
6. **建案例頁**：依 `docs/case/<slug>.html` 的模板（中文解說 + iframe 嵌入互動圖 + 本站數字表 + 重現步驟）。
7. **更新** `docs/worked.html` 的案例卡。

## 已知限制

- **無 LLM key 時**：文件／PDF／圖片語料會被 `--code-only` 略過（會在案例頁標註）。要完整抽取需設 `GEMINI_API_KEY` / `MOONSHOT_API_KEY` / `ANTHROPIC_API_KEY` 等。
- **互動圖節點上限**：預設 5000 節點（`exporters/html.py` 的 `MAX_NODES_FOR_VIZ`）。超過時可用 `GRAPHIFY_VIZ_NODE_LIMIT=<N>` 提高，或退而呈現 `graph.json` 統計與 `GRAPH_REPORT.md`。OpenCode 案例 3903 節點在界內。
- **本機 graphify 版本**：`--code-only` 等新 flag 需要 0.9.x；0.8.44 及更早已無此旗標（本站已升到 0.9.36）。

## 回饋與貢獻

- 本站是教學站，不是官方文件。發現翻譯錯誤或想補充主題，歡迎開 [issue](https://github.com/Shuming-Yang/graphify-zh-tw/issues)。
- 想貢獻案例：跑一個真實 repo 的 graphify 產出，依[新增案例流程](#如何新增一個案例)發 PR。

---

**相關連結**

- 上游 repo：[Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify)（Apache-2.0）
- 官方網站：[graphify.com](https://graphify.com)
- PyPI 套件：`graphifyy`（雙 y）→ CLI 指令為 `graphify`
- 本站 repo：[Shuming-Yang/graphify-zh-tw](https://github.com/Shuming-Yang/graphify-zh-tw)
- 本站上線：[shuming-yang.github.io/graphify-zh-tw](https://shuming-yang.github.io/graphify-zh-tw/)
- 學習路徑建議服務：[learning-path-advisor](https://shuming-yang.github.io/learning-path-advisor/) — 依角色推薦教學網站學習路徑
