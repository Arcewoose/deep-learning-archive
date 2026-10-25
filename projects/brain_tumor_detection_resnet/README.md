# Brain Tumor MRI Classification with Transfer Learning

Binary classification pipeline to detect brain tumors from MRI scans using pre-trained convolutional neural network backbones.

---

## 1. Problem Formulation
- **Objective**: Identify the presence of brain tumors from T1/T2-weighted brain MRI scan images.
- **Dataset**: Brain MRI binary classification dataset.
  - Class `YES` (1): Scans with confirmed tumor presence.
  - Class `NO` (0): Normal scans without tumor indications.
- **Split Strategy**: Train / Validation / Test stratified split via `split-folders`.

---

## 2. Model Architecture & Pipeline
- **Input Preprocessing**: Image resizing to $(224, 224, 3)$, normalization, and data augmentation.
- **Backbone**: **ResNet50** pre-trained on ImageNet (`include_top=False`).
- **Transfer Learning Setup**:
  - Feature extraction layers frozen (`trainable=False`) to preserve low-level visual representations.
  - Custom classification head: `Flatten()` $\rightarrow$ `Dropout(0.5)` $\rightarrow$ `Dense(1, activation='sigmoid')`.
- **Optimization**: Binary Crossentropy loss, RMSprop / Adam optimizers, monitored with accuracy and validation loss.

---

## 3. Experimental Results
- Evaluated performance across training epochs:
  - Initial ResNet50 transfer learning achieved peak **validation accuracy of 91.67%** (`val_loss: 1.0149`).
  - Compared convergence characteristics and stability against baseline CNN implementations.
