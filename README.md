# Track_reid_zsw

## Introduction
A multi object detect and track Library Based on tensorrt

一个基于TensorRT的多目标检测和跟踪融合算法库，可以同时支持行人的多目标检测和跟踪，当然也可以仅仅当检测库使用。

本算法的主框架采用了JDE+deepsort结构，其中由JDE算法检测出人的坐标与其对应的外观特征，然后基于deepsort的方法进行目标与运动轨迹的匹配。
JDE中的检测框架则采用了YOLOV5 L 的模型结构。
主要参考了下面四篇工作
## Reference
* JDE: https://arxiv.org/pdf/1909.12605v1.pdf
* CSTrack: https://arxiv.org/pdf/2010.12138.pdf
* YOLOV5: https://github.com/ultralytics/yolov5
* DeepSort: https://arxiv.org/pdf/1703.07402.pdf

## Requirements
* ubuntu 18.04 for x86
* gcc/g++ >= 7.5.0  
* opencv >= 3.4.8
* cuda >=10.0  cudnn >= 7.6
* tensorRT >= 7.0.0
* (Optional) ffmpeg (used in the video demo)

## How to build and run
* modify track/CMakeLists.txt Change opencv and tensorRT to your local directory
* modify demo/CMakeLists.txt Change opencv and tensorRT to your local directory
* modify demo/src/main.cpp Change video path to your local directory
* sh make.sh
* cd demo/build
* ./itest



