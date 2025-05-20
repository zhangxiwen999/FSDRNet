# FSDRNet
FSDRNet: A Dynamic Recovery Network Based on Frequency-Spatial Collaborative Processing

<div align="center">
    <img src="Fig1.png" alt="FSDRNet模型架构图" width="800"/>
</div>

## 项目简介

FSDRNet (Frequency-Spatial Collaborative Dynamic Recovery Network) 是一种创新的图像恢复网络，通过多域协作特征增强和动态路由处理实现高效图像恢复。本项目将不同的图像退化类型视为多域信号表示问题，而非独立任务，建立了一个统一的图像恢复框架。

### 主要特点

- **多域协作处理**：融合空间域和频率域信息，充分利用两个域的互补优势
- **动态调节机制**：根据输入特性自动调整参数，有效处理单一、复合和未知退化类型
- **物理引导的滤波器**：基于物理先验设计专用滤波器，实现精确恢复
- **出色的跨任务性能**：在去噪、去模糊、去雾、去雨和低光增强多任务上表现优异

## 安装要求

```bash
# 环境要求
python >= 3.7
pytorch >= 1.7.0
numpy
einops==0.4.1
opencv_python==4.6.0.66
PyYAML==6.0
scikit_image==0.19.3
scikit_learn==1.0.2
scipy==1.7.3
tensorboardX==2.1
termcolor==1.1.0
timm==0.6.7
tqdm==4.64.0
matplotlib
torchvision
所有的代码还在进行整理，尽情期待
如需要数据集可参考
