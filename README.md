# deep-person-reid
This repo contains [pytorch](http://pytorch.org/) implementations of deep person re-identification approaches.

We will actively maintain this repo.

## Pretrained models
## Prepare data
Create a directory to store reid datasets under this repo via `mkdir data/`.

Market1501 [7]:
1. download dataset to `data/` from http://www.liangzheng.org/Project/project_reid.html.
2. extract dataset and rename to `market1501`.

MARS [8]:
1. create a directory named `mars/` under `data/`.
2. download dataset to `data/mars/` from http://www.liangzheng.com.cn/Project/project_mars.html.
3. extract `bbox_train.zip` and `bbox_test.zip`.
4. download split information from https://github.com/liangzheng06/MARS-evaluation/tree/master/info and put `info/` in `data/mars`. (we want to follow the standard split in [8])
## Train
## Test
## Results
### Setup
* Image size: 256-by-128 <br />
* Optimizer: Adam [6] <br />
* Loss functions: <br />
xent: cross entropy + label smoothing regularizer [5] <br />
htri: triplet loss with hard positive/negative mining [4] <br />

### Market1501

| Model | Size (M) | Loss | Rank-1 / -5 / -10 (%) | mAP (%) | Reported Rank | Reported mAP |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| ResNet50 [1] | 25.05 | xent | 85.8 / 94.4 / 96.3 | 70.1 | | |
| ResNet50M [2] | 30.01 | xent | 88.8 / 95.3 / 97.0 | 74.4 | 89.9 / - / -  | 75.6 |
| DenseNet121 [3] | 7.72 | xent | | | | |

## References
[1] [He et al. Deep Residual Learning for Image Recognition. CVPR 2016.](https://arxiv.org/abs/1512.03385)<br />
[2] [Yu et al. The Devil is in the Middle: Exploiting Mid-level Representations for Cross-Domain Instance Matching. arXiv:1711.08106.](https://arxiv.org/abs/1711.08106) <br />
[3] [Huang et al. Densely Connected Convolutional Networks. CVPR 2017.](https://arxiv.org/abs/1608.06993) <br />
[4] [Hermans et al. In Defense of the Triplet Loss for Person Re-Identification. arXiv:1703.07737.](https://arxiv.org/abs/1703.07737) <br />
[5] [Szegedy et al. Rethinking the Inception Architecture for Computer Vision. CVPR 2016.](https://arxiv.org/abs/1512.00567) <br />
[6] [Kingma and Ba. Adam: A Method for Stochastic Optimization. ICLR 2015.](https://arxiv.org/abs/1412.6980) <br />
[7] [Zheng et al. Scalable Person Re-identification: A Benchmark. ICCV 2015.](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Zheng_Scalable_Person_Re-Identification_ICCV_2015_paper.pdf) <br />
[8] [Zheng et al. MARS: A Video Benchmark for Large-Scale Person Re-identification. ECCV 2016.](http://www.liangzheng.com.cn/Project/project_mars.html) <br />