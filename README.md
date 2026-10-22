# 雙城選舉公開預測

這個儲存庫是 2026 年台北市與新北市市長選舉最新預測結果的公開彙整。它不是完整的應用程式或模型程式碼庫，而是報告層：一份簡潔、可檢視、可分享的預測輸出匯總。

目標很簡單：讓模型輸出更透明、容易檢視，也更容易分享。若你正在瀏覽這個儲存庫，你應該能在一眼之內理解模型當前的判讀與預測重點。

## 這裡在做什麼

這裡的輸出來自階層式貝葉斯狀態空間預測模型，將民調資料整合起來、平滑未表態選民，並估計候選人獲勝機率與不確定性範圍。

換句話說：這是一份精簡且公開的選舉預測紀錄，而不是競選資料庫，也不是具營運功能的軟體產品。

## 先看哪些內容

先從簡明的預測摘要開始：

- `results/Taipei_NewTaipei_fb_post.txt` — 最新的社群貼文風格更新，包括候選人百分比、不確定性區間，以及對模型的簡短說明

接著打開視覺化輸出：

- `results/Taipei_forecast_dashboard.png` — 台北市預測儀表板
- `results/NewTaipei_forecast_dashboard.png` — 新北市預測儀表板
- `results/Taipei_Retrospective_vs_Actual_Polls.png` — 台北市對照歷史民調與實際結果的回溯檢視
- `results/NewTaipei_Retrospective_vs_Actual_Polls.png` — 新北市對照歷史民調與實際結果的回溯檢視

最後，確認發布時間戳記：

- `results/published_at_utc.txt` — 最新預測發布的 UTC 時間戳記

## 如何閱讀這些輸出

1. 先閱讀文字摘要。它提供最新預測最精簡的解讀。
2. 打開各城市的預測儀表板，查看城市層級視覺與模型估計結果。
3. 檢視回溯圖，了解模型歷史適配情況與穩定性。
4. 參考時間戳記，理解預測產生時點與選舉時間軸的關聯。

## 為什麼存在這個儲存庫

這個儲存庫作為模型輸出的透明、可分享彙整。它適合讀者：

- 在不深入程式碼的情況下看見最新預測
- 檢視模型隨時間變化的行為
- 理解當前估計與歷史驗證快照之間的差異
- 以乾淨、易讀的方式分享結果

## 注意事項

這些是為公共利益與探索性分析所產生的預測輸出。它們不是官方選舉結果，應被視為某一特定時間點下機率模型的快照���

## 儲存庫結構

```text
.
├── .gitkeep
└── results/
    ├── Taipei_forecast_dashboard.png
    ├── NewTaipei_forecast_dashboard.png
    ├── Taipei_Retrospective_vs_Actual_Polls.png
    ├── NewTaipei_Retrospective_vs_Actual_Polls.png
    ├── Taipei_NewTaipei_fb_post.txt
    └── published_at_utc.txt
```

如果你是第一次造訪這個儲存庫，最好的閱讀路徑是：先打開文字摘要，再查看儀表板，最後檢視回溯驗證圖表，從中體會預測模型的整體表現與歷史穩定性。
