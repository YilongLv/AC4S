# Adaptively Center-Shape Sensitive Sample Selection for Ship Detection in SAR Images

With the wide application of synthetic aperture radar in maritime surveillance, a ship detection method has been rapidly developed. However, there is still a key problem common in most methods, i.e., how to select positive and negative samples. The mainstream MaxIoUAssign has inherent problems, such as a fixed threshold and rough classification, resulting in the low quality of the positive samples. To solve these problems, we propose a new sample selection method called adaptively center-shape sensitive sample selection (AC4S). The proposed method introduces shape similarity between proposal boxes and ground truth as one of the evaluation criteria and collaborates with Intersection of Union(IoU) to measure the quality of the proposal boxes. Meanwhile, the center distance between proposal boxes and ground truth is used to control the influence degree of IoU and shape similarity. In this way, the quality score of the proposal boxes can be determined through IoU, shape similarity, and center position, making sample selection more comprehensive. Additionally, to avoid a fixed threshold, the standard deviation of the quality score is used as a variable to form the adaptive threshold. Finally, we conducted extensive experiments on the benchmark SSDD and HRSID datasets. The experimental results demonstrated the superiority of our method.


## Installation

Please refer to [get_started.md](docs/get_started.md) for installation.

## Get Started

Please see [get_started.md](docs/get_started.md) for the basic usage of MMDetection.

## Quick start to train the model

```

# Training on multiple GPUs. eg: 8 GPUs
bash ./tools/dist_train.sh /mmdetection-master/configs/ac4s/ac4s_faster_rcnn_r50_fpn_1x_ssdd 8

# Training on a single GPU
python tools/train.py /mmdetection-master/configs/ac4s/ac4s_faster_rcnn_r50_fpn_1x_ssdd

```

## Acknowledgement

Thanks to MMDetection Team for their powerful deep learning detection framework.


