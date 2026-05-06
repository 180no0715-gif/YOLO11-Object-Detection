# YOLO11-Object-Detection
基於 YOLO11s 之實時物件偵測系統，包含雲端訓練腳本與本地部署實作。
# YOLO11-Object-Detection 專案

本專案為大一資管系學生之實作作品，旨在實現從雲端訓練到本地端實時部署的完整 AI 物件偵測流程。

## 🚀 技術亮點
- **雲端運算**：利用 Google Colab 與 NVIDIA GPU 進行大規模迭代訓練。
- **自動化備份**：設計核心資產備份腳本，實現 Google Drive 持久化存儲。
- **本地端部署**：透過 Anaconda 建立 Python 3.12 隔離環境，並利用 CUDA 加速影像推論。

## 📂 檔案說明
- `goat.ipynb`: 雲端開發與模型訓練完整歷程。
- `yolo_detect.py`: 本地端實時影像偵測與標註腳本。
- `train_val_split.py`: 自動化資料集分割工具。
- `results.png`: 模型訓練成績單與損失函數曲線。
