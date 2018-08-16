# Personal-Deep-Learning-Paper-Record
# Under Construction
# Table of Contents
- [Network](#network)
- [Classification](#classification)
# Rank
- Human Segmentation <Br>
  - ★★★ <Br>
  - ★★ <Br>
  **[ResNeXt]**, **[Deformable-ConvNets]**,**[DenseNet]** <Br>
  - ★ <Br>
  
# Network
### **RAM**
**[Paper]** Recurrent models of visual attention <Br>
**[Year]** NIPS 2014 <Br>
**[Authors]** [Volodymyr Mnih](https://www.cs.toronto.edu/~vmnih/), [Nicolas Heess](http://homepages.inf.ed.ac.uk/s0677090/), [Alex Graves](https://www.cs.toronto.edu/~graves/), [Koray Kavukcuoglu](http://koray.kavukcuoglu.org/)<Br>
 **[Pages]** <Br>
  https://github.com/kevinzakka/recurrent-visual-attention (Unofficial) <Br>
  https://github.com/jlindsey15/RAM (Unofficial) <Br>
  https://github.com/zhongwen/RAM  (Unofficial) <Br>
 **[Description]**<Br>

### **ResNeXt ★★**
**[Paper]** Aggregated Residual Transformations for Deep Neural Networks <Br>
**[Year]** arXiv 1611 <Br>
**[Authors]** [Saining Xie](http://vcl.ucsd.edu/~sxie/), [Ross Girshick](http://www.rossgirshick.info/), [Piotr Dollár](https://pdollar.github.io/), [Zhuowen Tu](http://pages.ucsd.edu/~ztu/), [Kaiming He](http://kaiminghe.com/) <Br>
 **[Pages]** https://github.com/facebookresearch/ResNeXt <Br>
 **[Description]**<Br>
1) ResNet的改进版, 复杂度不变的情况下提升了精度. 只看了其它blog的解析, 自己没读 
  
### **Deformable-ConvNets ★★**
**[Paper]** Deformable Convolutional Networks <Br>
**[Year]** ICCV 2017 Oral<Br>
**[Authors]**	[Jifeng Dai](http://www.jifengdai.org/), [Haozhi Qi](http://haozhi.io/), [Yuwen Xiong](http://www.cs.toronto.edu/~yuwen/), [Yi Li](https://liyi14.github.io/), [Guodong Zhang](http://www.cs.toronto.edu/~gdzhang/), [Han Hu](https://sites.google.com/site/hanhushomepage/), [Yichen Wei](https://www.microsoft.com/en-us/research/people/yichenw/) <Br>
 **[Pages]** https://github.com/msracver/Deformable-ConvNets <Br>
 **[Description]**<Br>
1) 传统CNN对几何形变的适应力差, 这是标准卷积中的规则格点采样造成的. 为此论文提出了deformable convolution和deformable ROI pooling
2) 具体做法很简洁, 即用卷积层从前一层的feature map中学习到每个位置的offsets, 整个过程是完全可微的.
3) 实验效果很好. 论文可以之后精读

### **DenseNet ★★**
**[Paper]** Densely Connected Convolutional Networkss <Br>
**[Year]** CVPR 2017 Best Paper<Br>
**[Authors]** [Gao Huang](http://www.cs.cornell.edu/~gaohuang/), [Zhuang Liu](https://liuzhuang13.github.io/), [Laurens van der Maaten](https://lvdmaaten.github.io/), [Kilian Q. Weinberger](http://www.cs.cornell.edu/~kilian/)	<Br>
**[Pages]** https://github.com/liuzhuang13/DenseNet <Br>
**[Description]**<Br>
1) 核心思路是每一层都与之前的层直接相连, 实现特征的重复利用, 并使得每层的feature map数可以设置的很小. <Br>
2) 实际设计中, 采用dense block + transition layer的结构. 每个dense block中进行feature的密集连接(将前面得到feature直接concat到后面的feature map上), 并用1*1的conv降维, transition layer的作用也是降低前一block的输出维度. <Br>
3) 优点: 性能好, 相对而言参数较少. 缺点: 很耗内存. 以caffe为例, concat层会为需要concat的feature另外分配一份新的内存空间, 这样第L层的feature实际需要L(L+1)/2个feature的空间. 作者团队给出了优化策略, 还没看. <Br>
  
### ***Residual Attention Network***
**[Paper]** Residual Attention Network <Br>
**[Year]** CVPR 2017 Spotlight <Br>
**[Authors]** Fei Wang, [Mengqing Jiang](https://github.com/Jmq14), Chen Qian, [Shuo Yang](http://shuoyang1213.me/), Chen Li, Honggang Zhang, [Xiaogang Wang](http://www.ee.cuhk.edu.hk/~xgwang/), [Xiaoou Tang](https://www.ie.cuhk.edu.hk/people/xotang.shtml) <Br>
 **[Pages]** https://github.com/fwang91/residual-attention-network <Br>
 **[Description]**<Br>
1) 提出了一个形式上与resnet很相似的结构: resudual attention net, 将attention机制结合进前馈深度神经网络中. <Br>
2) 所谓residual attention network, 即采用类似residual block的(1+M(x))*F(x)的形式, 而不是直接将attention map M(x)直接与feature map相乘, 避免了使feature数值越来越小的问题. Attention mask branch采用了encoder-decoder的结构. <Br>
3) 虽然本文看上去就是将resnet中的high way一支改成encoder-decoder结构的mask branch, 但其思路和论述的角度比较独特, 值得学习. 从结果上看attention mask branch的确能起到抑制背景, 增强前景feature的效果, 感觉挺神奇. 不过, 这一机制能否用到如语义分割等其他任务上存疑.<Br>
  
### **SENet**
**[Paper]** Squeeze-and-Excitation Networks <Br>
**[Year]** CVPR 2018 <Br>
**[Authors]**  Jie Hu, Li Shen, Gang Sun<Br>
**[Pages]** https://github.com/hujie-frank/SENet <Br>
**[Description]** <Br>
