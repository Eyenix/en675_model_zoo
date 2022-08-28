
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

|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Max)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|-|-|-|
|512_512_eyenix_model_v1|-|-|-|-|-|
|640_640_eyenix_model_v1|-|-|-|-|-|

&#160;

**class** : Face  
<figure>
    <img src="./img/face_image.PNG" title="face">    
</figure>

|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Max)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|-|-|-|
|512_512_eyenix_model_v1|-|-|-|-|-|
|640_640_eyenix_model_v1|-|-|-|-|-|

&#160;

#### :arrow_forward: Classification (TBD)
**class** : -
|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Max)|
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
|Model|mAP|
|:-----:|:---:|
|320_320_eyenix_model_v1|0.752|
|512_512_eyenix_model_v1|0.782|
|640_640_eyenix_model_v1|-|

&#160;

:+1: Train Dataset : COCO 2017 (train, val) (TBD)  
:+1: Test Dataset : COCO 2017 (test)
|Model|mAP|
|:-----:|:---:|
|320_320_eyenix_model_v1|-|
|512_512_eyenix_model_v1|-|
|640_640_eyenix_model_v1|-|

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

&#160;

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FEyenix%2Fen675_model_zoo&count_bg=%2379C83D&title_bg=%23555555&icon=pytorch.svg&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
