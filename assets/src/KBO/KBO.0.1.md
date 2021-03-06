### Deeplearning Algorithms tutorial
谷歌的人工智能位于全球前列，在图像识别、语音识别、无人驾驶等技术上都已经落地。而百度实质意义上扛起了国内的人工智能的大旗，覆盖无人驾驶、智能助手、图像识别等许多层面。苹果业已开始全面拥抱机器学习，新产品进军家庭智能音箱并打造工作站级别Mac。另外，腾讯的深度学习平台Mariana已支持了微信语音识别的语音输入法、语音开放平台、长按语音消息转文本等产品，在微信图像识别中开始应用。全球前十大科技公司全部发力人工智能理论研究和应用的实现，虽然入门艰难，但是一旦入门，高手也就在你的不远处！
AI的开发离不开算法那我们就接下来开始学习算法吧！

#### 基于核的算法

支持向量机通过某非线性变换 φ( x) ，将输入空间映射到高维特征空间。特征空间的维数可能非常高。如果支持向量机的求解只用到内积运算，而在低维输入空间又存在某个函数 K(x, x′) ，它恰好等于在高维空间中这个内积，即K( x, x′) =<φ( x) ⋅φ( x′) > 。那么支持向量机就不用计算复杂的非线性变换，而由这个函数 K(x, x′) 直接得到非线性变换的内积，使大大简化了计算。这样的函数 K(x, x′) 称为核函数。

早在1964年Aizermann等在势函数方法的研究中就将该技术引入到机器学习领域，但是直到1992年Vapnik等利用该技术成功地将线性SVMs推广到非线性SVMs时其潜力才得以充分挖掘。而核函数的理论则更为古老，Mercer定理可以追溯到1909年，再生核希尔伯特空间(ReproducingKernel Hilbert Space, RKHS)研究是在20世纪40年代开始的。

核函数包括线性核函数、多项式核函数、高斯核函数等，其中高斯核函数最常用，可以将数据映射到无穷维，也叫做径向基函数（Radial Basis Function 简称 RBF），是某种沿径向对称的标量函数。通常定义为空间中任一点x到某一中心xc之间欧氏距离的单调函数 ，可记作 k（||x-xc||）， 其作用往往是局部的，即当x远离xc时函数取值很小。

 根据模式识别理论，低维空间线性不可分的模式通过非线性映射到高维特征空间则可能实现线性可分，但是如果直接采用这种技术在高维空间进行分类或回归，则存在确定非线性映射函数的形式和参数、特征空间维数等问题，而最大的障碍则是在高维特征空间运算时存在的“维数灾难”。采用核函数技术可以有效地解决这样问题。
 
 
基于核里的应用算法有：
* 支持向量机（SVM）
* 径向基函数（Radial Basis Function ，RBF)
* 线性判别分析（Linear Discriminate Analysis ，LDA)

核函数方法的特点:
* 核函数的引入避免了“维数灾难”,大大减小了计算量。而输入空间的维数n对核函数矩阵无影响，因此，核函数方法可以有效处理高维输入。
* 无需知道非线性变换函数的形式和参数。
* 核函数的形式和参数的变化会隐式地改变从输入空间到特征空间的映射，进而对特征空间的性质产生影响，最终改变各种核函数方法的性能。
* 核函数方法可以和不同的算法相结合，形成多种不同的基于核函数技术的方法，且这两部分的设计可以单独进行，并可以为不同的应用选择不同的核函数和算法。
