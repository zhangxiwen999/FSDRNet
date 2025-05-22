# FSDRNet：A Dynamic Recovery Network Based on Frequency-Spatial Collaborative Processing
# ABSTRACT
In traditional image restoration research, various image degradation types are typically treated as independent tasks, neglecting the intrinsic connections between degradation phenomena. Although All-in-one models have made progress in handling multiple degradation types within a single network, these methods still fail to fully exploit the correlations between different degradation types, limiting their ability to address complex scenarios. This paper proposes a Frequency-Spatial Collaborative Dynamic Recovery Network (FSDRNet) that achieves efficient image restoration through multi-domain collaborative feature enhancement and dynamic routing processing. In the feature enhancement stage, the spatial feature processing module employs a balanced feature mixing attention mechanism (EFMA) to precisely characterize local textures, while the frequency domain auxiliary module extracts global structural patterns through Fourier transforms and transmits key information to the spatial module via degradation guidance signals, establishing a unidirectional enhancement mechanism. In the dynamic processing stage, the network adaptively adjusts parameters according to degradation types and achieves precise restoration through physically-guided specialized filters. Extensive experiments demonstrate that FSDRNet achieves excellent performance across multiple tasks including denoising, deblurring, dehazing, deraining, and low-light enhancement, with an average PSNR of 28.52dB, while exhibiting significant generalization capability for unknown compound degradation. 
<div align="center">
    <img src="Fig1.png" alt="FSDRNet Model Architecture" width="800"/>
</div>
Fig. 1. Spatial-Spectral Dual-Domain Framework for Degradation Selection and Image Restoration. The framework integrates spatial domain processing with spectral analysis to identify and address multiple degradation types (S, Mix, I, K) with corresponding restoration strategies.

# Environment Requirements
<pre>
python==3.9.21
torch==1.11.0+cu113
torchvision==0.12.0+cu113
torchaudio==0.11.0+cu113
</pre>
#### The additional environment can be downloaded via the following commands:FSDRNet-main
<pre>
pip install -r requirements.txt
</pre>

# Datasets
FSDRNet was trained and evaluated on the following public datasets:

### Derain
- Rain200L/Rain100L: [Download Link](https://www.icst.pku.edu.cn/struct/Projects/joint_rain_removal.html) - Click "The dataset" on the page to download

### Dehaze
- RESIDE: [Official Website](https://sites.google.com/view/reside-dehaze-datasets/)
  - SOTS-Outdoor: [Dropbox](https://bit.ly/2XZH498) or [Baidu Drive](https://pan.baidu.com/share/init?surl=SSVzR058DX5ar5WL5oBTLg) (password: s6tu)

### Denoise
- BSD400: [GitHub Download](https://github.com/smartboy110/denoising-datasets)
- BSD68: [GitHub Download](https://github.com/smartboy110/denoising-datasets) or [Berkeley Dataset](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/)
- Urban100: [Public Dataset](https://github.com/JingyiXu404/MCSCNet) in the test data section
- Kodak24: [GitHub Download](https://github.com/MohamedBakrAli/Kodak-Lossless-True-Color-Image-Suite)

### Deblur
- GoPro: [Official Website](https://seungjunnah.github.io/Datasets/gopro.html) - Contains 3,214 image pairs for deblurring training and testing

### Delol
- LOL (Low-Light): [Kaggle Download](https://www.kaggle.com/datasets/soumikrakshit/lol-dataset) - Contains 500 pairs of low-light/normal-light images

<div align="center">
    <img src="Table1.png" alt="Experimental Results Table" width="800"/>
    <p>Table 1: Performance comparison with existing methods on multiple datasets</p>
</div>

## Note
The remaining code is still being organized. Please stay tuned.
