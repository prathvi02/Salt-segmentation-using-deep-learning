# Salt-segmentation-using-deep-learning
Implemented advanced FCNN for salt detection in seismic images, crucial for mining. Emphasis on the difficulty of accurate salt detection and the necessity for a reliable automated algorithm.

## About Dataset
- The dataset consists of 4,000 seismic image patches of size (101x101x3) and corresponding segmentation masks
- The images are chosen at various locations in the subsurface, and each pixel is classified as either salt or non-salt
- The dataset is used to create accurate seismic images and 3D renderings, which are essential for understanding the geological structure of the Earth's subsurface
- TGS, a leading geoscience data company, has developed a U-Net model for semantic segmentation using TensorFlow 2.0 to address this challenge
- The TGS Salt Identification Challenge is part of a broader effort by TGS to provide full-service salt interpretation using specially designed workflows and tools to produce accurate salt models

## Model used in this project

U-Net is an encoder-decoder convolutional neural network with extensive medical imaging, autonomous driving, and satellite imaging applications.
![image](https://github.com/prathvi02/Salt-segmentation-using-deep-learning/assets/73091532/7a366c05-0162-4b84-a404-dd965bbf0360)

## Model Architecture
- Input Layer: Takes input_img to define input image shape.
- Contracting Path (Encoder): Repeated 3x3 convolutions (unpadded) + ReLU, followed by 2x2 max pooling (stride 2) for downsampling. Doubles feature channels at each step to capture input context.
- Expansive Path (Decoder): Upsampling and concatenation, followed by two 3x3 convolutions + ReLU. Combines precise localization with contextual information from the contracting path.
- Final Layer: Utilizes a 1x1 convolution to map 64-component feature vectors to the desired number of classes.

# Result
![image](https://github.com/prathvi02/Salt-segmentation-using-deep-learning/assets/73091532/003c6e99-3a30-4fd5-8552-bc03401d426a)

- U-Net gave training accuracy of 97 % and validation accuracy of 94% and loss of just 0.14.

![image](https://github.com/prathvi02/Salt-segmentation-using-deep-learning/assets/73091532/3327d3bd-c267-4320-b821-c630d62e8f98)


## Segmentation Result

![image](https://github.com/prathvi02/Salt-segmentation-using-deep-learning/assets/73091532/31372fb1-b113-4575-85d5-eec51d05de59)
![image](https://github.com/prathvi02/Salt-segmentation-using-deep-learning/assets/73091532/db836ccd-9b3a-43fe-9537-002ecbe66105)






