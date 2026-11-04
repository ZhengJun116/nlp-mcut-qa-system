# NLP 自然語言處理 (115 S1) - 課程專案

本專案為 NLP 課程開發環境與實作練習區。

---

## 開發者資訊 (Developer Info)
* **學號**：[U12627042]
* **姓名**：[鄭軍]

## 硬體與環境狀態 (Environment Setup)
* **PyTorch 執行環境**：Windows CUDA 12.8

---

## 課程任務清單 (Task Checklist)

### Week 2：開發環境與專案架構初始化
請在完成下列任務後，將 `[ ]` 改為 `[x]`：
- [x] 成功建立 GitHub 帳號並 Clone 本專案至本機端。
- [x] 成功建立 `.venv` 虛擬環境，並透過 `.gitignore` 隱藏底層檔案。
- [x] 成功於虛擬環境內安裝通用套件清單 (`requirements.txt`) 與專屬硬體版本的 PyTorch。
- [x] 更新本 README 文件，填寫學號、姓名與 PyTorch 環境狀態。
- [x] 成功使用 Git 完成 `commit` 並 `push` 同步至 GitHub 雲端。
### Week 4 / 8: Data Ingestion & Topology-Aware Chunking
- [x] **環境建置與版控防護**：更新 `.gitignore` 成功阻擋原始 PDF 與暫存 JSON，並保留 `.keep` 目錄結構。
- [x] **資料擷取與合併**：任務 1-A 頁首頁尾清除、1-B 雙語標題合併、1-C 雙語條文合併 (完成者分別打勾)。
  - [x] 1-A
  - [x] 1-B
  - [x] 1-C
- [x] **結構健全度 (Mechanical Sanity)**：
  - [x] 拓撲錨定率
  - [x] 運用「中位數 (Median)」計算文本長度。
- [x] **語意品質 (Semantic Quality)**：
  - [x] (選修) 成功計算 Shannon Information Entropy (夏農資訊熵)，比較 Cleaned 與 Raw 資料的中位數資訊熵。
- [x] **觀測儀表板與報告**：
  - [x] 成功繪製 4 拼圖資料觀測儀表板 (4-Panel Dashboard)。
  - [x] 成功將核心評估指標匯出為根目錄下的 `metrics.json`。
