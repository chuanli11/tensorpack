Installation
===

```bash
sudo pip3 install virtualenv

cd tensorpack
virtualenv -p /usr/bin/python3.6 venv-maskrcnn
. venv-maskrcnn/bin/activate

pip install --upgrade git+https://github.com/tensorpack/tensorpack.git

cd examples/FasterRCNN

pip install -r requirements.txt 

git clone https://github.com/cocodataset/cocoapi.git
cd cocoapi/PythonAPI
make install
```

Train
===

```bash

CUDA_VISIBLE_DEVICES=0 ./train.py --config \
    MODE_MASK=True MODE_FPN=True \
    DATA.BASEDIR=/home/ubuntu/demo/data/coco \
    BACKBONE.WEIGHTS=/home/ubuntu/demo/model/ImageNet-R50-AlignPadding.npz
```


**Memory Requirement (MiB)**

| Batch Size  | Memory  |
|---|---|
| bs=1 |   |
| bs=2 |   |
| bs=4 |   |
| bs=8 |   |

**Throughput (samples/sec)** 

|   | 2060  | 2070  | 2080  |  1080 Ti | 2080 Ti | TitanRTX | Quadro RTX 6000 | V100 | Quadro RTX 8000 |
|---|---|---|---|---|---|---|---|---|---|
| bs=1  |   |   |   |   |   |   |   |   |   |
| bs=2  |   |   |   |   |   |   |   |   |   |
| bs=4  |   |   |   |   |   |   |   |   |   |
| bs=8  |   |   |   |   |   |   |   |   |   |


500 images
1080Ti: 02:00
2080: 01:55
Quadro RTX 6000: 01:25
Quadro RTX 8000: 01:24
