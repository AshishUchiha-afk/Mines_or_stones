# Mines_or_stones
A binary classification project to detect whether a sonar signal reflects off a mine or a rock using machine learning.

## ⚙️ How to Run the Code Without Hassle in google colab

Follow the steps below to get started easily:

1. 📥 **Run the following cell in the notebook:**

   ```python
   from google.colab import files
   files.upload()
2.🔐 Upload your Kaggle token (kaggle.json) when prompted.

3.✅ Now the code is ready to run — all necessary permissions and access will be set up!

## ⚙️ How to Set Up the Project Locally (Kaggle API Method)

Follow these steps if you want to use the Kaggle API to download the dataset directly:

1. 🔑 **Get Your Kaggle API Credentials**  
   - Go to your [Kaggle Account Settings](https://www.kaggle.com/account)
   - Click on **"Create New API Token"**
   - This will download a file called `kaggle.json`

2. 📁 **Place the Token File**  
   - Move `kaggle.json` to the `.kaggle` folder:
     - On Windows: `C:\Users\<YourUsername>\.kaggle\kaggle.json`
     - On macOS/Linux: `~/.kaggle/kaggle.json`

3. 🧠 **Use the Following Code to Programmatically Download the Dataset**

   ```python
   import os
   import kaggle

   # Set Kaggle credentials (optional if kaggle.json is correctly placed)
   os.environ['KAGGLE_USERNAME'] = 'your_username'
   os.environ['KAGGLE_KEY'] = 'your_key'

   # Download and unzip the dataset
   kaggle.api.dataset_download_files('dataset', path='.', unzip=True)
---

## 📌 Project Highlights

- ⚙️ Binary classification: **Mine (1)** or **Rock (0)**
- 🧼 Data preprocessing, scaling, and label encoding
- 🧠 Trained using models like Logistic Regression, SVM, and Random Forest
- 📊 Model evaluation using accuracy score and confusion matrix
- 💾 Saves the trained model for real-time prediction use

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Pickle

---

## 📁 Project Structure

Mines_or_stones/
├── Mines_or_stones.ipynb → Main Jupyter notebook
├── sonar.csv → Dataset file
├── mines_model.pkl → Saved trained model
└── README.md → Project documentation

---

## 📈 Evaluation Metrics

- Accuracy Score
- Confusion Matrix
- Classification Report

---

## 🔍 Dataset Info

- **60 features** representing sonar signal strength at various angles
- **Target**:  
  - `M` = Mine  
  - `R` = Rock (converted to 1 and 0 in preprocessing)

---

## 📌 Future Improvements

- Add hyperparameter tuning with GridSearchCV
- Deploy model using Streamlit or Flask for real-time input and predictions
- Explore additional classifiers like XGBoost

---
