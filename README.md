# Traffic Signs Detection

## Problem Statement
In urban environments, efficient routing/transport of goods is a huge problem. To solve that problem we are creating a computer vision-based that can solution that can analyze images of roadways to detect and classify stationary objects. We are solving the small chunk of large problem statement.

This project involves the detection and classification of traffic signs using the YOLOv9 (You Only Look Once version 9) object detection model. YOLOv9 is a state-of-the-art object detection algorithm that excels in both speed and accuracy, making it ideal for real-time applications such as autonomous driving and traffic monitoring.

## Features
- Real-time traffic sign detection
- High accuracy and low latency
- Uses advanced deep-learning techniques for object detection

## Dataset
Two types of dataset
1. Only sign dataset (Easily available)
2. Signs with background (Actual on images with curation)
    1. Vietnam traffic signs (duplicate data)
    2. Moroccan traffic signs ( less data, Arabic )
    3. Kaggle has a Google Map screenshot dataset [Link]([https://markdownlivepreview.com/](https://www.kaggle.com/datasets/raduoprea/traffic-signs))

| Dataset | Image Count |
|---|---|
| Train Data | 3253 (74.25%)
| Test Data | 628 (14.33%)
| Val Data | 500 (11.41%) 

![dataset distribution](/images/data_distribution_visualise.png "data_distribution_visualise")

![sample dataset](/images/data_sample.png "sample dataset")

## Performance Metrics
![Performance Metrics](/images/accuracy_calculation.png "accuracy_calculation")

<b>True Positive:
A correctly detected traffic sign with the correct label.

False Positive:
A detected traffic sign that is incorrectly labeled.

False Negative:
A traffic sign that was missed by the detector.
</b>

- **Intersection over Union (IoU):** IoU is a measure of the overlap between the predicted bounding box and the ground truth bounding box. It is calculated as the area of the intersection divided by the area of the union of the two boxes. A higher IoU indicates better performance.
  
- **Precision:** Precision is the ratio of true positive detections to the total number of detections made. It indicates how many of the detected signs are actually correct.
  
  Precision = True Positives / True Positives + False Positives

- **Recall:** Recall is the ratio of true positive detections to the total number of actual signs. It indicates how many of the actual signs were correctly detected.
  
  Recall = True Positives / True Positives + False Negatives

- **F-Score:** The F-Score is the harmonic mean of precision and recall, providing a single metric that balances both precision and recall.
  
  F1 = 2 * (Precision * Recall) / (Precision + Recall)

## F1 Score Comparision
- V1 is Uncooked Model (Half Train)
- V2 is a fully trained model 
![Performance Metrics](/images/accuracy_comparision.png "accuracy_comparision.png")


#### Getting Started
### Prerequisites
- Python 3.7+
- PyTorch
- OpenCV
- Other dependencies listed in `requirements.txt`

## Conclusion:
Our YOLOv9-based traffic sign detection system shows promise but requires further improvements:

1. Data Augmentation: Increase data for specific classes to enhance model training.
2. Data Curation Quality: Improve annotation accuracy and consistency.
3. OCR Integration: Add OCR capabilities for signs with textual information.
4. Pipeline Development: Develop a robust data processing and model deployment pipeline.
5. Model Upgrades: Regularly update and retrain the model with new data.
6. Performance Monitoring: Implement monitoring to identify and address shortcomings.




