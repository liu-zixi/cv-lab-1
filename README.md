# cv-lab-1

# 项目名称：从零开始构建三层神经网络分类器，实现图像分类

作者：刘子希 22307140051

## 训练方法：

使用封装好的train函数，参数如下。

```python
def train(epochs = 10, learning_rate = 0.001, l2_lambda = 0.001, c1 = 6, c2 = 16, k1 = 5, k2 = 5, save_model_name = 'manual_cnn_10_0.001_0.001_6_16_5_5.pth'):

'''
Input:

epochs: 训练周期数
learning_rate: 学习率
l2_lambda: 正则化强度
c1: 卷积层1的通道数
c2: 卷积层2的通道数
k1: 卷积层1的核大小
k2: 卷积层2的核大小
save_model_name: 该次训练期望生成的模型文件名 

Output:

1. 每5000个batch打印一次当前损失值和训练集上的准确率
2. 每10000个batch可视化一次通过卷积层1和2后的图像
3. 全部训练完成后打印损失曲线和准确率曲线

'''
```

输出示例：

```python
Epoch 9/10:  80%|███████▉  | 9999/12500 [17:12<04:00, 10.41it/s, loss=2.0480, acc=43.6%]
Epoch 9 Batch 10000: Loss=2.0480, Acc=43.62%
```

输出的卷积图像：

![image](https://github.com/user-attachments/assets/b5bccf9a-8219-487b-b0bf-667220ace262)

输出的loss和准确率曲线：

![image](https://github.com/user-attachments/assets/4ca0cbac-07ac-44c6-b961-a2d4a8291146)


## 测试方法：

已上传若干已训练好的模型，模型的命名按照如下规则，可使用封装好的test函数在测试集上测试：

```python

'''
模型命名规则
'manual_cnn_epochs_learningrate_l2lambda_c1_c2_k1_k2'

例:
manual_cnn_10_0.001_0.001_6_16_5_5 代表周期数10, 学习率0.001, 正则化强度0.001, 卷积层1通道数6, 卷积层2通道数16, 卷积层1核大小5*5, 卷积层2核大小5*5
的模型
'''

def test(model_name):

'''

Input: 模型名称   ### 可能需要在model_name前加上文件夹路径，我自己训练时是在同一个文件夹下了
Output: 将输出在测试集上的测试准确率

'''
```

输出示例：

```python
Correction: 4529
Accuracy of the network on the 10000 test images: 45.29 %
```
