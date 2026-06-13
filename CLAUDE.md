# CLAUDE.md — 020_NP_GI_Examer_Site（Repo B，網站層，公開）

> 這是 **generated site repo**。內容全部由處理層 repo `../020_NP_GI_Examer`（私有）的 build script 產出。
> **Source of truth = `../020_NP_GI_Examer`。本 repo 的 HTML / JSON 一律由 build 產生，禁止手改。**

## 鐵律

1. **禁手改**：`index.html` / `gi.html` / `data/qbank_gi.json` / `assets/` 都是 build 產物。要改內容 → 回 `../020_NP_GI_Examer` 改 pipeline / 解析 → 重跑 `0004_build_qbank_json.py` + `0005_build_site.py` → 重新產出到本 repo → commit/push。
2. **公開 repo，零 secret**：不放 `.env`、不放原始考題 PDF、不放 pipeline script、不放 OpenEvidence 查詢全文（OE 全文留在私有 Repo A 的 `OE_record/`；本站只顯示「🔎 YYYYMMDD_HHMM 查詢 OpenEvidence」時間戳引用）。
3. **deploy = GitHub Pages from root**：`Settings → Pages → Build from a branch → main / (root)`。從**根目錄**上線，故所有檔案放 repo 根，不放子資料夾。
4. **無帳號**：純前端 + localStorage（key `np_gi_v1`）；跨裝置同步是 Phase 2。

## 結構

```
index.html              # 入口導覽
gi.html                 # 胃腸肝膽科題庫單檔（inline Q[] + E{}）
data/qbank_gi.json      # 由 Repo A 0004 產出
assets/                 # 可選 css/圖
README.md               # Pages 啟用 SOP
```

## commit 前綴

`feat:` / `fix:` / `chore:` / `docs:`
