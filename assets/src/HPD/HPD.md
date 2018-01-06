### Deeplearning Algorithms tutorial
谷歌的人工智能位于全球前列，在图像识别、语音识别、无人驾驶等技术上都已经落地。而百度实质意义上扛起了国内的人工智能的大旗，覆盖无人驾驶、智能助手、图像识别等许多层面。苹果业已开始全面拥抱机器学习，新产品进军家庭智能音箱并打造工作站级别Mac。另外，腾讯的深度学习平台Mariana已支持了微信语音识别的语音输入法、语音开放平台、长按语音消息转文本等产品，在微信图像识别中开始应用。全球前十大科技公司全部发力人工智能理论研究和应用的实现，虽然入门艰难，但是一旦入门，高手也就在你的不远处！
AI的开发离不开算法那我们就接下来开始学习算法吧！

#### Hopfield神经网络

人工神经网络 （Artificial Neural Network，ANN）简称神经网络(NN)，是基于生物学中神经网络的基本原理，在理解和抽象了人脑结构和外界刺激响应机制后，以网络拓扑知识为理论基础，模拟人脑的神经系统对复杂信息的处理机制的一种数学模型，根植于神经科学、数学、思维科学、人工智能、统计学、物理学、计算机科学以及工程科学的一门技术，通常用于解决分类和回归问题。具有并行分布的处理能力、高容错性、智能化和自学习等能力的特征，本质上是一个有大量简单元件相互连接而成的复杂网络，具有高度的非线性，能够进行复杂的逻辑操作和非线性关系实现的系统。

神经网络由大量的节点（或称神经元）之间相互联接构成，每个节点代表一种特定的输出函数，称为激活函数（activation function）；每两个节点间的连接都代表一个对于通过该连接信号的加权值，称之为权重（weight），神经网络就是通过这种方式来模拟人类的记忆。网络的输出则取决于网络的结构、网络的连接方式、权重和激活函数。而网络自身通常都是对自然界某种算法或者函数的逼近，也可能是对一种逻辑策略的表达，是对传统逻辑学演算的进一步延伸。

<p align="center">
<img width="300" align="center" src="../../images/91.jpg" />
</p>
人工神经网络中，神经元处理单元可表示不同的对象，例如特征、字母、概念，或者一些有意义的抽象模式。网络中处理单元的类型分为三类：输入单元、输出单元和隐单元。输入单元接受外部世界的信号与数据；输出单元实现系统处理结果的输出；隐单元是处在输入和输出单元之间，不能由系统外部观察的单元。神经元间的连接权值反映了单元间的连接强度，信息的表示和处理体现在网络处理单元的连接关系中。

算法背景和发展

20世纪40年代，人们开始对神经网络研究。

1943 年，美国心理学家麦克洛奇（Mcculloch）和数学家皮兹（Pitts）提出了M-P模型，此模型比较简单，但是意义重大。在模型中，通过把神经元看作功能逻辑器件来实现算法，从此开创了神经网络模型的理论研究。

1949心理学家赫布（Hebb）提出Hebb法则，为构造有学习功能的神经网络模型奠定了基础。

1957 年，罗森勃拉特（Rosenblatt）以M-P 模型为基础，提出了感知器（Perceptron）模型；

1959年，美国著名工程师威德罗（B.Widrow）和霍夫（M.Hoff）等人提出ADALINE网络模型，ADALINE网络模型是一种连续取值的自适应线性神经元网络模型，可以用于自适应系统。

1972年，芬兰的KohonenT.教授，提出了自组织神经网络SOM(Self-Organizing feature map)。

1976年，美国Grossberg教授提出了著名的自适应共振理论ART(Adaptive Resonance Theory)，其学习过程具有自组织和自稳定的特征。

1982年，美国物理学家霍普菲尔德（Hopfield）提出了一种离散神经网络，即离散Hopfield网络，从而有力地推动了神经网络的研究；

1984年，Hinton与年轻学者Sejnowski等合作提出了Boltzmann机模型；

1986年，儒默哈特（D.E.Ru melhart）等人在多层神经网络模型的基础上，提出了多层神经网络权值修正的反向传播学习算法----BP算法（Error Back-Propagation）；

1988年，Chua和Yang提出了细胞神经网络（CNN）模型；

1994年，廖晓昕关于细胞神经网络的数学理论与基础的提出，带来了这个领域新的进展。通过拓广神经网络的激活函数类，给出了更一般的时滞细胞神经网络(DCNN)、Hopfield神经网络（HNN）、双向联想记忆网络（BAM）模型；