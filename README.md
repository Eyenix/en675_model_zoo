
<img alt="Python" src ="https://img.shields.io/badge/python-3.8-orange"/>


## EN675 NPU Model Zoo
The EN675 Series SoC Model Zoo privides the trained models for AI Object Detection (OD) and Classification (CLS) applications.  
:rocket: EN675 NPU Spec Link : [EYENIX EN675 NPU Spec & Demo](https://resonant-duke-420.notion.site/EN675-AI-NPU-Solution-d407c17992d8447b9c98ac2bfede8cdb)
***
&#160;
## New Release
### :star::star::star:A modified *yolov7-tiny* model is available. eyenix_model_v2 is a modified model based on yolov7-tiny.:star::star::star:
&#160;
### :star: Download
#### :arrow_forward: Object Detection
**classes** : Person, Bicycle, Motorbike, Car, Bus, Truck  
<figure>
    <img src="./img/6classes_image.PNG" title="6class">    
</figure>

|Model|ONNX|Compile Results|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|[320_320_eyenix_model_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9623478/320_320_eyenix_model_v1.zip)|[od6class_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9623476/od6class_320.zip)|[od6class_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812959/od6class_320.zip)|11MB|26ms|13ms|
|512_512_eyenix_model_v1|[512_512_eyenix_model_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9466030/512_512_eyenix_model_v1.zip)|[od6class_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9466035/od6class_512.zip)|[od6class_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812963/od6class_512.zip)|18MB|37ms|20ms|
|640_640_eyenix_model_v1|[640_640_eyenix_model_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9485742/640_640_eyenix_model_v1.zip)|[od6class_640.bin](https://github.com/Eyenix/en675_model_zoo/files/9485743/od6class_640.zip)|[od6class_640.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812969/od6class_640.zip)|25MB|54ms|29ms|
|672_384_eyenix_model_v2|[672_384_eyenix_model_v2.onnx](https://github.com/Eyenix/en675_model_zoo/files/12256208/672_384_eyenix_model_v2.zip)|[od6class_672_384.bin](https://github.com/Eyenix/en675_model_zoo/files/12459169/od6class_672_384.zip)|[od6class_672_384.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812971/od6class_672_384.zip)|22MB|63ms|28ms|


&#160;

**class** : Face  
<figure>
    <img src="./img/face_image.PNG" title="face">    
</figure>

|Model|ONNX|Compile Results|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_face_v1|[320_320_eyenix_model_face_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9925051/320_320_eyenix_model_face_v1.zip)|[face_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9925058/face_320.zip)|[face_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813033/face_320.zip)|12MB|22ms|11ms|
|448_448_eyenix_model_face_v1|[448_448_eyenix_model_face_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9925055/448_448_eyenix_model_face_v1.zip)|[face_448.bin](https://github.com/Eyenix/en675_model_zoo/files/9925059/face_448.zip)|[face_448.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813035/face_448.zip)|23MB|50ms|20ms|
|512_512_eyenix_model_face_v1|[512_512_eyenix_model_face_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9925056/512_512_eyenix_model_face_v1.zip)|[face_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9925060/face_512.zip)|[face_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813036/face_512.zip)|31MB|68ms|28ms|  
|512_288_eyenix_model_face_v2|[512_288_eyenix_model_face_v2.onnx](https://github.com/Eyenix/en675_model_zoo/files/12256218/512_288_eyenix_model_face_v2.zip)|[face_512_288.bin](https://github.com/Eyenix/en675_model_zoo/files/12459171/face_512_288.zip)|[face_512_288.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813038/face_512_288.zip)|14MB|38ms|17ms|


**caution** : For the eyenix_face model_v1, the confidence score max is 64 instead of 256. User needs to change the value of the ClassConfTH array in npu_conf.c

&#160;

### :trophy: Performance
#### :arrow_forward: Object Detection
:+1: Train Dataset : PASCAL VOC 2007 (train, val), PASCAL VOC 2012 (train, val)  
:+1: Test Dataset : PASCAL VOC 2007 (test)
|Model|mAP at IOU = 0.50 (GPU)|mAP at IOU = 0.50 (NPU)| test file |
|:-----:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|74.5|73.3|[VOC320_quantized.zip](https://github.com/Eyenix/en675_model_zoo/files/9669475/VOC320_quantized.zip)|
|512_512_eyenix_model_v1|77.0|75.5|[VOC512_quantized.zip](https://github.com/Eyenix/en675_model_zoo/files/9642077/VOC512_quantized.zip)|
|640_640_eyenix_model_v1|79.2|77.5|[VOC640_quantized.zip](https://github.com/Eyenix/en675_model_zoo/files/9642078/VOC640_quantized.zip)|

&#160;

:+1: Train Dataset : COCO 2017 (train) 
:+1: Test Dataset : COCO 2017 (val)
|Model|mAP at IOU = 0.50:0.95 (GPU)|mAP at IOU = 0.50:0.95 (NPU)| mAP at IOU = 0.50 (GPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|:---:|:---:|
|640_352_eyenix_model_v2|33.4|27.5|49.9|44.9|
|832_480_eyenix_model_v2|36.9|29.1|54.8|48.2|

&#160;

### :clapper:promotion (DEMO)
#### :arrow_forward: Parking lot solution
![Parking_lot solution](https://user-images.githubusercontent.com/66294848/188069884-3441a15f-2a91-477a-b8d1-6337c931c25d.gif)

&#160;


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FEyenix%2Fen675_model_zoo&count_bg=%2379C83D&title_bg=%23555555&icon=pytorch.svg&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
