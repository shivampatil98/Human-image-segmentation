# Human-image-segmentation

This project focuses on human image segmentation using deep learning techniques. The primary objective is to segment human figures from background areas in images. This solution employs a U-Net model architecture built using TensorFlow/Keras for semantic segmentation. The model is trained on a custom Human Segmentation Dataset and evaluates performance based on various metrics such as accuracy, loss, and Intersection over Union (IoU).

## Dataset

The Human Segmentation Dataset used in this project consists of high-resolution images containing humans along with their corresponding binary segmentation masks. The dataset includes images labeled with 1 for the human region and 0 for the background.

## Model Architecture

The model used in this project is a U-Net architecture, which is highly effective for image segmentation tasks. U-Net consists of a contracting path (encoder) to capture context and a symmetrical expanding path (decoder) to enable precise localization of the human figure in the image.

The architecture consists of the following parts:

1. Encoder: A series of convolutional layers with max-pooling to capture spatial hierarchies.
2. Bottleneck: A series of convolutional layers at the lowest resolution.
3. Decoder: Up-convolutional layers to restore the image resolution, while combining features from the encoder via skip connections.
4. Output Layer: A sigmoid activation function is used in the final layer for binary segmentation.

## Training

The model was trained on the Human Segmentation Dataset with the following setup:

1. Image Size: 512x512
2. Batch Size: 16
3. Epochs: 50
4. Optimizer: Adam
5. Loss Function: Binary Cross-Entropy
6. Metrics: Accuracy, Intersection over Union (IoU)

## Evaluation Metrics

1. Accuracy: Measures the overall percentage of correctly classified pixels.
2. IoU (Intersection over Union): Measures the overlap between the predicted and ground truth masks, providing a better evaluation metric for segmentation.

## Results

Training Results
Training Accuracy: 73%
Validation Accuracy: 75%
Training Loss: 0.68
Validation Loss: 0.68

## IoU:

The Intersection over Union (IoU) for the human region segmentation was calculated and found to be 0.75, indicating that the model successfully identified human regions.
