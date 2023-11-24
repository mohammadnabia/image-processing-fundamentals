# Motion blur in spatial and frequency domains using Python in Google Colab

This repository provides code examples and a tutorial for performing Motion blur in spatial and frequency domains using Python in Google Colab.
Motion blur is crucial to computer vision and image processing, influencing how machines perceive and interpret dynamic scenes. This project aims to provide a comprehensive understanding of motion blur and its implications for image analysis by delving into spatial and frequency domains.

## Motion blur for what?
Motion blur is a phenomenon in photography and computer graphics where objects in motion appear blurred in the resulting image.
This effect occurs when the camera's shutter remains open for a significant duration while capturing a scene with moving elements.
As a result, these moving objects leave a streak or trail in the image, indicating their path of motion.
In machine learning, motion blur is often simulated or incorporated into training datasets for computer vision tasks. 

There are several reasons why motion blur is useful in machine learning applications:
* Realism and Generalization:
Including motion blur in training data helps models generalize better to real-world scenarios. Since motion blur is common in natural scenes, training with such data makes models more robust when exposed to similar conditions during deployment.

* Robustness to Variability: Introducing motion blur enables models to become more tolerant to variations in input data. This is crucial for applications where the appearance of objects may change due to factors such as motion, varying lighting conditions, or other environmental factors.

* Enhanced Feature Learning: Motion blur can aid in learning features invariant to motion-related transformations. Models trained on datasets with motion blur may develop a better understanding of object representations that are not overly sensitive to the exact position of objects in each frame.

* Improved Object Recognition: Motion blur can help prevent overfitting to specific object poses in scenarios involving rapid movement. By training with motion-blurred images, models can learn to recognize objects under different motion conditions, leading to more reliable object recognition in dynamic environments.

## Dependencies:
Ensure you have the following dependencies installed:

* *Python*
* *NumPy*
* *OpenCV*
* *Matplotlib*

## Examples
* Defining the motion blur function for spacial domain
- The convolution function with a selectable kernel
```python
def motion_blur(img, size=None, angle=None):

    k = np.zeros((size, size), dtype=np.float32)
    k[(size-1)//2, :] = np.ones(size, dtype=np.float32)
    k = cv2.warpAffine(k, cv2.getRotationMatrix2D((size/2-0.5, size/2-0.5), angle, 1.0), (size, size))
    k = k * (1.0/np.sum(k))
    return cv2.filter2D(img, -1, k) 

```

|![image](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/0007d319-4b3d-4573-beca-3fb6591aa03d)| 
|:--:| 
| *Output for different amount of size and angles* |

* In the frequency domain, you must first convert your photo into frequency domain mode, and after that, you can apply your transform using the degradation function of motion blur like the following equation:
 
|![image](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/ff6ff5fb-f0d8-4c42-b086-270849b910c5)| 
|:--:| 
| *The degradation function of motion blur in the frequency domain* |

* And finally, you can see the result of blurring the input image in the frequency domain
|![image](https://github.com/mohammadnabia/image-processing-fundamentals/assets/53332753/cb3238c6-7a05-4a4e-ba38-b35adc7fc3d9)| 
|:--:|

If you need more information, you can fully master this topic by viewing the provided code.


## STEPS
### part 1
- [x] Import cv2, numpy, matplotlib, urllib, cv2_imshow, random
- [x] Import your image
- [x] Define the motion blur function for the spatial domain and blur your image
### part 2
- [x] Normalize the input image
- [x] Convert the image from the spatial domain to the frequency domain by Fourier transform
- [x] use motion blur function and blur
- [x] 🏁Done🏁

## Contributing
Contributions to this repository are welcome. Please feel free to submit a pull request if you have any improvements, bug fixes, or additional examples related to image blurring. Let's collaborate and make this repository a valuable resource for the community.

## License
This project is licensed under the MIT License. You can use, modify, and distribute the code as the license permits.

- - -

We hope this repository and tutorial help you understand the Motion blur in spatial and frequency domains using Python in Google Colab. Please feel free to reach out if you have any questions or suggestions.

👾Have a splendid coding👾



