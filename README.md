# fast-universal

本仓库是改进的通用对抗扰动生成算法的源代码

文献[1]中生成通用对抗扰动的算法没有考虑到向量的方向会对向量叠加结果的模的增长造成影响，比如当两个向量具有相同的方向时，它们的叠加结果有最大的模，而当它们具有相反的方向时，它们的叠加结果将会有最小的模。这种影响会降低所生成的通用对抗扰动的模的增长速度并使得生成速度变慢。将所叠加向量的方向作为优化目标之一来加速通用对抗扰动的生成，故有本算法。

代码测试所用的tensorflow版本：`tensorflow-gpu 1.1.0`

通过命令`python demo_DenseNet121.py`来展示通用对抗扰动的实际效果

遵循`demo_DenseNet121.py`的流程可以生成你自己的通用对抗扰动

[1] Moosavi-Dezfooli S M, Fawzi A, Fawzi O, et al. Universal adversarial perturbations[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2017: 1765-1773.
