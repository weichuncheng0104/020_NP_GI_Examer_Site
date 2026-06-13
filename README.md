# NP 甄審 · 胃腸肝膽科題庫（網站）

專科護理師（Nurse Practitioner, NP）甄審考題解析 · 胃腸肝膽科。109–114 年「進階專科護理\_內科 / \_外科 / 通論」中與胃腸肝膽相關的題目，附逐選項詳解與教科書引註。

> **本站為自動產生的靜態網站。** 內容由私有處理層 repo `020_NP_GI_Examer` 的 pipeline 產出，請勿手改本 repo 的 HTML / JSON。

## 資料來源與免責

- 題目來源：衛生福利部公告之專科護理師甄審試題（公開可流通）。
- 解析知識依據：Sleisenger & Fordtran's 11e、Harrison 22e、Pocket Medicine 8e、Washington Manual 2022；教科書無法確認時，註明查詢 OpenEvidence 之日期時間。
- 一律以**官方標準答案**為正解。本站為個人學習用途，非臨床指引。

## GitHub Pages 啟用 SOP

1. 將本 repo push 到 GitHub（公開）。
2. `Settings` → `Pages` → `Build and deployment`：
   - Source = **Deploy from a branch**
   - Branch = **`main`** / **`/ (root)`**
3. 存檔後等 1–2 分鐘，Pages URL 形如 `https://<帳號>.github.io/<repo 名>/`。
4. 入口頁 = `index.html`；題庫頁 = `gi.html`。

## 本機預覽

```powershell
cd C:\AI_Space\020_NP_GI_Examer_Site
python -m http.server 8000
# 瀏覽 http://localhost:8000/
```

## 重新產生內容

回到處理層 repo：

```powershell
# 於處理層 repo（020_NP_GI_Examer，私有）根目錄：
.\.venv\Scripts\python.exe script\0005_build_qbank_json.py
.\.venv\Scripts\python.exe script\0006_build_site.py
# 產物會寫入本網站 repo（../020_NP_GI_Examer_Site），再回本 repo commit/push
```
