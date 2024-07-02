# Helmet Detection with YOLOv10

## Project Purpose

This project aims to develop and deploy an object detection model using the YOLOv10 architecture to identify whether a person is wearing a helmet. This model can be used in various safety applications, particularly in workplaces like construction sites.

## Project Architecture (Pipeline)

The project pipeline consists of the following steps:

1. **Data Collection**: Gathering a dataset of images with annotations indicating whether a person is wearing a helmet.
2. **Data Preprocessing**: Cleaning and preparing the dataset, including resizing images, normalization, and data augmentation.
3. **Model Training**: Training the YOLOv10 model using the preprocessed dataset.
4. **Model Evaluation**: Assessing the model's performance using metrics such as precision, recall, and mean average precision (mAP).
5. **Model Deployment**: Deploying the trained model for real-time helmet detection.

## Running the Project

To run the project locally, follow these steps:

### Prerequisites

- Python 3.x
- Required libraries: `numpy`, `pandas`, `torch`, `opencv-python`, etc.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/vinhvu512/Helmet_Safety_Detection.git
   cd Helmet_Safety_Detection
   
2. Clone the YOLOv10 repository from GitHub:
   ```bash
   git clone https://github.com/THU-MIG/yolov10.git
   cd yolov10
   pip install -q -r requirements.txt
   pip install -e .
   
### Example usage
   ```python
    from ultralytics import YOLOv10
    
    # Load a trained helmet detection YOLOv10n model
    model = YOLOv10("models/yolov10n_helmet_detection.pt")
    
    # Perform helmet detection on an image
    results = model("image.jpg")
    
    # Display the results
    results[0].show()
