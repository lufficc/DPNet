# Data Priming Network for Automatic Check-Out

Introduction
-----------------
This paper was accepted to ACM MM 2019.

This repository implements DPNet ([Data Priming Network for Automatic Check-Out](https://arxiv.org/abs/1904.04978)) using PyTorch 1.0.1 . This implementation is heavily influenced by the project [maskrcnn-benchmark](https://github.com/facebookresearch/maskrcnn-benchmark).

We propose a new data priming method
to solve the domain adaptation problem. Specifically, we first use
pre-augmentation data priming, in which we remove distracting
background from the training images using the coarse-to-fine strategy and select images with realistic view angles by the pose pruning
method. In the post-augmentation step, we train a data priming
network using detection and counting collaborative learning, and
select more reliable images from testing data to fine-tune the final
visual item tallying network.

![DPNet](DPNet.png)

## Code

Source code and more details are available [here](https://isrc.iscas.ac.cn/gitlab/research/acm-mm-2019-ACO).


## Results

![DPNet](results.png)

|    level |      method        |   cAcc |  mCIoU |  ACD | mCCD |  mAP50 |   mmAP |
|     ---: |               ---: |   ---: |   ---: | ---: | ---: |   ---: |   ---: |
|     easy | Syn+Render (DPNet) | 90.32% | 97.87% | 0.15 | 0.02 |  98.6% | 83.07% |
|   medium | Syn+Render (DPNet) | 80.68% | 97.38% | 0.32 | 0.03 | 98.07% | 77.25% |
|     hard | Syn+Render (DPNet) | 70.76% | 97.04% | 0.53 | 0.03 | 97.76% | 74.95% |
| averaged | Syn+Render (DPNet) | 80.51% | 97.33% | 0.34 | 0.03 | 97.91% | 77.04% |

## Citations
Please cite this project in your publications if it helps your research. 
```
@inproceedings{li2019data,
  title={Data Priming Network for Automatic Check-Out},
  author={Li, Congcong and Du, Dawei and Zhang, Libo and Luo, Tiejian and Wu, Yanjun and Tian, Qi and Wen, Longyin and Lyu, Siwei},
  booktitle={2019 ACM Multimedia Conference on Multimedia Conference},
  year={2019},
  organization={ACM}
}
```