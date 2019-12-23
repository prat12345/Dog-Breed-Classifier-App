# Project Objective : Write an Algorithm for a Dog Identification App using Deep Learning    
# Dataset :    
[Click here for Dataset1](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip) [Click here for Dataset2](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).     
# Motivation :   
learning and understanding of Convolutional Neural Networks    

# Pipeline for Project :   
* First thing in this pipeline is recognition algorithm for both humans and dogs and then classify it by giving out the exact name of breed.    
![p1.png](/Images/p1.png)   

# Human Face detector :    
```
We can try different pretrained algorithms by OpenCV.   
I have tried HOG, LBP, HAAR etc..   
```
* [HAAR](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml):  
This algorithm is also called voila jones algorithm based on HAAR like wavelets.
HAAR wavelets are sequence of rescaled square shaped functions which is explained in detailed way [here](https://en.wikipedia.org/wiki/Haar_wavelet).     

![p3.png](/Images/p3.png)            

HAAR like features for detection :      

![p2.png](/Images/p2.JPG)        

A target window of some determined size is moved over the entire input image for all possible locations to calculate HAAR like features and since it was a very high computational task, therefore alternative method using *integral images* was designed.
The way it works is described briefly below : 

Integral images calculation reduced the computations :    

In below figure, haar works by calculating the difference between sum of black and sum white shades and let's say here it comes out to be something like :   
&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; haar feature &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; real images      
            
![p4.png](/Images/p4.png)        
![p5.jpg](/Images/p5.JPG)         

The closer this difference is to "1", then most probably a haar feature has been detected !     

Integral images :    
![p6.jpg](/Images/p6.JPG)         
