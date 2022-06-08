<p align="center">
  <img width="80%" height="auto" src="resources/fig1.png">
</p>
<p align="center">
In this work, we designed a saliency detection model suitable for the target tracking task. Our proposed model takes a video as input and outputs the location of the most salient objects in the video, which benefits for improving the performance of downstream tracking network.  
</p>


# Abstract

Aiming at the problem that the current saliency detection models are not pertinent when dealing with tracking tasks and ignore the contribution of motion information to saliency, a spatio-temporal saliency detection model suitable for target tracking tasks is proposed. In the spatial domain, the spatial saliency detection model based on histogram contrast is improved by introducing SLIC superpixel segmentation and prior information of the target position, and the complete and saliency target of each frame is obtained. In the time domain, the motion feature channel is added as the guidance method of the visual attention, and the motion vector is detected by the frame difference method and the optical flow method. The motion vector's saliency is analysed using the features of motion entropy and direction consistency, and then the time-domain salient model is constructed. Finally, saliency maps of the time-domain and spatial domain are merged using an adaptive weighting approach to obtain the Spatio-temporal saliency detection model that adapts to different tracking task situations.

# Overview

<p align="center">
  <img width="50%" height="auto" src="resources/fig2.png">
</p>

  The above flow chart shows that our saliency detection model takes a video clip as input. Two branches are designed for low-level image-level features and dynamic semantic features, respectively. The branch for low-level features takes into a single frame and firstly calculates a colour histogram. Then the image will be classified into different regions through the SLIC super-pixel segmentation methods. Next, the colour contrast will be calculated at the super-pixel level. Finally, we will get the spatial domain saliency map, where the colour contrast defines the saliency. The branch for dynamic semantic features takes the adjacent video frames as input, and the optical flow methods will detect the motion in videos. Then the motion entropy will be calculated by the optical flow vector, which will be then used to define the temporal domain saliency map. The spatial saliency map and temporal saliency maps will be adaptively fused to get the final saliency map.


# Spaio-temporal saliency detection results

<p align="center">
  <img width="70%" height="auto" src="resources/fig3.png">
</p>

# Citation
```
@article{chen2022unsupervised,
  title={Unsupervised domain adaptation based COVID-19 CT infection segmentation network},
  author={Chen, Han and Jiang, Yifan and Loew, Murray and Ko, Hanseok},
  journal={Applied Intelligence},
  volume={52},
  number={6},
  pages={6340--6353},
  year={2022},
  publisher={Springer}
}
```
