# Histogram equalization using python in google colab

Have you ever wanted to increase the quality of your image or improve the contrast of your desired photo? 
In this repository, we will examine histogram equalization using Python programming language in the Google colab environment.
What is implemented in this repository is on black-and-white images. In fact, before starting to work with the photo, we single-channeled our picture, which means our photo is black and white, and we work only on the black and white channel. We removed the other Red, Green, and Blue channels.

## Introduction
Histogram equalization is a technique used to adjust the intensity distribution of an image. By redistributing the intensity values, histogram equalization can enhance the contrast of an image and reveal hidden details. It works by stretching the histogram to cover the entire intensity range, thus making the image visually more appealing and improving its overall quality.

This repository demonstrates how to perform histogram equalization using Python in Google Colab. It provides code examples and a step-by-step tutorial to help you understand and implement histogram equalization in your own projects.
## Prerequisites
To follow the examples in this repository, you need the following prerequisites:

* Basic knowledge of Python programming language.
* Familiarity with image processing concepts.
* A Google account to access Google Colab.

| ![download](https://user-images.githubusercontent.com/53332753/210248042-30cb165b-5375-4a26-a76d-bf4f1f8b64ed.png)| 
|:--:| 
| *The image on the left is our input and the image on the right is the output of our code.* |

## STEPS

- [x] Import cv2, numpy, matplotlib, urllib, cv2_imshow
- [x] Define your histogram function
- [x] Define cumulative summation of the data fucntion
- [x] Import or upload the image
- [x] Calculate the histogram of the input image
- [x] Calculate the cumulative sum of the input image
- [x] Acquire the value from the cumulative sum for every pixel in our image and set that as equalized image.
- [x] Compare the input image with the enhanced image
- [x] 🏁Done🏁

## Contributing
Contributions to this repository are welcome. If you have any improvements, bug fixes, or additional examples related to histogram equalization, please feel free to submit a pull request. Let's collaborate and make this repository a valuable resource for the community.

## License 
This project is licensed under the MIT License. You are free to use, modify, and distribute the code as permitted by the license.
