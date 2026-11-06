---
marp: true
theme: gaia
paginate: true
footer: "NLP 自然語言處理 115-S1"
---

<style>
  /* 1. Global Layout: Banner & Logo */
  section {
    background-color: #f8fafc;
    background-image: 
      url('./department_logo.png'), 
      linear-gradient(to right, #e0f2fe, #bae6fd);
    background-size: 
      50px 50px, 
      100% 95px; /* Slightly slimmer banner height */
    background-position: 
      calc(100% - 35px) 22px, 
      top left;
    background-repeat: no-repeat;

    /* ─── Fix 1: Pull content up closer to the banner ─── */
    padding-top: 120px;    /* Reduced from 160px */
    padding-bottom: 60px; /* Reserves space so text never overlaps footer/page number */
    padding-left: 60px;
    padding-right: 60px;
    justify-content: flex-start;

    /* ─── Fix 2: Compact font size for lecture/technical slides ─── */
    font-size: 26px;       /* Default is ~30px; 24-26px fits technical lists cleanly */
    line-height: 1.45;
  }

  /* ─── Fix 3: Remove default gap above the first bullet point ─── */
  section > ul,
  section > ol,
  section > p {
    margin-top: 20px;
    margin-bottom: 8px;
  }

  /* Tighter nested list spacing */
  section li {
    margin-bottom: 4px;
  }

  /* 2. Map Markdown Header (#) into the Banner Space */
  section h1 {
    position: absolute;
    top: 0;
    left: 0;
    margin: 0;
    padding: 24px 50px;     /* Centered vertically inside the 95px banner */
    width: calc(100% - 130px);
    font-size: 34px;
    font-weight: bold;
    color: #0f172a;
  }

  /* 3. Title Slide (retains center alignment & original scale) */
  section.title-slide {
    background-image: none;
    background-color: #f0f9ff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px;
    font-size: 30px;
  }

  section.title-slide h1 {
    position: static;
    width: 100%;
    padding: 0;
    font-size: 52px;
    color: #0369a1;
  }
</style>

<!-- _class: title-slide -->

# NLP 自然語言處理

<br/>

## <center> Week 09 期中評量：DATA_REPORT.md </center>

<br/>

#### 115 (上學期) 工業人工智慧學程 (選)

**林淯慈 Pauline Lin**

Week 09

---

# 期中評量調整 (Change to the Midterm)

* **期中不需要建立 Git Tag 與 Release。** 這項技能將在期末前教授 (期末需建立 `v1.0-final`)。
* 原本 Tag 與 Release 的 10%，平均移到第 3 節與第 4 節：

| 項目 | 比重 |
|---|---|
| 1. 資料集概覽 | 10% |
| 2. 清洗步驟 (對照截圖與說明) | 20% |
| 3. 評估指標與 AI 解讀查證 | **30%** |
| 4. 一個尚未解決的問題 | **30%** |
| 5. AI 協作 | 10% |

---

# 今日流程 (Today's Plan)

| 時間 | 內容 |
|---|---|
| 9:00 – 9:10 | 下載檔案；公布 **SEED** 與參考值；執行 `09_midterm_chunks` |
| 9:10 – 9:40 | 第 1 節 資料集概覽、第 2 節 清洗步驟 (表格與截圖) |
| 9:40 – 10:30 | 第 3.1–3.3 節 指標表、請 AI 解讀、查證兩個說法 |
| **10:30** | **先 Commit & Push 一次** (保險) |
| 10:30 – 11:00 | 第 3.4 節 你被指定的兩個 chunk |
| 11:00 – 11:30 | 第 4 節 一個尚未解決的問題、第 5 節 AI 協作 |
| 11:30 – 11:50 | 對照檢查清單；**11:50 前最後 Commit & Push** (以 **11:50** 的版本評分) |

**截止：11/6 11:50 前 Push**

---

# 步驟 0：準備檔案 (Set Up)

1. 從課程系統下載兩個檔案，放到正確位置：
   * `DATA_REPORT.md` → **專案根目錄** (與 `README.md` 同一層)
   * `09_midterm_chunks.ipynb` → **`notebooks/`** (與 `01_Data_Ingestion.ipynb` 同一層)
2. 建立截圖資料夾：在檔案總管中對專案根目錄按右鍵 → **New Folder** → `reports`，再在裡面建立 `figures`。
3. 開啟 `09_midterm_chunks.ipynb`，右上角選擇 `.venv` 核心 (Kernel)。
4. 填入 `STUDENT_ID` (你的學號) 與 `SEED` (老師公布)，點擊 **Run All**。
5. 在 VS Code 打開程式列出的**閱讀用檔案** (`cleaned_*.md`)，按 `Ctrl + G` 輸入程式給的行號，閱讀**完整**的 chunk，再填入 `DATA_REPORT.md` 第 3.4 節 (含**驗證碼**)。

---

# 繳交：Commit & Push (Submission)

**截止：11/6 11:50 前 Push**：`DATA_REPORT.md`、`reports/figures/`、`AI_USAGE.md`、`notebooks/09_midterm_chunks.ipynb` (以 11:50 的版本評分)

1. 確認 `DATA_REPORT.md` 已存檔，截圖都在 `reports/figures/` 中。
2. 在 Source Control (樹枝狀圖示) 中檢查變更清單，應該包含：
   * `DATA_REPORT.md`、`reports/figures/` 中的截圖、`AI_USAGE.md`、`notebooks/09_midterm_chunks.ipynb` (**保留輸出結果**)
3. 點擊 **[ + ]** 暫存 → 輸入訊息 `docs: 期中資料前處理報告` → **Commit** → **Sync Changes**。
4. 到 GitHub 網頁確認 `DATA_REPORT.md` 的截圖正常顯示。

---

# 繳交前檢查清單 (Final Checklist)

**11/6 11:50 前 Push** (以 11:50 的版本評分)
- [ ] `DATA_REPORT.md` 第 1–5 節完成，第 3.4 節含**驗證碼**
- [ ] 截圖在 `reports/figures/`，GitHub 上可正常顯示
- [ ] `AI_USAGE.md` 已新增 Week 09 段落
- [ ] `notebooks/09_midterm_chunks.ipynb` 已存檔，**保留輸出結果**
- [ ] 以上四項皆已 Commit & Push
