# Recycling-Classifier

![image](https://user-images.githubusercontent.com/122308669/229605103-31ec51ba-96c1-413e-ad05-352c236969d0.png)

## Business and Problem Understanding

The Environmental Protection Agency (EPA) is the stakeholder for this project. The goal is to incentivize companies to invest in the recycling industry. 
The EPA's 2020 Economic Report found that the US recycling industry generated 

- *681,000 jobs*
- *$37.8 billion in wages* 
- *$5.5 billion in tax revenues* 

They also noted that *collecting and recycling 1,000 tons of recyclable materials equates to 1.17 jobs, $65,230 wages, and $9,420 tax revenues.* However, as shown in the graph below, the amount of recyclable materials collected per year has decreased since around 2009 and has been difficult to recover.

![image](https://user-images.githubusercontent.com/122308669/229595112-1a077f10-03f6-4fae-bace-1316230b8fa6.png)
![2](https://user-images.githubusercontent.com/122308669/229606890-45a21137-6ce8-4eb8-9170-65ea4619640a.jpg)

The objective of this project is to create a recycling classification model to identify different types of materials, which will be used to develop a user-friendly app. The app will help people recycle more effectively, which will hopefully lead to an increase in the amount of recyclable materials generated each year. This, in turn, will create more opportunities for companies to invest in the recycling industry.

## Data Understanding

This Dataset was found on Kaggle
Heres the amount of images per class and an image example of every class

![image](https://user-images.githubusercontent.com/122308669/229598881-5ff650ca-9573-4e79-bfe8-513851e44490.png)


## Preprocessing

To address the limited amount of images in the original dataset, I applied data augmentation to the training set. Additionally, I used class weights to handle the class imbalance present in the dataset, which can be seen in the following images:

![image](https://user-images.githubusercontent.com/122308669/229600916-3be767af-e4d8-4147-8207-7b7361984718.png)

![image](https://user-images.githubusercontent.com/122308669/229600801-2753a47c-12b5-4b11-be8c-be7425d937e8.png)

## Modeling

Initially, I experimented with different combinations of convolutional layers and regularizations to build a model for identifying recycling materials. However, none of the models I tried produced satisfactory results. Therefore, I decided to use transfer learning, specifically the VGG16 model, which is pre-trained on over a million images from the ImageNet database. This pretrained network can classify images into 1000 object categories, such as animals, keyboards, pencils, and more.

The first VGG16 model I built included the best combination of convolutional layers and regularizations that I had previously tried, but ultimately, I achieved better results by using only the VGG16 model.

![1](https://user-images.githubusercontent.com/122308669/229606449-e9640b1d-a455-486e-8d00-c34727f551d5.jpg)

## Evaluation

![image](https://user-images.githubusercontent.com/122308669/229604433-f667370f-d41a-4c6f-885c-379cd1916497.png)

## Recommendations and Next Steps

![image](https://user-images.githubusercontent.com/122308669/229604631-1face15a-c9f6-406e-9099-7c65d4668386.png)

