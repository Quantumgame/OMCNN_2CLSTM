OM-CNN+2C-LSTM for video salinecy prediction
==========
The model of [**"Predicting Video Saliency using Object-to-Motion CNN and Two-layer Convolutional LSTM"**](https://arxiv.org/abs/1709.06316)

## Abstract
Over the past few years, deep neural networks (DNNs) have exhibited great success in predicting the saliency of images. However, there are few works that apply DNNs to predict the saliency of generic videos. In this paper, we propose a novel DNN-based video saliency prediction method. Specifically, we establish a large-scale eye-tracking database of videos (LEDOV), which provides sufficient data to train the DNN models for predicting video saliency. Through the statistical analysis of our LEDOV database, we find that human attention is normally attracted by objects, particularly moving objects or the moving parts of objects. Accordingly, we propose an object-to-motion convolutional neural network (OM-CNN) to learn spatio-temporal features for predicting the intra-frame saliency via exploring the information of both objectness and object motion. We further find from our database that there exists a temporal correlation of human attention with a smooth saliency transition across video frames. Therefore, we develop a two-layer convolutional long short-term memory (2C-LSTM) network in our DNN-based method, using the extracted features of OM-CNN as the input. Consequently, the inter-frame saliency maps of videos can be generated, which consider the transition of attention across video frames. Finally, the experimental results show that our method advances the state-of-the-art in video saliency prediction.

## Publication
The extended pre-print version of our work is published in [arXiv](https://arxiv.org/abs/1709.06316), one can cite with the Bibtex code:  
```
@InProceedings{Jiang2017predicting,  
author = {Lai Jiang, and Mai Xu, and Zulin Wang},  
title = {Predicting Video Saliency with Object-to-Motion CNN and Two-layer Convolutional LSTM},  
booktitle = {arXiv preprint arXiv:1709.06316},  
month = {Sep.},  
year = {2017}  
}
```
or:   
*Jiang, Lai, Mai Xu, and Zulin Wang. "Predicting Video Saliency with Object-to-Motion CNN and Two-layer Convolutional LSTM." arXiv preprint arXiv:1709.06316 (2017).*

## Models
The whole architecture consists of two parts: OM-CNN and 2C-LSTM, which is shown below. The pre-trained model has already been uploaded to [Google drive](https://drive.google.com/drive/folders/0BwrNwFvsiqVaaEVVUmpyZ0RWSzA?usp=sharing) and [BaiduYun](http://pan.baidu.com/s/1dFGlIY9).  
For running the demo, please the model should be decompressed to the directory of **./model/pretrain/**.

![OM-CNN](/fig/OM-CNN.png "OM-CNN")

![2C-LSTM](/fig/2C-LSTM.png "2C-LSTM")

## Database
As introduced in our paper, our model is trained by our newly-established eye-tracking database,  [LEDOV](https://github.com/remega/LEDOV-eye-tracking-database), which is also available at Dropbox ([Part1](https://www.dropbox.com/s/xqrae7bc73jnncr/LEDOV.zip.001?dl=0) and [Part2](https://www.dropbox.com/s/pxbahpwkea9icw0/LEDOV.zip.002?dl=0)) and [BaiduYun](http://pan.baidu.com/s/1pLmfjCZ)

## Usage
This model is implemented by **tensorflow-gpu** 1.0.0, and the detail of our computational environment is listed in **'requirement.txt'**. Just run **'TestDemo.py'** to see the saliency prediction results on a test video.

## Visual Results
Some visual results of our model and ground-truth.
![visualresult](/fig/visualresult.png "visualresult")

## Contact
If any question, please contact jianglai.china@buaa.edu.cn （or jianglai.china@aliyun.com）, or use public issues section of this repository.

## License
This code is distributed under MIT LICENSE.
