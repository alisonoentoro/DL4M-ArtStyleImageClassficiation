# 🖼️ Art Style Image Classification

## 📚 Overview  
In this project, we evaluated the performance of different image classification models on **27 distinct art styles**.  
We trained and compared four models to understand how architectural choices, dataset balancing, and data augmentation affect classification outcomes.

---

## 🧠 Models Trained

- **Baseline Model**  
  A standard CNN model without any balancing or augmentation.

- **Baseline + Class Weights**  
  Same CNN model trained with class weighting to address dataset imbalance.

- **Data Augmented Model**  
  The baseline model enhanced with data augmentation techniques: horizontal flip, rotation, zoom, contrast, and translation.

- **ResNet50 Model**  
  A transfer learning model using a pre-trained ResNet50 as a feature extractor.

---

## 🖼️ Dataset

We used the **WikiArt Dataset** from Kaggle, which includes:

- **81,444 images** across **29 artists**
- For this project, we focused on **27 major art styles** to build a more balanced classification task

---

## 🧰 Key Techniques Used

- **Data Augmentation**  
  To increase dataset diversity and help prevent overfitting.

- **Class Weights**  
  Applied to mitigate class imbalance during training.

- **Transfer Learning**  
  Used ResNet50’s pre-trained capabilities for better feature extraction.

- **Early Stopping and Checkpointing**  
  To prevent overfitting and automatically save the best performing model.

---

## 🎯 Project Goals

- Understand the effect of dataset balancing using class weights  
- Investigate how augmentation improves generalization  
- Compare a custom CNN's performance with a deeper pre-trained model (ResNet50)

---

## 🧪 How to Test the Models

To evaluate the model's performance on your own images in Google Colab:

1. Upload `image1.jpg`, `image2.jpg`, and `image3.jpg` (or similar test images)
2. Run the prediction cells to see how each model performs on unseen artwork

---

## 📊 Results & Findings

- The dataset was **imbalanced**, with more samples from styles like _Realism_ and _Post-Impressionism_, which skewed learning toward these categories.
- Many styles had **subtle visual overlaps**, making it difficult for the models to identify distinct features.
- While training metrics improved, **validation accuracy often lagged**, indicating challenges with generalization.
- **Subjective labeling** of art styles introduced ambiguity and potential mislabeling, adding noise to both training and evaluation processes.
