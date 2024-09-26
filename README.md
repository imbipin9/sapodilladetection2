# sapodilla detection
Sapodilla fruit detection using YoloV4, with support for training inference & evaluation

## Installation
### Installing from source

For normal training and evaluation we recommend installing the package from source 
```bash
git clone https://github.com/imbipin9/sapodilladetection2.git 
cd sapodilladetection2
pip3 install -r requirements.txt
```

#### Download dataset

Dataset can be downloaded from https://drive.google.com/file/d/1F_yVqQ0w-eAqAqFrwGDuSl3eaH4v_HL9/view?usp=sharing
Extract dataset
'''bash
tar xvzf dataset.tar
'''
#### Download pretrained checkpoint

Pre-trained checkpoint can be downloaded from https://drive.google.com/file/d/1CKrt91np_fMaubEr5KBSAjA8wR83cjNd/view?usp=sharing 

'''bash
ls checkpoint.pth
'''

#### Custom model

```bash
ls yolov4.yaml
```

#### Custom dataset path in custom.yaml

'''bash
ls custom.yaml
'''

#### Train
To train on the custom dataset run:

```bash
python train.py --config-file yolov4.yaml --data custom.yaml --weights "" 

```
#### Inference
To run inference 
'''bash
python detect.py --config-file yolov4.yaml  --data custom.yaml --weights weights/checkpoint.pth  --source dataset/v2/images/  --output ./output
'''


