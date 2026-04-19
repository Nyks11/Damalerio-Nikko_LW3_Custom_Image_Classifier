# Damalerio-Nikko_LW3_Custom_Image_Classifier

## Guide Questions – Student Reflection & Explanation

### 1. Dataset Preparation

**How did you organize your dataset in Google Drive?**
The dataset was organized by creating a main folder named `ImageDataset`. Each plant category had its own subfolder (e.g., Rose, Sunflower, Tulip), and each subfolder contained all images for that specific class.

**Why is folder structure important for TensorFlow image loading?**
The folder structure is important because TensorFlow uses the subfolder names as labels for classification. This allows the system to automatically assign the correct label to each image without manual labeling.

---

### 2. Model Training

**What is the role of convolutional layers in image classification?**
Convolutional layers extract important features from images, such as edges, shapes, and textures, which are used by the model to distinguish between different classes.

**Why do we split data into training and validation sets?**
Splitting the data ensures that the model is trained on one set of images and evaluated on a separate set. This allows us to measure how well the model generalizes to new, unseen data and helps prevent overfitting.

---

### 3. Performance Analysis

**What accuracy did your model achieve?**
The model achieved a validation accuracy of approximately **[insert your accuracy here]**.

**How did the number of images affect the model’s performance?**
A larger number of images improves model performance by providing more examples for learning, helping the model generalize better. With fewer images, the model may overfit or have lower accuracy.

---

### 4. Critical Thinking

**What challenges did you encounter while using your own dataset?**
Challenges included:
- Collecting enough images for each class
- Ensuring image quality and consistency
- Handling mislabeled or incorrect images
- Long training times for large datasets

**How can data augmentation improve your model?**
Data augmentation increases the diversity of the dataset by applying transformations such as flipping, rotation, and zooming. This helps the model generalize better and reduces overfitting.

---

### 5. Application

**Suggest a real-world application for your trained model.**
A practical application is a plant identification system where users can upload a photo of a plant and receive its name. This can be useful for gardeners, farmers, students, or botanists.

**How can this system be integrated into a mobile or web application?**
The trained model can be deployed on a server or converted into a mobile-friendly format. A mobile or web app can allow users to upload images, send them to the model for prediction, and display results along with confidence scores.

---

## Activity 3A: Improving and Evaluating a Custom Image Classifier

### Visualization & Overfitting

**1. What signs indicated overfitting in your first model?**
Overfitting was indicated when the training accuracy continued to increase while the validation accuracy stopped improving or started to decrease. Additionally, there was a noticeable gap between training and validation accuracy, showing that the model was performing well on training data but poorly on unseen data.

**2. How did data augmentation affect validation accuracy?**
Data augmentation improved validation accuracy by providing more varied training examples. This helped the model generalize better to unseen data, resulting in more stable and often higher validation performance.

---

### Model Improvement

**3. What is the purpose of dropout layers?**
Dropout layers are used to reduce overfitting by randomly disabling a portion of neurons during training. This prevents the model from relying too heavily on specific features and encourages it to learn more general patterns.

**4. Why does data augmentation improve generalization?**
Data augmentation improves generalization by exposing the model to different variations of the same images, such as rotated or flipped versions. This allows the model to learn more robust features and perform better on new, unseen data.

---

### Performance Comparison

**5. Compare accuracy before and after improvements.**
Before applying improvements, the model showed higher training accuracy but lower validation accuracy, indicating overfitting. After applying data augmentation and dropout, the validation accuracy improved and became closer to the training accuracy, showing better generalization.

**6. Which technique contributed most to improvement?**
Data augmentation contributed the most to improvement because it effectively increased the diversity of the dataset. This allowed the model to learn from more variations and reduced overfitting more significantly.

---

### Deployment & Application

**7. Why is saving the model important?**
Saving the model is important because it allows the trained model to be reused without retraining. This saves time and computational resources and makes it possible to deploy the model in real-world applications.

**8. How can this model be deployed in a real-world system?**
The model can be deployed by integrating it into a web or mobile application. The trained model can be hosted on a server or converted into a lightweight format for mobile devices. Users can upload images, and the system will process the image, run it through the model, and return the predicted class along with confidence scores.