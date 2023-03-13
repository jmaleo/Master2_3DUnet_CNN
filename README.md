# Master2_3DUnet_CNN

This project is a fork of the [3DUnet_CNN](https://github.com/ellisdg/3DUnetCNN) only used to train the model on the AutoImplant2020 dataset and the Brats2020 dataset. Also, we have tested pre trained models on the BraTs dataset.

This fork is presented as part of a computer project in Master 2 Computer Science at Toulouse III Paul Sabatier.

# Authors of this short fork
- Lou Denis
- Léo Arnal--Anger

## Prerequisites

Download the original repository from [3DUnet_CNN](https://github.com/ellisdg/3DUnetCNN).

You'll also need to install pre trained model from [3DUnet_CNN_pretrained_models](https://zenodo.org/record/4289225#.ZA9LRtLMJkg).
We essentially used the model with size 176x224x144.

## Explaination

There is 2 directories provided in this repository. In each of them, you can find a readme file that explain how to train the model on the AutoImplant2020 dataset and the Brats2020 dataset. Also, we have tested pre trained models on the BraTs dataset.
You just have to follow the readme file in the directory you want to use, and copy and paste the files into the given examples/ directory from the original repository.

## Installation

You must install [PyTorch](https://pytorch.org/get-started/locally/) and [nilearn](https://nilearn.github.io/stable/quickstart.html).

```bash
git clone git@github.com:ellisdg/3DUnetCNN.git
cd 3DUnetCNN
```

### Datasets AutoImplant2020

Download the [AutoImplant2020](https://zenodo.org/record/4270278#.ZA9FqNLMJkg) dataset and put it into the 'examples/autoimplant2020/augmented/' folder from the original repository.

You must have the following structure:
```bash
├── examples
│   ├── autoimplant2020
│   │   ├── augmented
│   │   │   ├── augmented_complete_skull
│   │   │   ├── augmented_complete_skull
│   │   │   └── augmented_implant
```

In order to train it, just for one epoch (4h30 with an RTX 3080 and 3.5 to 5gHz 20 threads CPU), you can follow the readme, updated with our tests, in the folder 'autoimplant2020/'.

### Datasets Brats2020

Download the [BraTS2020](https://www.kaggle.com/datasets/awsaf49/brats2020-training-data) dataset and put it into the 'examples/brats2020/' folder from the original repository.

You must have the following structure:
```bash
    ├── examples
    │   ├── brats2020
    │   │   ├── MICCAI_BraTS2020_TrainingData
    │   │   │   ├── BraTS20_Training_{subject}
    │   │   │   │   ├── BraTS20_Training_{subject}_flair.nii.gz
    │   │   │   │   ├── BraTS20_Training_{subject}_t1.nii.gz
    │   │   │   │   ├── BraTS20_Training_{subject}_t1ce.nii.gz
    │   │   │   │   ├── BraTS20_Training_{subject}_t2.nii.gz
    │   │   │   │   ├── BraTS20_Training_{subject}_seg.nii.gz
```
In order to train it, just for one epoch (30minutes to 1 hours with an RTX 3080 and 3.5 to 5gHz 20 threads CPU), you can follow the readme, updated with our tests, in the folder 'brats2020/'.
