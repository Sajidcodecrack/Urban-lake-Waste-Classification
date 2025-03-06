# Urban Lake Waste Classification

## Introduction
Urban lakes in Dhaka city are heavily polluted with various types of waste, significantly impacting the environment and aquatic life. To address this issue, we developed a deep learning model to classify and categorize waste found in these lakes. This project involves building a customized dataset and training a YOLOv8-based model to identify different waste types.

## Objective
The main goal of this project is to create an efficient classification model that can accurately identify waste types in urban lakes, thereby aiding in waste management and cleanup efforts.

## Waste Categories
Our deep learning model classifies lake waste into the following categories:
- **Plastic Waste**
- **Paper Waste**
- **Rubber Waste**
- **Organic Waste**

## Dataset Preparation
We collected and annotated **777 images** of lake waste from various sources, ensuring diversity in lighting conditions, angles, and environmental factors. The dataset was manually labeled and preprocessed for training.

### Data Augmentation
To improve model generalization, we applied the following data augmentation techniques:
- **Rotation**
- **Flipping**
- **Brightness adjustment**
- **Gaussian noise addition**

## Model Architecture
We used **YOLOv8 (You Only Look Once)** as the object detection and classification model due to its efficiency in real-time waste detection. The architecture was fine-tuned using our customized dataset.

### Training Parameters
- **Batch Size**: 16
- **Epochs**: 50
- **Optimizer**: Adam
- **Learning Rate**: 0.001
- **Loss Function**: Cross-Entropy Loss

## Evaluation Metrics
Despite facing challenges with accuracy, we focused on multiple performance metrics to evaluate the model:

### Confusion Matrix
A confusion matrix was used to visualize the classification performance for each waste category, highlighting correct and misclassified instances.

### F1 Score
To assess the balance between precision and recall, we calculated the F1 Score for each class:

| Waste Category | Precision | Recall | F1 Score |
|---------------|------------|---------|---------|
| Plastic | 0.78 | 0.80 | 0.79 |
| Paper | 0.74 | 0.76 | 0.75 |
| Rubber | 0.65 | 0.70 | 0.67 |
| Organic | 0.81 | 0.78 | 0.79 |

## Challenges Faced
- **Limited Dataset**: Due to the relatively small dataset, achieving higher accuracy was challenging.
- **Class Imbalance**: Some waste types were underrepresented in the dataset, affecting classification performance.
- **Real-world Variability**: Environmental factors such as lighting and water reflections impacted detection quality.

## Future Improvements
To enhance the model's performance, we plan to:
- **Expand the dataset** by collecting more images from various urban lakes.
- **Improve data balancing** by augmenting underrepresented waste categories.
- **Experiment with other architectures** such as EfficientDet or Swin Transformer.
- **Deploy the model** in a real-world system integrated with a mobile/web-based application for waste monitoring.

## Conclusion
This project is a step towards improving waste classification in Dhaka's urban lakes. While the current model provides promising results, further refinements and dataset expansion can significantly enhance its effectiveness. By leveraging deep learning, we aim to contribute to a cleaner and more sustainable environment.

---

### Repository Structure
```
Urban-lake-Waste-Classification/
│── dataset/                # Annotated images and labels
│── models/                 # Trained YOLOv8 model weights
│── scripts/                # Training and evaluation scripts
│── results/                # Performance reports and metrics
│── README.md               # Project documentation
```

### Acknowledgments
We appreciate the efforts of the team in data collection, annotation, and model training. Special thanks to contributors who helped refine this project.

