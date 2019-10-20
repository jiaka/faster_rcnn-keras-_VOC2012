### 一，文件介绍
1. [faster_rcnn_train_and_test.ipynb](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/faster_rcnn_train_and_test.ipynb)是主要的入口文件,它由四个步骤组成，分别是参数初始化，数据处理，网络搭建与训练，网络测试。
2. [resnet50.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/resnet50.py)定义了网络结构的函数，分类网络和回归网络。
3. [roi_helpers.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/roi_helpers.py)可以获得筛选后的预选框，交并比，将rpn预测结果转化为预选框等。
4. [losses.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/losses.py)定义了各个损失函数。
5. [data_generator.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/data_generator.py)包括了图片增强，得到rpn网络的训练数据，anchor属性计算等。
6. [data_augment.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/data_augment.py)为图片增强处理函数，包括对图片的翻转或旋转。
7. [RoiPoolingConv.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/RoiPoolingConv.py)定义roipooling层，将每个图片整合到相同大小。
8. [FixedBatchNormalizations.py](https://github.com/jiaka/faster_rcnn-keras-_VOC2012/blob/master/FixedBatchNormalizations.py)相当于重新定义了Batch Normalization。

### 二，资料下载
  本项目采用的数据集是PASCAL-VOC2012数据集，官方下载地址：[http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar)
  
  百度网盘下载地址：链接: [https://pan.baidu.com/s/1ngVYbWxGb0uOvC9Pymo8ow&shfl=shareset](https://pan.baidu.com/s/1ngVYbWxGb0uOvC9Pymo8ow&shfl=shareset) 提取码: 6ib7 
  
  VOC2012数据集分为20类，包括背景为21类，分别如下： 
- Person: person 
- Animal: bird, cat, cow, dog, horse, sheep 
- Vehicle: aeroplane, bicycle, boat, bus, car, motorbike, train 
- Indoor: bottle, chair, dining table, potted plant, sofa, tv/monitor

  在这里只是对这二十类进行目标检测，没有用到图片分割等，所以在数据集中只用到了下图标记的部分
  
  ![图片]()
  
  该网络采用resnet50网络，该网络的权重文件下载地址是：[https://github.com/fchollet/deep-learning-models/releases/download/v0.2/resnet50_weights_tf_dim_ordering_tf_kernels.h5](https://github.com/fchollet/deep-learning-models/releases/download/v0.2/resnet50_weights_tf_dim_ordering_tf_kernels.h5)
  
  百度网盘下载地址：链接: [https://pan.baidu.com/s/18BL8z3jH-dUnLaKe6sa4sw&shfl=shareset](https://pan.baidu.com/s/18BL8z3jH-dUnLaKe6sa4sw&shfl=shareset) 提取码: mexy 

  
### 三，使用说明
  1. 锚框的大小为[128、256、512]，比率为[1：1、1：2、2：1]。
  2. 




















  
