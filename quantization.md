# Quantization
模型量化论文, 主要关注与实际硬件部署相关的内容
# Table of Contents
- [PTQ](#ptq)
- [QAT](#qat)
- [Survey](#survey)
- [Resources](#resources)


## PTQ
### CLE/BC ★★
**[Paper]**  (ICCV 2019) Data Free Quantization Through Weight Equalization and Bias Correction <Br>
**[Author]** Markus Nagel, Mart van Baalen, Tijmen Blankevoort, Max Welling <Br>
**[[Project](https://cvlab.yonsei.ac.kr/projects/DAQ/)]** <Br> **[[Pytorch-Code](https://github.com/cvlab-yonsei/DAQ)]** <Br>

  
## QAT
### DAQ
**[Paper]**  (ICCV 2021) Distance-aware Quantization <Br>
**[Author]** Junghyup Lee, Dohyung Kim, [Bumsub Ham](https://cvlab.yonsei.ac.kr/) <Br>
  
### LSQ+ ★★
**[Paper]**  (CVPR 2020) LSQ+: Improving low-bit quantization through learnable offsets and better initialization <Br>
**[Author]** [Yash Bhalgat](https://yashbhalgat.github.io/), Jinwon Lee, Markus Nagel, Tijmen Blankevoort, [Nojun Kwak](http://mipal.snu.ac.kr/index.php/Main_Page) <Br>
**[[Unofficial-Pytorch-Code](https://github.com/DeadAt0m/LSQFakeQuantize-PyTorch)]** <Br>
将LSQ推广至非对称量化, scale和offset均可学习

### LSQ ★★
**[Paper]**  (arXiv 1902) Learned Step Size Quantization <Br>
**[Author]** Steven K. Esser, Jeffrey L. McKinstry, Deepika Bablani, Rathinakumar Appuswamy, Dharmendra S. Modha <Br>
**[[Unofficial-Pytorch-Code](https://github.com/DeadAt0m/LSQFakeQuantize-PyTorch)]** <Br>
学习scale

### PACT
**[Paper]**  (ICLR 2018) PACT: Parameterized Clipping Activation for Quantized Neural Networks <Br>
**[Author]** Jungwook Choi, Zhuo Wang, [Swagath Venkataramani](https://engineering.purdue.edu/people/swagath.venkataramani.1/index_html), Pierce I-Jen Chuang, Vijayalakshmi Srinivasan, Kailash Gopalakrishnan <Br>
**[[Unofficial-Pytorch-Code](https://github.com/KwangHoonAn/PACT)]**  **[[Unofficial-Pytorch-Code](https://github.com/cornell-zhang/dnn-gating)]** <Br>

### *Towards Effective Low-bitwidth Convolutional Neural Networks* ★
**[Paper]**  (CVPR 2018) Towards Effective Low-bitwidth Convolutional Neural Networks <Br>
**[Author]** Bohan Zhuang, Chunhua Shen, Mingkui Tan, Lingqiao Liu, Ian Reid <Br>
**[[Pytorch-Code](https://github.com/nowgood/QuantizeCNNModel)]** <Br>
提出3个trick: 1) 分两阶段, 先量化weight, 再量化act; 2) 逐渐降低比特数, 对2bit量化等情况可能有效; 3) 用float模型对quant模型做feature的蒸馏


### *Quantization and Training of Neural Networks for Efficient Integer-Arithmetic-Only Inference* ★★★
**[Paper]**  (CVPR 2018) Quantization and Training of Neural Networks for Efficient Integer-Arithmetic-Only Inference<Br>
**[Author]** Benoit Jacob, Skirmantas Kligys, [Bo Chen](http://www.vision.caltech.edu/bchen3/_site2/index.html), [Menglong Zhu](http://dreamdragon.github.io/), Matthew Tang, Andrew Howard, [Hartwig Adam](https://research.google/people/author37870/), Dmitry Kalenichenko <Br>
比较详细地介绍了qat和int8推理




## Survey
### *A White Paper on Neural Network Quantization* ★★☆
**[Paper]**  (arXiv 2106) A White Paper on Neural Network Quantization <Br>
**[Author]** Markus Nagel, Marios Fournarakis, Rana Ali Amjad, Yelysei Bondarenko, Mart van Baalen, Tijmen Blankevoort <Br>
高通量化白皮书, 提供了PTQ和QAT的一些实用建议

### *A Survey of Quantization Methods for Efficient Neural Network Inference* ★★
**[Paper]**  (arXiv 2103) A Survey of Quantization Methods for Efficient Neural Network Inference <Br>
**[Author]** [Amir Gholami](http://amirgholami.org/), Sehoon Kim, [Zhen Dong](https://dong-zhen.com/), [Zhewei Yao](https://yaozhewei.github.io/), [Michael W. Mahoney](https://www.stat.berkeley.edu/~mmahoney/), [Kurt Keutzer](https://people.eecs.berkeley.edu/~keutzer/) <Br>

### Integer Quantization for Deep Learning Inference
**[Paper]**  (arXiv 2004) Integer Quantization for Deep Learning Inference: Principles and Empirical Evaluation <Br>
**[Author]** Hao Wu, Patrick Judd, Xiaojie Zhang, [Mikhail Isaev](https://research.monash.edu/en/persons/mikhail-isaev), Paulius Micikevicius <Br>

### *Quantizing deep convolutional networks for efficient inference: A whitepaper* ★★
**[Paper]**  (arXiv 1806) Quantizing deep convolutional networks for efficient inference: A whitepaper <Br>
**[Author]** Raghuraman Krishnamoorthi <Br>
谷歌量化白皮书

  
  
  
## Resources
[高通量化框架AIMET(TF1, Pytorch)](https://github.com/quic/aimet)

[Intel Distiller](https://github.com/IntelLabs/distiller)
  
[基于pytorch的QAT, PTQ, 剪枝等算法实现](https://github.com/666DZY666/micronet)
  
[Awesome Model Quantization](https://github.com/htqin/awesome-model-quantization#Survey_of_Quantization)

