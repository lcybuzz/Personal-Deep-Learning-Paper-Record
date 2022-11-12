Quantization, integer inference, and other stuff related to mobile deployment

# Table of Contents
- [PTQ](#ptq)
- [QAT](#qat)
- [Inference](#inference)
- [Survey](#survey)
- [Resources](#resources)
- [Frameworks](#frameworks)

# PTQ
- **Data Free Quantization Through Weight Equalization and Bias Correction** <Br>
Markus Nagel, Mart van Baalen, Tijmen Blankevoort, Max Welling <Br>
[ICCV 2019] [[Project](https://cvlab.yonsei.ac.kr/projects/DAQ/)] [[Pytorch-Code](https://github.com/cvlab-yonsei/DAQ)] <Br>
[**CLE/BC**] [★★]
  

# QAT
- **Distance-aware Quantization** <Br>
Junghyup Lee, Dohyung Kim, [Bumsub Ham](https://cvlab.yonsei.ac.kr/) <Br>
[ICCV 2021] <Br>
[**DAQ**]

- **Fully Quantized Image Super-Resolution Networks** <Br>
[Hu Wang](https://huwang01.github.io/), Peng Chen, [Bohan Zhuang](https://bohanzhuang.github.io/), [Chunhua Shen](https://cshen.github.io/) <Br>
[MM 2021] [[Pytorch-Code](https://github.com/billhhh/FQSR)] <Br>
[**FQSR**] [★☆]
 
- **Gradient ℓ1 Regularization** <Br>
Milad Alizadeh, Arash Behboodi, Mart van Baalen, [Christos Louizos](https://christoslouizos.wordpress.com/), Tijmen Blankevoort, [Max Welling](https://staff.fnwi.uva.nl/m.welling/) <Br>
[ICLR 2020] <Br>
[★☆] 高通出品. 提出加入梯度的L1正则, 减小量化误差.

- **PAMS: Quantized Super-Resolution via Parameterized Max Scale** <Br>
Huixia Li, Chenqian Yan, [Shaohui Lin](https://sites.google.com/site/shaohuilin007/home), [Xiawu Zheng](https://sites.google.com/view/zhengxiawu), Yuchao Li, [Baochang Zhang](http://shi.buaa.edu.cn/mpl/en/index.htm), Fan Yang, [Rongrong Ji](https://mac.xmu.edu.cn/rrji_en/) <Br>
[arXiv 1902] <Br>
[★]

- **LSQ+: Improving low-bit quantization through learnable offsets and better initialization** <Br>
[Yash Bhalgat](https://yashbhalgat.github.io/), Jinwon Lee, Markus Nagel, Tijmen Blankevoort, [Nojun Kwak](http://mipal.snu.ac.kr/index.php/Main_Page) <Br>
[CVPR 2020] [[Unofficial-Pytorch-Code](https://github.com/DeadAt0m/LSQFakeQuantize-PyTorch)] <Br>
[**LSQ+**] [★★] 将LSQ推广至非对称量化, scale和offset均可学习

- **Learned Step Size Quantization** <Br>
Steven K. Esser, Jeffrey L. McKinstry, Deepika Bablani, Rathinakumar Appuswamy, Dharmendra S. Modha <Br>
[arXiv 1902] [[Unofficial-Pytorch-Code](https://github.com/DeadAt0m/LSQFakeQuantize-PyTorch)] <Br>
[**LSQ**] [★★] 学习scale

- **ProxQuant: Quantized Neural Networks via Proximal Operators** <Br>
[Yu Bai](https://yubai.org/), [Yu-Xiang Wang](https://sites.cs.ucsb.edu/~yuxiangw/), [Edo Liberty](https://edoliberty.github.io//)  <Br>
[ICLR 2019] [[Pytorch-Code](https://github.com/allenbai01/ProxQuant)] <Br>

- **PACT: Parameterized Clipping Activation for Quantized Neural Networks** <Br>
Jungwook Choi, Zhuo Wang, [Swagath Venkataramani](https://engineering.purdue.edu/people/swagath.venkataramani.1/index_html), Pierce I-Jen Chuang, Vijayalakshmi Srinivasan, Kailash Gopalakrishnan <Br>
[ICLR 2018] [[Pytorch-Code](https://github.com/IntelLabs/distiller/blob/master/distiller/quantization/clipped_linear.py)] <Br>
[★☆] Intel出品. 提出对ReLU的上限加一个可学习的截断, 使qat时网络能自动找到更好的clip range.

- **On periodic functions as regularizers for quantization of neural networks** <Br>
[Maxim Naumov](https://research.facebook.com/people/naumov-maxim/), Utku Diril, [Jongsoo Park](https://sites.google.com/site/jongsoopark/), Benjamin Ray, Jedrzej Jablonski, [Andrew Tulloch](https://tullo.ch/) <Br>
[arXiv 1811] <Br>
[★☆] Facebook出品

- **Learning Sparse Low-Precision Neural Networks With Learnable Regularization** <Br>
Yoojin Choi, Mostafa El-Khamy, [Jungwon Lee](https://sites.google.com/site/jungwonlee) <Br>
[arXiv 1809] <Br>
三星出品

- **LQ-Nets: Learned Quantization for Highly Accurate and Compact Deep Neural Networks** <Br>
[Dongqing Zhang](https://github.com/zdqzeros), [Jiaolong Yang](http://jlyang.org/), [Dongqiangzi Ye](https://github.com/EowinYe), [Gang Hua](https://www.microsoft.com/en-us/research/people/ganghua/)  <Br>
[ECCV 2018] [[TF-Code](https://github.com/microsoft/LQ-Nets)] <Br>
MSRA出品

- **Towards Effective Low-bitwidth Convolutional Neural Networks** <Br>
Bohan Zhuang, Chunhua Shen, Mingkui Tan, Lingqiao Liu, Ian Reid  <Br>
[CVPR 2018] [[Pytorch-Code](https://github.com/nowgood/QuantizeCNNModel)] <Br>
[★] 提出3个trick: 1) 分两阶段, 先量化weight, 再量化act; 2) 逐渐降低比特数, 对2bit量化等情况可能有效; 3) 用float模型对quant模型做feature的蒸馏


  



# Inference
- **Towards Fully 8-bit Integer Inference for the Transformer Model** <Br>
Ye Lin, Yanyang Li, Tengbo Liu, Tong Xiao, Tongran Liu, [Jingbo Zhu](https://www.nlplab.com/members/zhujingbo.html) <Br>
[IJCAI 2020] <Br>



# Survey
- **A White Paper on Neural Network Quantization** <Br>
Markus Nagel, Marios Fournarakis, Rana Ali Amjad, Yelysei Bondarenko, Mart van Baalen, Tijmen Blankevoort <Br>
[arXiv 2106] <Br>
[★★☆] 高通量化白皮书, 提供了PTQ和QAT的一些实用建议

- **A Survey of Quantization Methods for Efficient Neural Network Inference** <Br>
[Amir Gholami](http://amirgholami.org/), Sehoon Kim, [Zhen Dong](https://dong-zhen.com/), [Zhewei Yao](https://yaozhewei.github.io/), [Michael W. Mahoney](https://www.stat.berkeley.edu/~mmahoney/), [Kurt Keutzer](https://people.eecs.berkeley.edu/~keutzer/) <Br>
[arXiv 2103] <Br>

- **Integer Quantization for Deep Learning Inference: Principles and Empirical Evaluation** <Br>
Hao Wu, Patrick Judd, Xiaojie Zhang, [Mikhail Isaev](https://research.monash.edu/en/persons/mikhail-isaev), Paulius Micikevicius <Br>
[arXiv 2004] <Br>

- **Quantizing deep convolutional networks for efficient inference: A whitepaper** <Br>
Raghuraman Krishnamoorthi <Br>
[arXiv 1806] <Br>
谷歌量化白皮书

- **Quantization and Training of Neural Networks for Efficient Integer-Arithmetic-Only Inference** <Br>
Benoit Jacob, Skirmantas Kligys, [Bo Chen](http://www.vision.caltech.edu/bchen3/_site2/index.html), [Menglong Zhu](http://dreamdragon.github.io/), Matthew Tang, Andrew Howard, [Hartwig Adam](https://research.google/people/author37870/), Dmitry Kalenichenko <Br>
[CVPR 2018] <Br>
比较详细地介绍了qat和int8推理

  
  
  
# Resources
[基于pytorch的QAT, PTQ, 剪枝等算法实现](https://github.com/666DZY666/micronet)
  
[Awesome Model Quantization](https://github.com/htqin/awesome-model-quantization#Survey_of_Quantization)

  
  
# Frameworks
高通量化框架AIMET(TF1, Pytorch) [[AIMET](https://github.com/quic/aimet)]

[[Intel Distiller](https://github.com/IntelLabs/distiller)]
  
Facebook端侧推理框架 [[QNNPACK](https://github.com/pytorch/QNNPACK)]  [[FBGEMM](https://github.com/pytorch/FBGEMM)] [[Blog](https://engineering.fb.com/2018/11/07/ml-applications/fbgemm/)]

[[NCNN](https://github.com/Tencent/ncnn)]
  
[[MNN](https://github.com/alibaba/MNN)]
  
[[OpenVINO](https://github.com/openvinotoolkit/openvino)]
