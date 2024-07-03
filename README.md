# Brain Tumour Classifier

## Description

This project is a Brain Tumour Classifier built using TensorFlow Lite and Streamlit. It allows users to upload MRI scans to determine the type of brain tumour present. The classifier categorizes tumours into types such as pituitary, glioma, meningioma, or determines if no tumour is detected.

## Demo


https://github.com/Nithin1729S/Brain-Tumor-Classification/assets/78496667/45e0de43-15cf-4be4-a97c-88b42fcba074





 ## Screenshots
![Screenshot from 2024-07-04 03-32-03](https://github.com/Nithin1729S/Brain-Tumor-Classification/assets/78496667/623b1a92-dec5-4e81-b213-0c21a26430af)
![Screenshot from 2024-07-04 03-33-40](https://github.com/Nithin1729S/Brain-Tumor-Classification/assets/78496667/16a19c15-187e-4814-b852-2275fb17b4ee)

 
[Watch the Demo Video on YouTube](https://youtu.be/8CGXEmEt4Sc)
## Technologies Used

- Python
- TensorFlow Lite
- Streamlit
- SQLite

## Features

- Upload an MRI scan to classify brain tumours.
- Provides immediate prediction results based on uploaded images.
- Sidebar with information about brain tumours, symptoms, and health advice.
- SQLite database integration to store prediction results.
  
## How the Model Was Trained

### 1. Data Collection and Preparation

The dataset consists of MRI scan images categorized into different classes (pituitary, notumor, glioma, meningioma). Training and testing datasets were prepared with a distribution as follows:

Training Set:
pituitary: 1457
notumor: 1595
glioma: 1321
meningioma: 1339

Testing Set:
pituitary: 300
notumor: 405
glioma: 300
meningioma: 306


### 2. Data Augmentation

Images were augmented to increase the diversity of the training set using techniques such as rotation, flipping, and zooming.

### 3. Model Architecture

The model used transfer learning with MobileNetV2 as the base model, pretrained on ImageNet. The final layers were adjusted for the specific classification task:

- MobileNetV2 base with frozen layers
- Additional dense layers for classification

### 4. Training

The model was compiled with Adam optimizer and trained for 20 epochs. Training and validation accuracies were monitored using callbacks for early stopping and model checkpointing.

### 5. Evaluation

The trained model achieved the following performance on the test set:

- Test Loss: 0.299
- Test Accuracy: 93.3%

### 6. Model Deployment

The trained model was saved in HDF5 format (`model.h5`) and its architecture in JSON format (`brain_model.json`) for deployment.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Brain-Tumour-Classifier.git
   
2. Install Dependencies:
   ```bash
   pip install -r requirements.txt
3. Run the application:
   ```bash
   streamlit run app.py


   
