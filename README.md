# Segmentation_U-Net

Urban Landscape Image Segmentation
When I initially came across the field of computer vision, my knowledge was limited to Object Detection and Classification. However, Image Semantic Segmentation adds another layer to this. Image Segmentation involves the division of a digital image into multiple segments, which can also be referred to as regions or objects (collections of pixels). The main purpose of segmentation is to simplify or alter the image representation into something more understandable and analyzable. This technique is often employed to identify objects and define boundaries within an image.

Context
Traffic congestion and a high number of accidents are persistent issues in numerous large cities globally. One of the key contributors to these problems is driver negligence. The World Health Organization (WHO) recognizes the traffic system as one of the most intricate and perilous systems we encounter nearly every day.

Objectives
The introduction of Self-Driving Car technology aims to mitigate accidents and congestion resulting from driver negligence.

Cityscapes Dataset
Acquiring the Dataset
The official dataset can be obtained from their website. Registration and account creation are prerequisites for downloading. After downloading the dataset, it can be uploaded to Google Colab for further use.

Data Preprocessing
1. Normalization of the Dataset
2. Application of One Hot Encoding
3. Dataset Splitting

Construction of the UNet Model
"The architecture comprises of an encoding path for contextual information capture and a symmetric decoding path that enables precise localization. Our results demonstrate that this network can be trained end-to-end using a limited number of images and outperforms previous state-of-the-art methods." - Excerpt from the UNet Paper

![image](https://github.com/zakky211/Segmentation_U-Net/assets/62234134/f0bfa279-e7ca-40c1-8e13-d01d67aef8db)

Model Training
The initial steps involve setting up model checkpointing and early stopping. Adam optimization is employed with a learning rate of 0.001. The choice of loss function is Categorical Cross-Entropy, while Accuracy serves as the evaluation metric.

Number of Epochs: 100
Batch Size: 8

After experimenting with three training processes, the best model achieves a training loss: 0.2486 - accuracy: 0.9208 - val_loss: 0.6316 - val_accuracy: 0.8446, Test loss: 0.887, Test accuracy: 0.787, Mean IoU: 41.55%.

Model Loading
Previously saved models can be loaded using "keras.models.load_model(model-path)". 

Evaluating Model Predictions
The process of prediction involves several images:
![image](https://github.com/zakky211/Segmentation_U-Net/assets/62234134/80db725f-5758-40bf-acdf-2e9f92fc3918)


