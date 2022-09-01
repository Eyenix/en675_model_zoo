
<img alt="Python" src ="https://img.shields.io/badge/python-3.6-orange"/>


## EN675 NPU Model Zoo
The EN675 Series SoC Model Zoo privides the trained models for AI Object Detection (OD) and Classification (CLS) applications.  
:rocket: EN675 NPU Spec Link : [EYENIX EN675 NPU Spec & Demo](https://resonant-duke-420.notion.site/EN675-AI-NPU-Solution-d407c17992d8447b9c98ac2bfede8cdb)
***
&#160;
### :star: Download
#### :arrow_forward: Object Detection
**classes** : Person, Bicycle, Motorbike, Car, Bus, Truck  
<figure>
    <img src="./img/6classes_image.PNG" title="6class">    
</figure>

|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|11MB|26ms|13ms|
|512_512_eyenix_model_v1|[512_512_eyenix_model_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9466030/512_512_eyenix_model_v1.zip)|[od6class_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9466035/od6class_512.zip)|18MB|37ms|20ms|
|640_640_eyenix_model_v1|-|-|25MB|54ms|29ms|


&#160;

### To be updated later
**class** : Face  
<figure>
    <img src="./img/face_image.PNG" title="face">    
</figure>

|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|-|-|-|
|512_512_eyenix_model_v1|-|-|-|-|-|
|640_640_eyenix_model_v1|-|-|-|-|-|

&#160;

#### :arrow_forward: Classification (TBD)
**class** : -
|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model|-|-|-|-|-|
|512_512_eyenix_model|-|-|-|-|-|
|640_640_eyenix_model|-|-|-|-|-|
***

&#160;

### :trophy: Performance
#### :arrow_forward: Object Detection
:+1: Train Dataset : PASCAL VOC 2007 (train, val), PASCAL VOC 2012 (train, val)  
:+1: Test Dataset : PASCAL VOC 2007 (test)
|Model|mAP at IOU = .50 (GPU)|mAP at IOU = .50 (NPU)|
|:-----:|:---:|:---:|
|320_320_eyenix_model_v1|0.752|-|
|512_512_eyenix_model_v1|0.782|-|
|640_640_eyenix_model_v1|-|-|

&#160;

### To be updated later
:+1: Train Dataset : COCO 2017 (train)  
:+1: Test Dataset : COCO 2017 (val)
|Model|mAP at IOU = .50 (GPU)|mAP at IOU = .50:.05:.95 (GPU)|mAP at IOU = .50 (NPU)|mAP at IOU = .50:.05:.95 (NPU)|
|:-----:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|-|-|
|512_512_eyenix_model_v1|-|-|-|-|
|640_640_eyenix_model_v1|-|-|-|-|

&#160;

#### :arrow_forward: Classification (TBD)  
:+1: Train Dataset : ImageNet  
:+1: Test Dataset : ImageNet
|Model|TOP-1 Accuracy|
|:-----:|:---:|
|320_320_eyenix_model|-|
|512_512_eyenix_model|-|
|640_640_eyenix_model|-|
***

&#160;

### :fire: How to apply Model 
#### This method is applied from EN675_SDK_V1.10.00R environment.  
1. Set UYVH and UYVV values in BSP/conf/videocore_hw.par to match the resolution of the model user want to use.
2. Download the bin file of the desired model and apply it.
3. User needs to match the path definition with the bin file in the BSP/spf/npu/testapp/src/npu_conf.h.


&#160;


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FEyenix%2Fen675_model_zoo&count_bg=%2379C83D&title_bg=%23555555&icon=pytorch.svg&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
