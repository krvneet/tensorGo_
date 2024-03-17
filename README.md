## ESRGAN (Enhanced SRGAN) [:rocket: [BasicSR](https://github.com/xinntao/BasicSR)] [[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)]

:sparkles: **New Updates.**

We have extended ESRGAN to [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN), which is a **more practical algorithm for real-world image restoration**. For example, it can also remove annoying JPEG compression artifacts. <br> You are recommended to have a try :smiley:

In the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) repo,

- You can still use the original ESRGAN model or your re-trained ESRGAN model. [The model zoo in Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN#european_castle-model-zoo).
- We provide a more handy inference script, which supports 1) **tile** inference; 2) images with **alpha channel**; 3) **gray** images; 4) **16-bit** images.
- We also provide a **Windows executable file** `RealESRGAN-ncnn-vulkan` for easier use without installing the environment. This executable file also includes the original ESRGAN model.
- The full training codes are also released in the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) repo.

Welcome to open issues or open discussions in the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) repo.

- If you have any question, you can open an issue in the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) repo.
- If you have any good ideas or demands, please open an issue/discussion in the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) repo to let me know.
- If you have some images that Real-ESRGAN could not well restored, please also open an issue/discussion in the [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) repo. I will record it (but I cannot guarantee to resolve it😛).

Here are some examples for Real-ESRGAN:

<p align="center">
  <img src="https://raw.githubusercontent.com/xinntao/Real-ESRGAN/master/assets/teaser.jpg">
</p>
:book: Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data

> [[Paper](https://arxiv.org/abs/2107.10833)] <br>
> [Xintao Wang](https://xinntao.github.io/), Liangbin Xie, [Chao Dong](https://scholar.google.com.hk/citations?user=OSDCB0UAAAAJ), [Ying Shan](https://scholar.google.com/citations?user=4oXBp9UAAAAJ&hl=en) <br>
> Applied Research Center (ARC), Tencent PCG<br>
> Shenzhen Institutes of Advanced Technology, Chinese Academy of Sciences

-----

As there may be some repos have dependency on this ESRGAN repo, we will not modify this ESRGAN repo (especially the codes).

The following is the original README:

#### The training codes are in :rocket: [BasicSR](https://github.com/xinntao/BasicSR). This repo only provides simple testing codes, pretrained models and the network interpolation demo.

[BasicSR](https://github.com/xinntao/BasicSR) is an **open source** image and video super-resolution toolbox based on PyTorch (will extend to more restoration tasks in the future). <br>
It includes methods such as **EDSR, RCAN, SRResNet, SRGAN, ESRGAN, EDVR**, etc. It now also supports **StyleGAN2**.

### Enhanced Super-Resolution Generative Adversarial Networks
By Xintao Wang, [Ke Yu](https://yuke93.github.io/), Shixiang Wu, [Jinjin Gu](http://www.jasongt.com/), Yihao Liu, [Chao Dong](https://scholar.google.com.hk/citations?user=OSDCB0UAAAAJ&hl=en), [Yu Qiao](http://mmlab.siat.ac.cn/yuqiao/), [Chen Change Loy](http://personal.ie.cuhk.edu.hk/~ccloy/)

We won the first place in [PIRM2018-SR competition](https://www.pirm2018.org/PIRM-SR.html) (region 3) and got the best perceptual index.
The paper is accepted to [ECCV2018 PIRM Workshop](https://pirm2018.org/).

:triangular_flag_on_post: Add [Frequently Asked Questions](https://github.com/xinntao/ESRGAN/blob/master/QA.md).

> For instance,
> 1. How to reproduce your results in the PIRM18-SR Challenge (with low perceptual index)?
> 2. How do you get the perceptual index in your ESRGAN paper?

#### BibTeX

    @InProceedings{wang2018esrgan,
        author = {Wang, Xintao and Yu, Ke and Wu, Shixiang and Gu, Jinjin and Liu, Yihao and Dong, Chao and Qiao, Yu and Loy, Chen Change},
        title = {ESRGAN: Enhanced super-resolution generative adversarial networks},
        booktitle = {The European Conference on Computer Vision Workshops (ECCVW)},
        month = {September},
        year = {2018}
    }

<p align="center">
  <img src="figures/baboon.jpg">
</p>

The **RRDB_PSNR** PSNR_oriented model trained with DF2K dataset (a merged dataset with [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/) and [Flickr2K](http://cv.snu.ac.kr/research/EDSR/Flickr2K.tar) (proposed in [EDSR](https://github.com/LimBee/NTIRE2017))) is also able to achive high PSNR performance.

| <sub>Method</sub> | <sub>Training dataset</sub> | <sub>Set5</sub> | <sub>Set14</sub> | <sub>BSD100</sub> | <sub>Urban100</sub> | <sub>Manga109</sub> |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| <sub>[SRCNN](http://mmlab.ie.cuhk.edu.hk/projects/SRCNN.html)</sub>| <sub>291</sub>| <sub>30.48/0.8628</sub> |<sub>27.50/0.7513</sub>|<sub>26.90/0.7101</sub>|<sub>24.52/0.7221</sub>|<sub>27.58/0.8555</sub>|
| <sub>[EDSR](https://github.com/thstkdgus35/EDSR-PyTorch)</sub> | <sub>DIV2K</sub> | <sub>32.46/0.8968</sub> | <sub>28.80/0.7876</sub> | <sub>27.71/0.7420</sub> | <sub>26.64/0.8033</sub> | <sub>31.02/0.9148</sub> |
| <sub>[RCAN](https://github.com/yulunzhang/RCAN)</sub> |  <sub>DIV2K</sub> | <sub>32.63/0.9002</sub> | <sub>28.87/0.7889</sub> | <sub>27.77/0.7436</sub> | <sub>26.82/ 0.8087</sub>| <sub>31.22/ 0.9173</sub>|
|<sub>RRDB(ours)</sub>| <sub>DF2K</sub>| <sub>**32.73/0.9011**</sub> |<sub>**28.99/0.7917**</sub> |<sub>**27.85/0.7455**</sub> |<sub>**27.03/0.8153**</sub> |<sub>**31.66/0.9196**</sub>|

## Quick Test
#### Dependencies
- Python 3
- [PyTorch >= 1.0](https://pytorch.org/) (CUDA version >= 7.5 if installing with CUDA. [More details](https://pytorch.org/get-started/previous-versions/))
- Python packages:  `pip install numpy opencv-python`

