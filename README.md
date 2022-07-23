
-   ## Wheather Image Recognition
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/iStock-477110708%20(1).jpg?raw=true)
prepared by:Huzaifa Nusairat

-   ## problem overview

- Dataset contains 6862 images of different types of weather, it can be used to implement weather classification based on the photo.

- The objective of the project is:
Build a deep learning model to Recognize weather state.

-   ## Solution process

### Discuss about The Data:

- I got the data set from kaggle Data sets site: Read Data.txt

- Dataset contains 6862 images of different types of weather.
- It has (11) classes ['rain', 'dew', 'frost', 'rainbow', 'snow', 'rime', 'sandstorm', 'hail', 'fogsmog', 'lightning', 'glaze'].

### Analyze The Data :

- The Data is unbalanced, There is a discrepancy in the number of pictures per class, Most of the pictures are rime pictures, and the minority are rainbow pictures.
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/eda.png?raw=true)

- Some samples of pictures:
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/pic1.png?raw=true)
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/pic2.png?raw=true)

### Analytical approach:

- It is a supervised Machine Learning project.

- First, I split Data into (train, val, test)
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/split.png?raw=true)

- Then using resamplling techniques such as (albumentation laibrary to augmanted Data) make each class has the same number of images and tensorflow generator to create and label each part of Data sets.
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/after_aug.png?raw=true)

- Fed the training data set into some pre_traind models and found that Mobile_Net architecture has the best accuracy in testing data set.
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/acc_loss.png?raw=true)

- Finally, analysing the error of Mobile_Net architecture after predicting test data set found the following result:
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/error1.png?raw=true)
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/error2.png?raw=true)

- Some samples of miss labeled images:
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/error3.png?raw=true)


-   ## Models comparison

- I tryed a CNN model (Three Conv layers with Dense layer contain 256 units and dropout regularization layer) and (3) pre_trained models ['Xception-Net', 'Mobile_Net', 'DenseNet201'].
![alt text](https://github.com/Huzaifa-Nusairat/Weather_Image_Recognetion/blob/main/images/models.png?raw=true)


-   ## Recommendation

- Collect more images to get better model performance
- Using other pre_traind models it could give more accuracy on testing data set