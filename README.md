# YOLOv5 - Oriented Object Detection - Tracking

# Installation
## Requirements
* Linux, Windows
* Python 3.7+ 
* PyTorch ≥ 1.7 and < 1.11
* CUDA 9.0 or higher

## Install 
a. Create a conda virtual environment and activate it, e.g.,
```
conda create -n yolo python=3.9 -y 
conda activate yolo
```
b. Make sure your CUDA runtime api version ≤ CUDA driver version. (for example 11.3 ≤ 11.4)
```
nvcc -V
nvidia-smi
```
c. Install PyTorch and torchvision following the [official instructions](https://pytorch.org/), Make sure cudatoolkit version same as CUDA runtime api version, e.g.,
```
pip3 install torch==1.10.1+cu113 torchvision==0.11.2+cu113 torchaudio==0.10.1+cu113 -f https://download.pytorch.org/whl/cu113/torch_stable.html
nvcc -V
python
>>> import torch
>>> torch.version.cuda
>>> exit()
```
d. Clone the yolov5-obb-tracking repository.
```
git clone https://github.com/opnuub/yolov5-obb-tracking.git
cd yolov5-obb-tracking
```
e. Install yolov5-obb-tracking.

```python 
pip install -r requirements.txt
cd utils/nms_rotated
python setup.py develop  #or "pip install -v -e ."
```


## Acknowledgements
This repository is based on https://github.com/hukaixuan19970627/yolov5_obb.
