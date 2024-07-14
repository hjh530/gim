<p align="center">
  <a href="README.md"><img src="https://img.shields.io/badge/English-white" alt='English'></a>
  <a href="README.zh-CN-simplified.md"><img src="https://img.shields.io/badge/%E4%B8%AD%E6%96%87-white" alt='Chinese'></a>
</p>

<h2 align="center">GIM: Learning Generalizable Image Matcher From Internet Videos</h2>


<div align="center">
	<a href="https://www.youtube.com/embed/FU_MJLD8LeY">
		<img src="assets/demo/video.png" width="50%" alt="Overview Video">
	</a>
</div>
<p></p>

<div align="center">

<a href="https://iclr.cc/Conferences/2024"><img src="https://img.shields.io/badge/%F0%9F%8C%9F_ICLR'2024_Spotlight-37414c" alt='ICLR 2024 Spotlight'></a>
<a href="https://xuelunshen.com/gim"><img src="https://img.shields.io/badge/Project_Page-3A464E?logo=gumtree" alt='Project Page'></a>
<a href="https://arxiv.org/abs/2402.11095"><img src="https://img.shields.io/badge/arXiv-2402.11095-b31b1b?logo=arxiv" alt='arxiv'></a>
<a href="https://huggingface.co/spaces/xuelunshen/gim-online"><img src="https://img.shields.io/badge/%F0%9F%A4%97_Hugging_Face-Space-F0CD4B?labelColor=666EEE" alt='HuggingFace Space'></a>
<a href="https://www.youtube.com/watch?v=FU_MJLD8LeY"><img src="https://img.shields.io/badge/Overview_Video-E33122?logo=Youtube" alt='Overview Video'></a>
![GitHub Repo stars](https://img.shields.io/github/stars/xuelunshen/gim?style=social)

<!-- <a href="https://xuelunshen.com/gim"><img src="https://img.shields.io/badge/📊_Zero--shot_Image_Matching_Evaluation Benchmark-75BC66" alt='Zero-shot Evaluation Benchmark'></a> -->
<!-- <a href="https://xuelunshen.com/gim"><img src="https://img.shields.io/badge/Source_Code-black?logo=Github" alt='Github Source Code'></a> -->

<a href="https://en.xmu.edu.cn"><img src="https://img.shields.io/badge/XMU-183F9D?logo=Google%20Scholar&logoColor=white" alt='Intel'></a>
<a href="https://www.intel.com"><img src="https://img.shields.io/badge/Labs-0071C5?logo=intel" alt='Intel'></a>
<a href="https://www.dji.com"><img src="https://img.shields.io/badge/DJI-131313?logo=DJI" alt='Intel'></a>

</div>

|      | <div align="left">Method</div>                               | <div align="left">Mean<br />AUC@5°<br />(%) ↑</div> | GL3      | BLE      | ETI      | ETO      | KIT      | WEA      | SEA      | NIG      | MUL      | SCE      | ICL      | GTA      |
| ---- | ------------------------------------------------------------ | --------------------------------------------------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
|      |                                                              | Handcrafted                                         |          |          |          |          |          |          |          |          |          |          |          |          |
|      | RootSIFT                                                     | 31.8                                                | 43.5     | 33.6     | 49.9     | 48.7     | 35.2     | 21.4     | 44.1     | 14.7     | 33.4     | 7.6      | 14.8     | 35.1     |
|      |                                                              | Sparse Matching                                     |          |          |          |          |          |          |          |          |          |          |          |          |
|      | [SuperGlue](https://github.com/magicleap/SuperGluePretrainedNetwork) (in) | 21.6                                                | 19.2     | 16.0     | 38.2     | 37.7     | 22.0     | 20.8     | 40.8     | 13.7     | 21.4     | 0.8      | 9.6      | 18.8     |
|      | SuperGlue (out)                                              | 31.2                                                | 29.7     | 24.2     | 52.3     | 59.3     | 28.0     | 28.4     | 48.0     | 20.9     | 33.4     | 4.5      | 16.6     | 29.3     |
|      | **GIM_SuperGlue**<br />(50h)                                 | 34.3                                                | 43.2     | 34.2     | 58.7     | 61.0     | 29.0     | 28.3     | 48.4     | 18.8     | 34.8     | 2.8      | 15.4     | 36.5     |
|      | [LightGlue](https://github.com/cvg/LightGlue)                | 31.7                                                | 28.9     | 23.9     | 51.6     | 56.3     | 32.1     | 29.5     | 48.9     | 22.2     | 37.4     | 3.0      | 16.2     | 30.4     |
| ✅    | **GIM_LightGlue**<br />(100h)                                | **38.3**                                            | **46.6** | **38.1** | **61.7** | **62.9** | **34.9** | **31.2** | **50.6** | **22.6** | **41.8** | **6.9**  | **19.0** | **43.4** |
|      |                                                              | Semi-dense Matching                                 |          |          |          |          |          |          |          |          |          |          |          |          |
|      | [LoFTR](https://github.com/zju3dv/LoFTR) (in)                | 10.7                                                | 5.6      | 5.1      | 11.8     | 7.5      | 17.2     | 6.4      | 9.7      | 3.5      | 22.4     | 1.3      | 14.9     | 23.4     |
|      | LoFTR (out)                                                  | 33.1                                                | 29.3     | 22.5     | 51.1     | 60.1     | **36.1** | **29.7** | **48.6** | **19.4** | 37.0     | **13.1** | 20.5     | 30.3     |
| ✅    | **GIM_LoFTR**<br />(50h)                                     | **39.1**                                            | **50.6** | **43.9** | **62.6** | **61.6** | 35.9     | 26.8     | 47.5     | 17.6     | **41.4** | 10.2     | **25.6** | **45.0** |
|      | **GIM_LoFTR**<br />(100h)                                    | ToDO                                                |          |          |          |          |          |          |          |          |          |          |          |          |
|      |                                                              | Dense Matching                                      |          |          |          |          |          |          |          |          |          |          |          |          |
|      | [DKM](https://github.com/Parskatt/DKM) (in)                  | 46.2                                                | 44.4     | 37.0     | 65.7     | 73.3     | 40.2     | 32.8     | 51.0     | 23.1     | 54.7     | 33.0     | **43.6** | 55.7     |
|      | DKM (out)                                                    | 45.8                                                | 45.7     | 37.0     | 66.8     | 75.8     | 41.7     | 33.5     | 51.4     | 22.9     | 56.3     | 27.3     | 37.8     | 52.9     |
|      | **GIM_DKM**<br />(50h)                                       | 49.4                                                | 58.3     | 47.8     | 72.7     | 74.5     | 42.1     | **34.6** | 52.0     | **25.1** | 53.7     | 32.3     | 38.8     | 60.6     |
| ✅    | **GIM_DKM**<br />(100h)                                      | **51.2**                                            | **63.3** | **53.0** | **73.9** | 76.7     | **43.4** | **34.6** | **52.5** | 24.5     | 56.6     | 32.2     | 42.5     | **61.6** |
|      | [RoMa](https://github.com/Parskatt/RoMa) (in)                | 46.7                                                | 46.0     | 39.3     | 68.8     | 77.2     | 36.5     | 31.1     | 50.4     | 20.8     | 57.8     | **33.8** | 41.7     | 57.6     |
|      | RoMa (out)                                                   | 48.8                                                | 48.3     | 40.6     | 73.6     | **79.8** | 39.9     | 34.4     | 51.4     | 24.2     | **59.9** | 33.7     | 41.3     | 59.2     |
|      | **GIM_RoMa**                                                 | ToDO                                                |          |          |          |          |          |          |          |          |          |          |          |          |

> The data in this table comes from the **ZEB**: <u>Zero-shot Evaluation Benchmark for Image Matching</u> proposed in the paper. This benchmark consists of 12 public datasets that cover a variety of scenes, weather conditions, and camera models, corresponding to the 12 test sequences starting from GL3 in the table. We will release **ZEB** as soon as possible.

## ✅ TODO List

- [ ] Inference code
  - [ ] gim_roma
  - [x] gim_dkm
  - [x] gim_loftr
  - [x] gim_lightglue
- [ ] Training code

> We are actively continuing with the remaining open-source work and appreciate everyone's attention.

## 🤗 Online demo

Go to [Huggingface](https://huggingface.co/spaces/xuelunshen/gim-online) to quickly try our model online.

## ⚙️ Environment

I set up the running environment on a new machine using the commands listed below.
```bash
conda install pytorch==1.10.1 torchvision==0.11.2 torchaudio==0.10.1 cudatoolkit=11.3 -c pytorch -c conda-forge
pip install albumentations==1.0.1 --no-binary=imgaug,albumentations
pip install pytorch-lightning==1.5.10
pip install opencv-python==4.5.3.56
pip install imagesize==1.2.0
pip install kornia==0.6.10
pip install einops==0.3.0
pip install loguru==0.5.3
pip install joblib==1.0.1
pip install yacs==0.1.8
pip install h5py==3.1.0
```

## 🔨 Usage

Clone the repository

```bash
git clone https://github.com/xuelunshen/gim.git
cd gim
```

Download `gim_dkm` model weight from [Google Drive](https://drive.google.com/file/d/1gk97V4IROnR1Nprq10W9NCFUv2mxXR_-/view?usp=sharing)

Put it on the folder `weights`

Run the following command
```bash
python demo.py --model gim_dkm
```
or
```bash
python demo.py --model gim_loftr
```
or
```bash
python demo.py --model gim_lightglue
```

The code will match `a1.png` and `a2.png` in the folder `assets/demo`</br>, and output `a1_a2_match.png` and `a1_a2_warp.png`.

<details>
<summary>
	Click to show
	<code>a1.png</code>
	and
	<code>a2.png</code>.
</summary>
<p float="left">
  <img src="assets/demo/a1.png" width="25%" />
  <img src="assets/demo/a2.png" width="25%" /> 
</p>
</details>



<details>
<summary>
	Click to show
	<code>a1_a2_match.png</code>.
</summary>
<p align="left">
	<img src="assets/demo/_a1_a2_match.png" width="50%">
</p>
<p><code>a1_a2_match.png</code> is a visualization of the match between the two images</p>
</details>

<details>
<summary>
	Click to show
	<code>a1_a2_warp.png</code>.
</summary>
<p align="left">
	<img src="assets/demo/_a1_a2_warp.png" width="50%">
</p>
<p><code>a1_a2_warp.png</code> shows the effect of projecting <code>image a2</code> onto <code>image a1</code> using homography</p>
</details>

There are more images in the `assets/demo` folder, you can try them out.

<details>
<summary>
	Click to show other images.
</summary>
<p float="left">
  <img src="assets/demo/b1.png" width="15%" />
  <img src="assets/demo/b2.png" width="15%" /> 
  <img src="assets/demo/c1.png" width="15%" />
  <img src="assets/demo/c2.png" width="15%" /> 
  <img src="assets/demo/d1.png" width="15%" />
  <img src="assets/demo/d2.png" width="15%" /> 
</p>
</details>

## 📌 Citation

If the paper and code from `gim` help your research, we kindly ask you to give a citation to our paper ❤️. Additionally, if you appreciate our work and find this repository useful, giving it a star ⭐️ would be a wonderful way to support our work. Thank you very much.

```bibtex
@inproceedings{
xuelun2024gim,
title={GIM: Learning Generalizable Image Matcher From Internet Videos},
author={Xuelun Shen and Zhipeng Cai and Wei Yin and Matthias Müller and Zijun Li and Kaixuan Wang and Xiaozhi Chen and Cheng Wang},
booktitle={The Twelfth International Conference on Learning Representations},
year={2024}
}
```

## 🌟 Star History

<a href="https://star-history.com/#xuelunshen/gim&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=xuelunshen/gim&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=xuelunshen/gim&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=xuelunshen/gim&type=Date" />
  </picture>
</a>

## License

This repository is under the MIT License. This content/model is provided here for research purposes only. Any use beyond this is your sole responsibility and subject to your securing the necessary rights for your purpose. 
