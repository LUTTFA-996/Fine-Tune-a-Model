# Fine-Tune-a-Model
This project focuses on fine-tuning a pre-trained Convolutional Neural Network (CNN) for age group classification using the UTKFace Dataset.
# The goal was to categorize face images into five broader age bins (wider bins):
- Child (0-12 years)
- Teenager (13-19 years)
- Adult (20-39 years)
- Middle-to-Older Adult (40-59 years)
- Senior (60+ years)
- The model was evaluated based on accuracy and per-class performance.
- No GUI was required for this project.
# Dataset: UTKFace Age Dataset
# 1. Data Loading
- Loaded images from the UTKFace directory.
- Extracted age labels from filenames.
* 2. Age Binning
- Mapped continuous ages into wider categorical bins (Child, Teenager, Adult, etc.).
- Used a Python function for mapping.
# 3. Data Preprocessing
- Resized all images to 128x128 pixels.
- Normalized pixel values to range [0,1].
- Applied data augmentation (horizontal flips, zoom, rotation).
# 4. Model Building (Transfer Learning)
- Used MobileNetV2 (pre-trained on ImageNet) as the base CNN.
- Froze base layers to prevent overfitting.
- Added a custom classification head (Dense layers) for our 5 age classes.
# 5. Model Training (Fine-tuning)
- Used Adam optimizer with a low learning rate.
- Loss Function: Sparse Categorical Crossentropy
- Evaluation Metric: Accuracy
- Training done for 20 epochs.
# 6. Evaluation Metrics
* Overall Accuracy: ~71% on test set
# Generated Confusion Matrix
- Per-class Precision, Recall, F1-Score
