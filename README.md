# Rethinking the Quality of High-Activity Enhancer Generation: A Multi-Agent Collaborative Framework under Long Tail Constraints

## 1. Environment setup

1.1 Install torch

```
conda create -n ReMAC python=3.9
conda activate ReMAC
pip install conda install pytorch==2.3.1 torchvision==0.18.1 torchaudio==2.3.1 pytorch-cuda=12.1 -c pytorch -c nvidia
```

1.2 Install gReLU

To install from source:

```
git clone https://github.com/Genentech/gReLU.git
cd gReLU
pip install .
```

To install using pip:

```
pip install gReLU
```

The rest of the libraries can be installed by default.

## 2. File descriptions

ga.py：Article experiments section code

main_gosai.py：Article experiments section code

train_enhancer.py：The path where the dataset is stored

finetune_reward.py：Diffusion model code

## 3. Run

Get the dataset

huggingface path:(https://huggingface.co/datasets/a1271390389/enhancer_249/tree/main)

Train diffusion model

```
python main_gosai.py
```

Train fitness predicitor

```
python train_enhancer.py
```

Finetune diffusion model

```
train finetune_reward_bp.py
```




#### 
