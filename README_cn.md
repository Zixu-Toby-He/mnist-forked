以下是提供的中文翻译：

---

MNIST 手写数字数据库是最流行的图像识别数据集之一，该数据库包含 6 万个训练样本和 1 万个测试样本。本页面旨在为 MNIST 数据库提供一个镜像下载站点，原始网站位于 http://yann.lecun.com/exdb/mnist/ 。有关数据集的更多详细信息，请访问原始网站。

# 下载
[训练用图像](https://storage.googleapis.com/cvdf-datasets/mnist/train-images-idx3-ubyte.gz)  
[训练用标签](https://storage.googleapis.com/cvdf-datasets/mnist/train-labels-idx1-ubyte.gz)

[测试用图像](https://storage.googleapis.com/cvdf-datasets/mnist/t10k-images-idx3-ubyte.gz)  
[测试用标签](https://storage.googleapis.com/cvdf-datasets/mnist/t10k-labels-idx1-ubyte.gz)

# 文件格式
以下文件格式说明来自 http://yann.lecun.com/exdb/mnist/ 。

IDX 文件格式是一种用于存储各种数值类型的向量和多维矩阵的简单格式。  
基本格式如下：

```
元数据
第 0 维的大小
第 1 维的大小
第 2 维的大小
.....
第 N 维的大小
数据
```

元数据包含4字节，前 2 个字节始终为 0，第 3 个字节表示数据的类型：
```
0x08：无符号字节
0x09：有符号字节
0x0B：短整型（2 字节）
0x0C：整型（4 字节）
0x0D：浮点型（4 字节）
0x0E：双精度浮点型（8 字节）
```

第 4 个字节表示向量/矩阵的维度数：1 表示向量，2 表示矩阵...  
每个维度的大小以 4 字节整数存储（高位字节优先，大端字节序，如同大多数非 Intel 处理器）。  
数据的存储方式类似于 C 语言中的数组，即最后一维的索引变化最快。

# 致谢
感谢 Yann LeCun 教授慷慨允许 CVDF 托管 MNIST 数据库中的图像和标注副本，并感谢 Google Cloud Platform 提供存储空间。