# Multiple Linear Regression Explorer (多元線性回歸分析平台)

> 基於 CRISP-DM 流程設計的多元線性回歸（Multiple Linear Regression）與特徵選擇（Feature Selection）互動式探索平台原型。

---

## 📌 專案簡介 (Overview)

本專案為一個可在瀏覽器中直接開啟、操作的純前端互動原型。以多元線性回歸為核心，結合特徵工程與模型簡潔性（Model Parsimony）評估，幫助使用者直觀比較不同特徵選擇方法下的模型表現、回歸方程式係數與殘差診斷。

---

## 🌟 核心功能 (Key Features)

### 1. 🗂️ Dataset 下拉選單切換
- **內建經典資料集**：
  - **Kaggle 50 Startups**：藉由研發、行銷、行政支出等商業數據預測新創公司利潤（Profit）。
  - **Boston Housing**：利用房間數（RM）、低所得比例（LSTAT）等環境與社區屬性預測房價中位數（MEDV）。
- **Custom Dataset**：支援切換至自訂資料集模式，介面說明與預測變數欄位將動態更新。

### 2. ⚙️ 自訂 Dataset 配置
- **彈性參數輸入**：可自行輸入資料集名稱、特徵數量（Features count）以及目標變數（Target variable, Y）。
- **CSV 上傳介面**：提供 CSV 檔案選取介面（目前原型版本為 UI 佔位，提示尚未連接後端模型訓練）。

### 3. 📊 回歸分析 Dashboard 與特徵選擇
- **5 種特徵選擇演算法切換**：
  - **Lasso**（L1 正則化篩選）
  - **Forward SFS**（前向逐步特徵選擇）
  - **RFE**（遞歸特徵消除）
  - **ElasticNet**（彈性網路）
  - **Exhaustive Search**（窮舉搜尋）
  - **Compare all methods**（多演算法綜合比較）
- **模型複雜度調整 ($k$ 值)**：可自由切換選取特徵數 $k = 1 \sim 5$，觀察模型在簡潔度與預測力之間的最佳平衡點（Sweet Spot）。
- **多維評估指標**：
  - **Test RMSE**（均方根誤差，越低越好）
  - **$R^2$ Score**（決定係數，反映模型解釋變異度）
  - **Adjusted $R^2$**（校正決定係數，懲罰過多不必要的特徵變數）
  - **MAE**（平均絕對誤差）
  - **F-statistic**（整體迴歸模型顯著性檢定）
- **動態趨勢圖表**：即時繪製 RMSE 與 $R^2$ 隨特徵數量變化的折線趨勢圖。

### 4. 🧮 迴歸方程式與統計推論檢定
- **Fitted OLS Equation**：即時呈現擬合之多元線性回歸方程式。
- **係數檢定表**：顯示各預測變數的迴歸係數 ($\beta$)、標準誤（Std. Error）、$t$ 統計量、$p$-value、95% 信賴區間與共線性診斷（VIF）。

### 5. 🎛️ 即時預測計算機 (Live Prediction Calculator)
- 透過滑桿或數值輸入欄位微調特徵數值（如研發費用、行銷支出），即時計算並動態呈現預測結果。

### 6. 🔍 殘差與異常值診斷 (Residuals & Diagnostics)
- 提供測試集殘差診斷表格，追蹤實際值、預測值、殘差、絕對誤差百分比及異常標籤。

---

## 🛠️ 技術架構 (Tech Stack)

- **前端技術**：純原生 HTML5、CSS3、Vanilla JavaScript（無第三方大型依賴，極速載入）。
- **視覺化呈現**：原生響應式 SVG 圖表繪製。
- **方法論架構**：CRISP-DM 跨產業資料探勘標準流程。
- **響應式佈局 (RWD)**：支援桌機、平板與行動裝置操作。

---

## 📂 檔案目錄架構 (Repository Structure)

```text
1014/
├── index.html                          # GitHub Pages 預設首頁入口
├── regression_dataset_explorer.html    # 多元線性回歸分析平台主頁面
└── README.md                           # 專案詳細說明文件
```

---

## 🚀 如何使用 (Quick Start)

### 1. 本地開啟
直接在瀏覽器中連點開啟 [`regression_dataset_explorer.html`](regression_dataset_explorer.html) 或 [`index.html`](index.html) 即可開始操作。

### 2. 線上展示 (GitHub Pages)
若已在 GitHub Repository 的 **Settings $\rightarrow$ Pages** 啟用部署，可透過以下網址直接在線體驗：
- 👉 [線上展示平台 (GitHub Pages)](https://timko1018.github.io/1014/)

---

## 🔗 參考與誌謝 (References)

- **設計靈感參考**：[50 Startups Multiple Linear Regression Explorer](https://huanchen1107.github.io/AIoT-DIC2-MultipleLR/)
- **範例資料集**：Kaggle 50 Startups & Boston Housing Dataset
