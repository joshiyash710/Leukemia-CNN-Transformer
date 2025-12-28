Leukemia Classification Using Hybrid CNN–Transformer

This project focuses on automated detection of leukemia from microscopic blood smear images using a hybrid deep learning architecture. The model combines the strengths of Convolutional Neural Networks (CNNs) for local feature extraction with Transformer encoders to capture global contextual relationships within the image.

By leveraging this hybrid approach, the system can accurately differentiate between leukemia (ALL) and normal hematopoietic cells. The model is trained and validated using k-fold cross-validation, ensuring robust performance and generalization. Additionally, hyperparameter optimization is performed using Optuna to identify the best configuration for backbone selection, learning rate, image size, and transformer parameters.

The final solution provides:

High-accuracy classification of leukemia vs. normal samples.

Ensemble predictions from multiple trained folds for more reliable results.

Confidence scores to identify low-confidence samples, enabling further review.

This approach demonstrates how advanced deep learning techniques can be applied to medical image analysis to support faster and more reliable diagnostic workflows in hematology.
