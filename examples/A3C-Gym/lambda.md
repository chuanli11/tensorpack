Installation
===

```bash
sudo pip3 install virtualenv

cd tensorpack
virtualenv -p /usr/bin/python3.6 venv-a3c
. venv-a3c/bin/activate

pip install --upgrade git+https://github.com/tensorpack/tensorpack.git

cd examples/A3C-Gym

pip install -r requirements.txt 

pip install gym[atari]
```

Train
===
```bash
python train-atari.py --env Breakout-v0 --gpu 0
```


**Memory Requirement (MiB)**


| Batch Size  | Memory  |
|---|---|
| bs=64 |  |
| bs=128 |  |
| bs=256 |  |
| bs=512 |  |
| bs=1024 |  |

**Throughput (iteration * BS/sec)** 

|   | 2060  | 2070  | 2080  |  1080 Ti | 2080 Ti | TitanRTX | Quadro RTX 6000 | V100 | Quadro RTX 8000 |
|---|---|---|---|---|---|---|---|---|---|
| bs=64 |  |  |  |  |  |  |  |  |  |
| bs=128 |  |  |  |  |  |  | 1600 |  | 1544 |
| bs=256 |  |  |  |  |  |  |  |  |  |
| bs=512 |  |  |  |  |  |  |  |  |  |
| bs=1024 |  |  |  |  |  |  |  |  |  |

