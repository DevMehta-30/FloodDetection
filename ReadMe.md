# Comprehensive Flood Detection and Pathway Assessment

## 📄Introduction

The aim of the project is to employ a deep learning model in order to **detect Flood Events** and tell if the **path used to reach a particular location is flood-prone or not.**

The thought between this project came from _SIH,2022 problem statement_:\
https://qa.sih.gov.in/sih2022PS?technology_bucket=MTQ=&category=U29mdHdhcmU=&organization=Q2VudHJhbCBXYXRlciBDb21taXNzaW9uIChDV0MpLCBNaW5pc3RyeSBvZiBKYWwgU2hha3Rp&organization_type=MQ==

## ⌨️Important steps of the project:

- **Flood Detection**
- **Path Assessment**

## 🌊Flood Detection

It involves training a **_Convolutional Neural Network (CNN)_** on labeled satellite imagery and environmental data to classify flood and non-flood regions. Real-time data, such as current satellite images and weather information, is then fed into the model for flood prediction. Alerts are generated when flooding is detected, and visualization tools provide insights into affected areas. Continuous model improvement is achieved through feedback and adaptation to changing flood patterns, ensuring accurate and timely flood detection and response.

- **DataSet Information**  
  The dataset is divided into two parts:  
  Label and Source:  
  <br>
  The folder ‘Label’ contains json files of individual dates where the flooded areas are labeled.
  It will be used for mapping with real time satellite images in the ‘Source’ folder and help identify flooded
  and non-flooded areas.  
  <br>
  ‘Source’ folder as earlier mentioned contains images from December 2018 to may 2019. We have made separate folders for each corresponding date separately containing 12 files each.
  The 12 files includes Tif files starting from B01 to B12 which typically refer to different bands or spectral channels of data.
  <br>
  ![Alt text](/Screenshots/image.png)
  <br>
  B1 - Blue Band: The blue band typically captures information in the blue part of the visible spectrum.
  <br>
  B2 - Green Band: This band captures data in the green part of the visible spectrum.
  <br>
  B3 - Red Band: The red band captures data in the red part of the visible spectrum.
  <br>
  B4 - Near-Infrared Band (NIR): This band captures data in the near-infrared part of the spectrum. NIR data is valuable for vegetation health assessment.
  <br>
  B5 - Shortwave Infrared Band (SWIR): SWIR data is in the shortwave infrared region and is useful for detecting geological features and moisture content.
  <br>
  B6 - Thermal Infrared Band (TIR): TIR data measures temperature-related information.
  <br>
  B7 - Mid-Infrared Band: This band captures data in the mid-infrared region, which is useful for various applications, including mineral identification.
  <br>
  B8 - Panchromatic Band: The panchromatic band typically has higher spatial resolution and is used for detailed mapping.
  <br>
  B9 - Cirrus Band: The cirrus band captures data related to atmospheric cirrus clouds.
  <br>
  B10 and B11 - Thermal Infrared Bands: These bands may capture data in different thermal infrared regions and are useful for temperature-related applications.
  <br>
  B12 - SWIR Band: Another shortwave infrared band for additional information.

- **Data Preprocessing**
  <br>
  We are using primarily using the following python libraries:
  <br>
  <br>
  1.Rasterio -is a Python library for reading and writing geospatial raster data. It provides tools for working with formats such as GeoTIFF, and it's commonly used in geospatial and remote sensing applications
  <br><br>
  2.OpenCV- is a popular open-source computer vision and image processing library that provides a wide range of tools and functions for tasks like image manipulation, computer vision, and machine learning.
  <br><br>
  Rest are some python modules like cv2,glob,shutil and subprocess specifically helping with file path expansions and managing the root directories.
  After processing in the end we get a list containing all source files which in this comes to be around ‘1189’.
  ![Alt text](</Screenshots/image-3.jpg>)

- **Data Modeeling**
  <br>
  We have used the deep learning model containing all these layers after splitting the train and test data.
  <br><br>
  These components are used in building and training neural network models, particularly for image classification tasks using the Keras library:
  <br>

1. Sequential Model: A `Sequential` model is a linear stack of layers. You add layers one by one, and each layer flows into the next one. It is suitable for most deep learning applications. It represents a neural network with a clear input-to-output flow.
   <br><br>
2. Dense Layer: A `Dense` layer is a fully connected layer in a neural network. Each neuron in this layer is connected to every neuron in the previous and subsequent layers. It's used for feedforward neural networks and can perform tasks such as classification and regression.
   <br><br>
3. Convolutional Layer (Conv2D): A `Conv2D` layer is used for processing spatial data, such as images. It applies convolutional filters to extract features from input data. This layer is critical in convolutional neural networks (CNNs) for tasks like image recognition.
   <br><br>
4. MaxPooling Layer (MaxPool2D): A `MaxPool2D` layer reduces the spatial dimensions of the input data by selecting the maximum value within a certain region. It is commonly used in CNNs to downsample and reduce the computational load.
   <br><br>
5. Flatten Layer: A `Flatten` layer is used to flatten the output from previous layers into a 1D vector. This is often necessary to connect the convolutional layers to dense layers in a neural network.
   <br><br>
6. Dropout Layer: A `Dropout` layer is a regularization technique used to prevent overfitting. It randomly drops a fraction of neurons during training to improve the model's generalization.

- **Conclusion**
  <br>
  After evaluating the above model we get an accuracy of 82%.
  ![Alt text](</Screenshots/image-4.jpg>)
  <br><br>
  ![Alt text](</Screenshots/image-5.jpg>)

## 🛣️Path Assessment

In our project, we've harnessed the power of the Python library, **OSMnx**, along with open-source mapping resources to create a sophisticated system for street mapping. With this technology, users have the flexibility to select their desired location and mode of transport. Our system then swiftly computes and displays the shortest distance between the chosen points. Integrating our initial model for flood detection, we take it a step further. Before suggesting a path, our system assesses the safety of the route by evaluating if the path is flooded or not. This dynamic fusion of street mapping and flood detection ensures that users can make informed decisions about their travel routes, especially during flood-related situations, thus enhancing safety and efficiency.
<br>

**_Safe Path_**
<br>
![Alt text](/Screenshots/image-1.png)
<br>

**_Flooded Path_**
<br>
![Alt text](/Screenshots/image-2.png)

## 🖥️Tech Stack

![Static Badge](https://img.shields.io/badge/Python-blue)
<br>
![Static Badge](https://img.shields.io/badge/Keras-green)
<br>
![Static Badge](https://img.shields.io/badge/OSMNx-red)
<br>
![Static Badge](https://img.shields.io/badge/Folium-green)
<br>
![Static Badge](https://img.shields.io/badge/Scikit-Learn-red)
<br>
![Static Badge](https://img.shields.io/badge/Glob-blue)
<br>
![Static Badge](https://img.shields.io/badge/Pandas-Numpy-yellow)

## Team Members

- #### [Dev Mehta](https://github.com/DevMehta-30)
- #### [Astha Jha](https://github.com/Rythmastha)
- #### [Shailza Thakur](https://github.com/ShailzaThakur7)
