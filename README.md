# LGFC

Local-Global Feature Collaborative Learning with Level-Wise Decoding for Infrared Small Target Detection

Currently, it is still in the process of refinement. After the formal publication of the paper, the code will be further improved.
![frame](https://github.com/user-attachments/assets/475b242e-6300-4ebd-9315-5d6364ce760d)


## Introduction

Due to low signal-to-noise ratio, weak vision contrast and small size, infrared small targets are prone to be overwhelmed by backgrounds. Therefore, capturing long-distance dependencies of images and acquiring the semantically-distinctive features between targets and backgrounds are pretty crucial. Currently-existing detection methods are generally based on convolutions. Due to the inherent locality of convolutions, the expectation to capture a global range of contextual relationships is often challenging to implement. To address the vital issue of local-global feature utilization, we propose a Multi-scale Vision Transformer with Level-wise Decoding (MViT-LD) scheme, integrating convolution and ViT in a multi-level cascade to capture the local details and global contextual information of infrared small targets. Moreover, we improve the self-attention mechanism of ViT by refining the local features captured by Local Window Attention to highlight small targets. Besides, more attention is paid to the nearby regions while acquiring the extensive dependencies through the Global Axial Attention with Gaussian masks. To avoid feature loss in decoding, we specially design a level-wise decoding group with Cross-layer Feature Interaction to retain more target information, instead of skip-connection in the tradition structure of U-Net. Finally, considering the shapes and boundaries of infrared small targets, we propose a Coarse-to-Fine Refinement to refine rear decoding to obtain more accurate detection results. The experiments show the superiority and generalization ability of our MViT-LD over state-of-the-art methods.

## Datasets

- Datasets are available at [NUAA-SIRST](https://github.com/YimianDai/sirst) and [IRSTD-1K](https://github.com/RuiZhang97/ISNet)

## Prerequisite

- python == 3.8
- pytorch == 1.10.0
- einops == 0.7.0
- opencv-python == 4.7.0.72
- scikit-learn == 1.2.2
- scipy == 1.9.1
- Tested on Ubuntu 20.04.6, with CUDA 12.0, and 1x NVIDIA 3090(24 GB)

## ROC curves
![roc](https://github.com/user-attachments/assets/f93a5940-12ad-495d-9786-ccad58e3642c)

## Contact

IF any questions, please contact with Weiwei Duan via email: [dwwuestc@163.com]().

## Reference

- Li, Boyang, et al. "Dense nested attention network for infrared small target detection." IEEE Transactions on Image Processing 32 (2022): 1745-1758.
- Lin, Jian, et al. "IR-TransDet: Infrared Dim and Small Target Detection With IR-Transformer." IEEE Transactions on Geoscience and Remote Sensing (2023).
