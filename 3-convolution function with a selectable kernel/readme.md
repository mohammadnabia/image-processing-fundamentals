# Convolution Function with Selectable Kernel for Image Filtering & Spatial Filtering using Python in Google Colab

This repository provides code examples and a tutorial for performing image filtering and spatial filtering using a convolution function with a selectable kernel in Python on Google Colab. The examples and explanations provided here will help you understand the concept of convolution and implement various spatial filtering techniques effectively in your own image processing projects.

## Introduction
Convolution is a fundamental operation in image processing, used for tasks such as image filtering and feature extraction. It involves sliding a kernel (also known as a filter or mask) over an image and performing element-wise multiplication and summation operations to obtain a new output image. Spatial filtering is a common application of convolution, where different kernel configurations can produce various effects like blurring, sharpening, edge detection, and more.

This repository provides a convolution function with a selectable kernel that allows you to perform image filtering and spatial filtering using Python in Google Colab. It covers various techniques and provides code examples to help you understand and implement different filters in your own projects.

## Prerequisites

To follow the examples in this repository, you need the following prerequisites:

* Basic knowledge of Python programming language.
* Familiarity with image processing concepts.
* A Google account to access Google Colab.

## Examples

- The convolution function with a selectable kernel
```python
def convolution1(image, kernel):
  pixels = []
  for i in range(image.shape[0]):
    for j in range(image.shape[1]):
      pixels.append(image[i,j]);

  pixels = np.array(pixels).reshape(image.shape[0],image.shape[1]);

  pixels = np.insert(pixels , [0,image.shape[0]] , np.zeros(len(pixels[0])) , axis = 0);
  pixels = np.insert(pixels , [0,image.shape[1]] , np.zeros((len(pixels[:, 0]) ,1)) , axis = 1);

  convoluted_matrix = [];
  for i in range(1,image.shape[0]):
    for j in range(1,image.shape[1]):
     temp = pixels[i:i+3 , j:j+3]
     product = np.multiply(temp,kernel)
     convoluted_matrix.append(sum(sum(product)));

  convoluted_matrix = np.array(convoluted_matrix).reshape(image.shape[0]-1,image.shape[1]-1);

  return(convoluted_matrix)
```
 - Laplacian filter
 
| ![download](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/cfc83af4-31e8-4320-b2e5-fbab518b818b)| 
|:--:| 
| *The image on the left is our input - the image in the middle is laplacian -4 filtered image -  the image on the right is laplacian +4 filtered image* |

- Derivative filter

| ![download](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/c30a7832-9a4c-406d-89f5-00ed3e64f428)| 
|:--:| 
| *The image on the left is our input - the image in the middle is derivative2 -8 filtered image -  the image on the right is derivative2 +8 filtered image* |

- Sobel filter

| ![download](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/bbc9c6bb-e660-43ef-872c-e9a64f4a4a94)| 
|:--:| 
| *The image on the left is our input - the image in the middle is sobelx filtered image -  the image on the right is sobely filtered image* |

- Median filter

| ![download](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/eaecc06f-e460-4699-9999-2b5c315fd918)| 
|:--:| 
| *The above image is the input and histogram of the input image - The bottom image is the output and the histogram of the output image* |

## STEPS

- [x] Import cv2, numpy, matplotlib, urllib, cv2_imshow
- [x] Define histogram function 
- [x] Defining the convolution function with a selectable kernel for use in filtering
- [x] import images
- [x] define kernels to use as spatial filters (smoothing filters, laplacian, sobel mask, median filter etc)
- [x] use kernels
- [x] 🏁Done🏁


## Contributing
Contributions to this repository are welcome. If you have any improvements, bug fixes, or additional examples related to image filtering and spatial filtering, please feel free to submit a pull request. Let's collaborate and make this repository a valuable resource for the community.

## License
This project is licensed under the MIT License. You are free to use, modify, and distribute the code as permitted by the license.

- - -

We hope this repository and tutorial help you understand the convolution function and its application in image filtering and spatial filtering using Python in Google Colab. If you have any questions or suggestions, please feel free to reach out.

👾Have a marvelous coding👾





