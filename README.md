# 循环神经网络(Recurrent Neural Network, RNN 순환 신경망)

### 开发环境(development environment 개발환경)
- PyCharm 
- Python 3.6
- Numpy 

### 主要原理(주요원리)
循环神经网络(Recurrent Neural Network, RNN)是一类以序列(sequence)数据为输入, 在序列的演进方向进行递归(recursion)且所有节点(循环单元)按链式连接的递归神经网络(recursive neural network)。   
对循环神经网络的研究始于二十世纪80-90年代, 并在二十一世纪初发展为深度学习（deep learning）算法之一, 其中双向循环神经网络(Bidirectional RNN, Bi-RNN)和长短期记忆网络(Long Short-Term Memory networks，LSTM)是常见的循环神经网络。   
循环神经网络具有记忆性,参数共享并且图灵完备(Turing completeness), 因此在对序列的非线性特征进行学习时具有一定优势。循环神经网络在自然语言处理(Natural Language Processing, NLP), 例如语音识别, 语言建模, 机器翻译等领域有应用, 也被用于各类时间序列预报。引入了卷积神经网络(Convoutional Neural Network, CNN)构筑的循环神经网络可以处理包含序列输入的计算机视觉问题。
