# 甲狀旁腺報告產生器

這是一個用於生成甲狀旁腺掃描報告的網頁工具。

## 功能

- 快速選擇甲狀旁腺部位和放射性活性級別
- 自動生成標準化的 Findings 和 Impression 文本
- 支持跨域通信，可嵌入在其他系統中使用
- 支持數據導入/導出功能

## 使用方法

1. 在表格中選擇需要報告的部位和對應的放射性活性
2. 系統會自動生成報告內容
3. 使用「Copy Findings」和「Copy Impression」按鈕複製相應報告段落
4. 或使用「Export Table Data」按鈕導出表格數據

## 跨域通信接口

支持通過 postMessage 與父頁面進行跨域通信：

### 從報告產生器傳出的訊息:
- `parathyroidReport`: 包含 findings 和 impression 的報告內容
- `parathyroidTableData`: 包含表格數據的導出內容

### 支持接收的指令:
- `clearTable`: 清空表格
- `copyFindings`: 複製 Findings
- `copyImpression`: 複製 Impression
- `getReports`: 獲取當前報告內容
- `importData`: 匯入表格數據
- `exportData`: 導出表格數據 