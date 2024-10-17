# Deep Dive into Deep Learning

This project compares multiple neural network architectures by varying the number of parameters to analyze training and testing accuracy and loss values for image classification.

## Dataset

- CIFAR-10 dataset
- 60,000 32x32 color images
- 10 classes with 6000 images per class
- Training set: 50,000 images
- Testing set: 10,000 images

## Implementation Details

- Convolutional Neural Network (CNN) architecture
- ADAM optimizer
- Cross Entropy loss function
- Learning rate of 1e-3
- Trained and tested using Cluster- turing.wpi.edu

## Model Variations

- ResNet18
- ResNet34
- DenseNet
- ResNeXt

## Data Augmentation

The following data augmentation techniques were applied:

1. CenterCrop(10)
2. Normalize((0.485, 0.456, 0.406), (0.229, 0.224, 0.225))
3. RandomRotation(30,70)

## Key Observations

- Different combinations of annotations have a direct impact on the output filter size of the network
- MaxPool2d() and AvgPool2d() functions were used to adjust the filter size input to the final classifier layer

## Results

| Model    | No of Epochs | Train Accuracy | Test Accuracy |
|----------|--------------|----------------|---------------|
| CNN      | 477          | 77.78          | 58.82         |
| ResNet18 | 150          | 95.99          | 43.22         |
| ResNet34 | 150          | 91.24          | 45.56         |
| DenseNet | 1200         | 70.06          | 45.15         |
| ResNeXt  | 7            | 45.41          | 10.88         |

## Computational Time

- ResNeXt took longer to train
- Basic CNN and ResNet18 were faster to train

## Future Work

Focus on improving test accuracy even over shorter training periods.

## How to Run

```bash
cd Classification
cd Code

# Train
python Train.py

# Test
python Test.py
```

## Requirements

(List any dependencies or requirements here)

## Contributors

(Add contributor information here)

## License

(Add license information here)
