# Personal-Deep-Learning-Paper-Record
# Under Construction

# Network
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
