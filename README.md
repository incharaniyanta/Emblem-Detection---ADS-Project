# Emblem-Detection---ADS-Project

In the proposed system, first, a logo detection method is employed to detect a few regions of interest (logo-patches), which likely contain the logo(s), in a document image. The detection method is based on the Convolutional neural network(CNN). For the logo recognition, a template-based recognition approach is proposed to recognize the logo which may present in every detected logo-patch. The proposed logo recognition strategy uses a search space reduction technique to decrease the number of template logo-models needed for the recognition of a logo in a detected logo-patch. The features used for search space reduction are based on the geometric properties of a detected logo-patch. Based on our experimentations on 16000 document images of Flickr dataset, 99.31% of the logos were detected as logo-patches. Among the detected logo 97.90% of logos were recognized. Considering both logo detection and recognition results, 97.22% of the logos in the document images could truly be detected/recognized as the overall performance of the proposed system. Later the project was deployed in EC2 instance to create web application with user interface.

The main concept behind the project is Image Classification using Convolutional neural network (CNN). Image Classification is one of the core problems in Computer Vision that, despite its simplicity, has a large variety of practical applications. A CNN consists of one or more convolutional layers, often with a subsampling layer, which are followed by one or more fully connected layers as in a standard neural network. Why are we choosing CNN?

### Ruggedness to shifts and distortion in the image:
Detection using CNN is rugged to distortions such as change in shape due to camera lens, different lighting conditions, different poses, presence of partial occlusions, horizontal and vertical shifts, etc. However, CNNs are shift invariant since the same weight configuration is used across space.

### Fewer memory requirements: 
In the convolutional layer, the coefficients are used across different locations in the space, so the memory requirement is drastically reduced. 

### Easier and better training: 
Assuming perfect training, we can design a standard neural network whose performance would be same as a CNN. But in practical training, a standard neural network equivalent to CNN would have more parameters, which would lead to more noise addition during the training process. Hence, the performance of a standard neural network equivalent to a CNN will always be poorer.


 So, we use CNN for image classification training models with 27 different logos. We compare the result from different model which was trained for same number data using two different approach. One model consists of Keras with tensor flow backend and the other is implementing transfer learning using Google’s popular Inception v3 model
 
## Deployment 
Both the trained models where deployed in EC2 instance with required user Interface. The web application was secured with different logins and each login had its own functionality. 

## Conclusion 
Inception V3 classifies better than Keras model build by us. The keras model requires more data of images which might in turn require more GPU than the GPU we used to train in Discovery cluster. 

## Future Scope 
The deployment can be performed for multiple images for company logo analytics used by consumers in social media by downloading images from their public post. We can even perform analysis-based geolocation-based consumer usage from the location shared in their post.

For more and better colcusions, please refer to the Project report.



## License
This project is licensed under the MIT License - see the file LICENSE.md for details
