# SegCaps-keras-chapter4

The chapter3 of the segmentation network summary: 
### Pay attention to the internal structure of CNN.

External links: Capsules for Object Segmentation [paper](https://arxiv.org/abs/1804.04241)

Nowadays, a lot of CNN networks perform very well in image segmentation and classification. However, we should not only focus on how to build a CNN network architecture efficiently, but also pay attention to the implementation of the internal structure of CNN.

Recently, Hinton, who is known as the "father of deep learning," proposed the capsule network -- [《Dynamic Routing Between Capsules》](https://arxiv.org/abs/1710.09829). Hinto's paper mentions that the capsule network is more like the way the brain works. When people process a certain visual information, the brain has a "routing" mechanism to find the best "capsule" in the brain to process the visual information. But CNN only considers the problem of "whether it has or not" and does not consider the structural relationship of the feature map. This structural relationship includes position, angle, and so on. In response to this problem, the concept of capsule is proposed. The output of capsule is no longer a neuron but a vector. This vector contains information such as position, size, angle, etc., so that it can model more detailed information. The code we present here is applying the capsule to the segmentation network.

**** References ****
This code borrows from [Cheng-Lin-Li](https://github.com/Cheng-Lin-Li)'s [work](https://github.com/Cheng-Lin-Li/SegCaps) and is modified to use on my own dataset.

### Environment: 
  
            Keras version >> 2.2.4; tensorflow(Keras backend) >> 1.3.0
            
## Notes
1. The problem of version mismatch was modified, and the model was applied to my own 2D dataset. The training and testing was successful.
2. [Here](https://github.com/naturomics/CapsNet-Tensorflow) is the code of 《Dynamic Routing Between Capsules》. This is capsule for classification.
3. Others proposed a variant of capsule [fast capsule](https://arxiv.org/abs/1806.07416). [Here](https://github.com/amobiny/Fast_CapsNet) is the paper's code.
