# 提交说明
(1) 产生带白噪声的正弦波数据集（X，y）。
X有100个样本、1个特征, 取值[0,10],
y = np.sin(X) + 0.1 * np.random.randn(100,1)
(2) 先用多项式特征变换（degree=10)扩展特征、然后利用sklearn的Ridge类构造估计器，alpha=1。将上述两步构成管道，来拟合这个数据集。画出学习曲线。
(3) 从[0,10]等间距取1000数据点构成 Xnew，用上述模型预测其输出，画出拟合结果。

**多项式特征变换：** 通过将特征扩展到多项式形式，可以捕捉到数据中的非线性关系。这里选择 degree=10 是为了增加模型的复杂性，以便更好地拟合数据。
**Ridge回归：** 使用Ridge回归可以有效地处理多重共线性问题，并通过正则化来防止过拟合。设置 alpha=1 是为了控制正则化的强度。
