
# 🩸 Blood Group Prediction Using Fingerprints

This project aims to predict human blood groups using fingerprint images through deep learning techniques.
It uses the **ResNet152** architecture with transfer learning to classify fingerprint images into one of the eight blood group types.

## 📁 Dataset

- **Source**: Kaggle
- **Path**: `/kaggle/input/finger-print-based-blood-group-dataset`
- **Classes**:
  - A+
  - A−
  - B+
  - B−
  - AB+
  - AB−
  - O+
  - O−

## 🧰 Technologies Used

- Python
- TensorFlow & Keras
- ResNet152
- Kaggle Notebooks
- ImageDataGenerator for data augmentation

## 🧪 Model Details

- **Base Model**: ResNet152 (without top layers)
- **Input Shape**: 224x224 RGB
- **Top Layers**: Flatten → Dense (activation='relu') → Dense(8, activation='softmax')
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam (learning rate = 0.0001)
- **Metrics**: Accuracy

## 🏋️‍♀️ Training

```python
model.compile(optimizer=Adam(learning_rate=0.0001),
              loss='categorical_crossentropy',
              metrics=['accuracy'])

history = model.fit(train_generator,
                    validation_data=val_generator,
                    epochs=10)
```

## 📈 Results

- The model was trained over 20 epochs.
- Accuracy and loss graphs were generated to visualize model performance.


## 🚀 Running the Project

To run this project:

1. Clone this repository.
2. Install dependencies.
3. Run the notebook using Jupyter.

```bash
git clone https://sneha3210.github.io/minor-project/
cd blood-group-prediction
pip install -r requirements.txt
jupyter notebook minor.ipynb
```
## 📌 Notes

- If the project includes errors from initial development, you can:
  - Keep the repository **private** initially.
  - Add proper comments and clean the code over time.
## 📜 License

This code is licensed for personal, educational use only.  
Modification, redistribution, or commercial use is strictly prohibited without prior written consent from the author.  
© 2025 Sneha

