## MSSAM:  Multi-Scale Spatial-Aware Mamba for Multimodal Remote Sensing Image Classification

## Abstract

Applying deep learning techniques to classify multimodal remote sensing imagery plays a vital role in Earth observation. Current methods primarily face three challenges: (1) interference from complex backgrounds, the presence of strongly directional structures such as roads and building clusters, and significant variations in the scale of ground objects. (2) Conversely, traditional Transformers are capable of modeling global dependencies, but the quadratic complexity of self-attention limits their applicability to high-resolution remote sensing data. (3) Emerging state space models, such as Mamba, offer the advantage of linear computational complexity. However, their unidirectional scanning mechanism creates a structural contradiction with 2D spatial understanding, leading to directional bias and contextual fragmentation. To overcome these limitations, we propose MSSAM, a groundbreaking hybrid encoder-decoder architecture that integrates: (1) the Multi-Scale Spatial-Aware Block (MSSAB), which employs a bidirectional context pre-fusion mechanism enabling a single Mamba module to capture bidirectional dependencies, and introduces dual-view Transformers to explicitly model spatial dependencies along horizontal and vertical dimensions respectively, achieving comprehensive 2D context awareness; and (2) the Multi-Branch Attention Spectral Rearrange Block (MBASR), which introduces a novel spectral rearrange mechanism that systematically promotes cross-branch feature interaction by reorganizing spectral features across channel groups. This enables the decoder to more effectively exploit local details and multi-scale semantic information through cascaded channel and spatial attention-guided multi-scale depthwise convolutions. On the Muufl, Houston, and Augsburg datasets, MSSAM achieves classification accuracies of 96.57%, 99.79%, and 97.89%, respectively, substantially outperforming existing state-of-the-art methods in comprehensive evaluations. Furthermore, MSSAM exhibits superior generalization performance when tested on two single-modality datasets: Pavia University (hyperspectral) and Flevoland (PolSAR). This research introduces a novel framework for intelligent interpretation of multimodal remote sensing imagery. 

## Requirements:

- Python 3.11
- PyTorch >= 2.10.0
- mamba-ssm >= 2.3.0

## Usage:

python main.py

