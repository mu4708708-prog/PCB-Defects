# PCB Defect Data using Deep Learning 

This project is a **Deep Learning-based PCB Defect Classification System** designed to automatically identify manufacturing defects in Printed Circuit Boards (PCB) from image data. The system uses custom CNN and ResNet-style architectures to classify multiple PCB defect categories with high accuracy.

---

## Dataset Structure

<pre>
pcb_defect_detection.ipynb
PCB_DATASET/
│
├── images/
│   ├── Missing_hole/
│   ├── Mouse_bite/
│   ├── Open_circuit/
│   ├── Short/
│   ├── Spur/
│   └── Spurious_copper/
│
├── rotation/
│   └── Augmented / Rotated Images
│
└── PCB_USED/
    └── Metadata / Supporting Files
</pre>

---

## Download Dataset

Due to GitHub file size limitations, the dataset can be downloaded separately from Kaggle:

🔗 **Dataset Link:**
https://www.kaggle.com/datasets/akhatova/pcb-defects

After downloading, place the dataset folder in your project root directory so the structure matches the one shown above.

---

## Technologies Used

* Python 3
* PyTorch
* Torchvision
* OpenCV
* NumPy
* Pandas
* Matplotlib / Seaborn
* Scikit-learn
* Google Colab

---

## Model Architectures

### Custom CNN

* `Conv2D (32 Filters)` → `BatchNorm` → `ReLU` → `MaxPool`
* `Conv2D (64 Filters)` → `BatchNorm` → `ReLU` → `MaxPool`
* `Conv2D (128 Filters)` → `BatchNorm` → `ReLU`
* `Conv2D (256 Filters)` → `BatchNorm` → `ReLU`
* `Conv2D (512 Filters)` → `BatchNorm` → `ReLU`
* `Global Average Pooling`
* `Dense Layer`
* `Dropout (0.4)`
* `Softmax Output`

### ResNet PCB

* Residual Blocks with Skip Connections
* Projection Shortcuts (1×1 Conv)
* Adaptive Global Average Pooling
* Fully Connected Output Layer

---

## Model Performance

| Model      | Accuracy   | Precision | Recall | F1-Score | Macro AUC  |
| ---------- | ---------- | --------- | ------ | -------- | ---------- |
| Custom CNN | 98.10%     | 0.9721    | 0.9810 | 0.9763   | 0.8422     |
| ResNet PCB | **98.10%** | 0.9721    | 0.9810 | 0.9763   | **0.8682** |

---

## Training Visualizations

Training and validation graphs were plotted to monitor:

* Accuracy vs Epochs
* Loss vs Epochs
* Overfitting / Underfitting Trends

Additional Visualizations:

* Grad-CAM Heatmaps
* Confusion Matrix
* ROC Curves
* Filter Visualization

---

## Evaluation

Final model performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

Early stopping and regularization were used to improve generalization.

---

## Run Notebook

The complete implementation is available in:

 **`pcb_defect_detection.ipynb`**

Ensure dataset paths are updated correctly before running.

---

## Notes

* Input Image Size: `224x224`
* Dataset Augmentation Applied
* GPU Recommended for Training
* Best Model Saved During Training

---

## 📬 Author

Built by **Muhammad Uzair** as part of **CS4059 – Fundamentals of Computer Vision**

---
