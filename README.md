# Plant-disease-recognition-from-leaf-images
A group project on complex image classification: evaluation of different architectures

Dataset: from Kaggle, 87976 images of healthy and diseased leaves classified in 38 classes

EDA:
Split: 70333 training / 17610 val / 33 test
256x256 resolution, RGB. Slight imbalance in favour of the Green channel, as expected.
The size of the dataset has been increased through data augmentation, therefore we explored the quality of the resulting dataset.
Image quality was explored through Laplacian variance, with a threshold of 100. 
0.6% of the images in the traning set and in the validation set are below the threshold. 
2 images in the dataset are below the threshold, making up 2% of the whole set of 33 images.

Frameworks and libraries: Pytorch, TensorFlow, PIL, IPython, cv2, Numpy, torchvision, transformers, Shap, Pandas

Model architectures:
- Custom CNN: 
- ResNet18
- MobileNetV3Large
- ViT
- Autoencoder

Results (accuracy):
- CNN: 90.9%
- ResNet18: 94.7%
- MobileNteV3Large: 99.2% (top score)
- ViT: 93.8%
- Autoencoder: 25.28% (lowest score)

EXAI SHAP:
Discoloration and texture have the highest impact on the classification, the background and the green areas of the leaves have little to no impact (they appear white on the SHAP heatmap).






