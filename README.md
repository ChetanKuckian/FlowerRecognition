# FlowerRecognition

### The dataset is taken from https://www.kaggle.com/alxmamaev/flowers-recognition.

- The dataset contains images of 5 different types of flowers
  - daisy : 769 images
  - dandelion : 1055 images
  - rose : 784 images
  - sunflower : 734 images
  - tulip : 984 images
- Using the splitfolders library created the training and validation subsets.
- I have set the input shape of the images to (250,250,3)
- A ImageDataGenerator from TensorFlow library is used to perform data augmentation and read the images from the folders.
- Created a CNN model using TensorFlow.
  - The First 2 layers contain a CNN layer with (5,5) kernel size and a MaxPooling layer of size (2,2), with number of filters as 32 and 64 respectively.
  - The next 3 layers  contain a CNN layer with (3,3) kernel size and a MaxPooling layer of size (2,2), with number of filters as 96 ,128 and 256 respectively.
  - The output of the final convolution layer gets flattened and is passed to the Dense layer with 512 nodes/neurons.
  - The final layer consists of 5 nodes/neurons which represent the 5 classes.
  - The models uses categorical_crossentropy as a loss function and Adam optimizer.
- With early stop in place the model got trained till 46 epochs and gave a training accuracy of 81.57% and a validation accuracy of 76.21% and the following f1-scores:
  - daisy : 0.78
  - dandelion : 0.80
  - rose : 0.61
  - sunflower : 0.82
  - tulip : 0.74
  
