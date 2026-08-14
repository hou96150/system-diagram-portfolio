# System Diagram Portfolio｜系統架構圖作品集

這是一組以真實專案程式碼與資料流程為依據的互動式 HTML 系統圖。每張圖都是單一、自包含、可離線開啟的檔案，並針對 16:9 畫面設計。

## 圖表清單

### Smart Pet Collar｜寵物智慧項圈

- [系統架構圖](https://hou96150.github.io/system-diagram-portfolio/outputs/smart-pet-collar-system-architecture.html)：邊緣辨識、後端事件、即時監控與硬體邊界。
- [模型訓練管線](https://hou96150.github.io/system-diagram-portfolio/outputs/smart-pet-collar-training-pipeline.html)：資料集、切分、特徵、模型與部署產物。
- [即時辨識時序圖](https://hou96150.github.io/system-diagram-portfolio/outputs/pet-collar-realtime-recognition-sequence.html)：音訊收集、邊緣推論、後端權威風險與 SSE 更新。
- [離線補送流程圖](https://hou96150.github.io/system-diagram-portfolio/outputs/pet-collar-offline-resend-flow.html)：SQLite FIFO、ACK 後刪除與 `clientEventId` 冪等去重。

### TOEIC AI Learning System

- [單字資料生命週期](https://hou96150.github.io/system-diagram-portfolio/outputs/toeic-vocabulary-data-lifecycle.html)：Drive／OCR 匯入、`pending` 人工審核閘門與 `approved` 正式字卡。

### Spectrum Detective

- [訊號分析學習管線](https://hou96150.github.io/system-diagram-portfolio/outputs/spectrum-detective-signal-analysis.html)：固定 seed 合成 RF frame、頻譜／瀑布判讀、證據計分與 Markdown 報告。

## 驗證與誠實邊界

- 6 個 HTML 均通過 diagram-design 自包含檢查。
- 本次新增的 4 張圖均以 1280 × 720 真實瀏覽器渲染，Console 為 0 error／0 warning。
- Spectrum Detective 圖明確標示為合成資料；目前不是 SDR 實測、IQ 匯入或 FFT 管線。
- 寵物項圈的軟體整合流程已對照實作；樹莓派蜂鳴器與實機耐候仍屬硬體待驗證範圍。
- TOEIC 的 OCR 匯入資料不會直接成為正式字卡，必須先經人工審核與明確核准。

直接開啟 [作品集首頁](https://hou96150.github.io/system-diagram-portfolio/)，或從上方連結逐張查看完整圖。

---

## English

This repository contains self-contained HTML diagrams grounded in the actual code and data flows of three working projects. The six diagrams cover smart-pet-collar architecture, training, runtime sequencing, offline delivery, the TOEIC vocabulary review lifecycle, and Spectrum Detective's deterministic synthetic-RF learning pipeline.

The diagrams intentionally preserve implementation limits: Spectrum Detective does not claim live SDR capture or an IQ-to-FFT path; imported TOEIC vocabulary remains pending until explicit human approval; smart-collar hardware validation is kept separate from verified software behavior.
