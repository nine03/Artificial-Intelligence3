# 循环神经网络(Recurrent Neural Network, RNN 순환 신경망)

### 开发环境(development environment 개발환경)
- PyCharm 
- Python 3.6
- Numpy 

### 主要原理(주요원리)
循环神经网络(Recurrent Neural Network, RNN)是一类以序列(sequence)数据为输入, 在序列的演进方向进行递归(recursion)且所有节点(循环单元)按链式连接的递归神经网络(recursive neural network)。   
对循环神经网络的研究始于二十世纪80-90年代, 并在二十一世纪初发展为深度学习（deep learning）算法之一, 其中双向循环神经网络(Bidirectional RNN, Bi-RNN)和长短期记忆网络(Long Short-Term Memory networks，LSTM)是常见的循环神经网络。   
循环神经网络具有记忆性,参数共享并且图灵完备(Turing completeness), 因此在对序列的非线性特征进行学习时具有一定优势。循环神经网络在自然语言处理(Natural Language Processing, NLP), 例如语音识别, 语言建模, 机器翻译等领域有应用, 也被用于各类时间序列预报。引入了卷积神经网络(Convoutional Neural Network, CNN)构筑的循环神经网络可以处理包含序列输入的计算机视觉问题。   
![d6ca7bcb0a46f21f429a50e4fb246b600d33aedf](https://user-images.githubusercontent.com/60682087/114156523-a4279d80-995d-11eb-873a-2e98fc7c8126.jpg)   

### RNN网路结构

![20170712163308512](https://user-images.githubusercontent.com/60682087/114157565-b7873880-995e-11eb-867e-4a386474daec.jpg)   
从上图我们可以看出, RNN隐藏层神经元的连接方式和普通神经网路的连接方式有一个非常明显的区别, 就是同一层的神经元的输出也成为了这一层神经元的输入。当然同一时刻的输出是不可能作为这个时刻的输入的。所以是前一个时刻（t-1）的输出作为这个时刻（t）的输入。   
![20170712163331539](https://user-images.githubusercontent.com/60682087/114157275-70994300-995e-11eb-97d5-eb858095de6d.jpg)   
上图就是一个序列的结构展开示意图。   
### 公式推导

设输入层到隐层的权重矩阵为V, 隐层自循环的权重矩阵为U, 隐层到输出层的权重矩阵为W, 对应的偏置为bh,by, 隐层的输出为h, z表示激活前对应的加权和。假设为三层网络。

1. 隐层输入变为：

![201707121633315391](https://user-images.githubusercontent.com/60682087/114161158-b952fb00-9962-11eb-910c-776e21c27e62.jpg)

2. 隐层最终输出变为：

![2017071216333153912](https://user-images.githubusercontent.com/60682087/114161376-f15a3e00-9962-11eb-918b-591d80478342.JPG)

说明：这个序列的最终的输出概率基于之前所有的输出。距离当前时间越长, 越早输入的序列, 在更新后的状态中所占权重越小, 从而表现出时间相关性。

- 这个项目是我为了重新学习人工智能而做的项目。（이 프로젝트는 내가 인공지능을 다시 공부하기위해서 만든 프로젝트입니다.）
