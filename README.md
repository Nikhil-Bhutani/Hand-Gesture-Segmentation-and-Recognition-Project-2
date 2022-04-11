# Hand-Gesture-Segmentation-and-Recognition-Project-2
This project is an extension to previous project Hand Gesture Recognition by implementing the Mask-RCNN algorithm for segmenting the gesture from image even in complex backgrounds and under different lighting conditions. Segmented images obtained as an output were further fed to transfer learning based architectures(VGG16, InceptionV3, Resnet50) for classification of gestures. Remarkable accuracies were achieved 97.87%, 97.46%, 98.06 for VGG16, InceptionV3 and Resnet50 respectively. 

### Install Required Libraries
```bash
   pip install tensorflow==1.13.1
```
```bash
   pip install keras==2.1.0
```
```bash
   pip install opencv-python
```
```bash
   pip install numpy 
```
```bash
   pip install pandas
```
```bash
   pip install matplotlib
```
```bash
   pip install scikit-learn
```
## Procedure
- First, some proportion of images from the dataset were labelled using VGG Annotator tool https://www.robots.ox.ac.uk/~vgg/software/via/via.html.
- Second, labelled data (.json file) along with the original images were fed to MASKRCNN model for training using Train_MASK_RCNN.ipynb.
- Third, by using Predict_Mask_RCNN.ipynb rest of the images can be segmented.
- Fourth, segmented images obtained can be classified and real time analysis for Hand Gesture Recognition can be performed using the files (RESNET50+INCEPTIONV3.ipynb, VGG_16.ipynb) present in Classification_Models directory.

**Note:- To implement the MASK_RCNN model (both Train_MASK_RCNN.ipynb and Predict_Mask_RCNN.ipynb), some files are needed for the implementation of MRCNN. The required files are present in the mrcnn directory.**
