# Image-Classification-and-Analysis-Using-Deep-Learning-Methods
This project built an image classifier using ResNet-50 (PyTorch) to categorize Amazon products into three classes. While achieving 91.67% training accuracy, test performance dropped to 41.67%, suggesting overfitting. Evaluation revealed poor results on Digital_Music. Solutions include more data and model optimization.

This project developed a PyTorch-based image classifier using ResNet-50 to categorize Amazon product images into three classes: All_Beauty, Digital_Music, and Health_and_Personal_Care. Key findings:

Performance:
Training accuracy: 91.67%
Test accuracy: 41.67% (indicating overfitting)
Digital_Music classification failed completely
Technical Approach:
Transfer learning with ResNet-50
Standard image preprocessing (resizing, augmentation)
CrossEntropy loss with Adam optimizer
Identified Issues:
Significant overfitting
Poor generalization on test set
Complete failure on Digital_Music category
Recommended Improvements:
Dataset expansion
Enhanced augmentation techniques
Model architecture adjustments
Class imbalance mitigation
The project demonstrates the challenges of applying transfer learning to limited datasets while highlighting the importance of proper model evaluation and validation techniques.
