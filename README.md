# Personal-Deep-Learning-Paper-Record
# Under Construction

# Model
### **Deformable-ConvNets ★★**
**[Paper]** Deformable Convolutional Networks <Br>
**[Year]** ICCV 2017 Oral<Br>
**[Authors]**	[Jifeng Dai](http://www.jifengdai.org/), [Haozhi Qi](http://haozhi.io/), [Yuwen Xiong](http://www.cs.toronto.edu/~yuwen/), [Yi Li](https://liyi14.github.io/), [Guodong Zhang](http://www.cs.toronto.edu/~gdzhang/), [Han Hu](https://sites.google.com/site/hanhushomepage/), [Yichen Wei](https://www.microsoft.com/en-us/research/people/yichenw/) <Br>
 **[Pages]** https://github.com/msracver/Deformable-ConvNets <Br>
 **[Description]**<Br>
1) 传统CNN对几何形变的适应力差, 这是标准卷积中的规则格点采样造成的. 为此论文提出了deformable convolution和deformable ROI pooling
2) 具体做法很简洁, 即用卷积层从前一层的feature map中学习到每个位置的offsets, 整个过程是完全可微的.
3) 实验效果很好. 论文可以之后精读
