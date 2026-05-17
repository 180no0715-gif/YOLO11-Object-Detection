# 基於 YOLO 之宿舍常見容器辨識系統

本專案以 YOLO 物件辨識模型為核心，
透過自行蒐集與標註宿舍常見容器影像，
建立即時容器辨識系統。

系統可辨識 Bottle、Can、Cup noodle、Snack 等類別，
並整合攝影機串流進行即時推論。

## 專案流程

1. 自行拍攝宿舍常見容器照片
2. 使用 Label Studio 進行資料標註
3. 輸出 YOLO 格式資料集
4. 於 Google Colab 進行模型訓練
5. 使用 OpenCV 整合攝影機串流
6. 於本地端環境進行即時辨識

## 使用技術

- Python
- YOLOv11
- OpenCV
- Google Colab
- Label Studio
- Anaconda

## 資料集

資料集由本人自行拍攝，
包含宿舍常見飲料與食品容器影像，
並透過 Label Studio 完成標註。

類別包含：
- Bottle
- Can
- Cup noodle
- Snack

## 模型問題分析

目前 Snack 類別辨識率較低，
推測與樣本數不足及背景干擾有關。

後續規劃：
- 增加資料量
- 導入資料增強
- 加入負樣本訓練

## 未來優化方向

- 增加更多容器類別
- 提升低光源辨識能力
- 導入 Raspberry Pi 部署

## 🚀 技術亮點
- **雲端運算**：利用 Google Colab 與 NVIDIA GPU 進行大規模迭代訓練。
- **自動化備份**：設計核心資產備份腳本，實現 Google Drive 持久化存儲。
- **本地端部署**：透過 Anaconda 建立 Python 3.12 隔離環境，並利用 CUDA 加速影像推論。

## 📂 檔案說明
- `goat.ipynb`: 雲端開發與模型訓練完整歷程。
- `yolo_detect.py`: 本地端實時影像偵測與標註腳本。
- `train_val_split.py`: 自動化資料集分割工具。
- `results.png`: 模型訓練成績單與損失函數曲線。
