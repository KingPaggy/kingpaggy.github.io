# 循环数据的均值(Circular mean/ 角度均值)

[Wikipedia](https://en.wikipedia.org/wiki/Circular_mean)

## 简介

循环数据的均值是指对于一组角度数据，求出其均值。这个均值是一个角度，表示这组角度数据的平均方向。

举例：
- 0° 和 360° 的算术均值是 180°，这是有误导性的，因为 360° 等于 0° 。
- 晚上 11 点到凌晨 1 点之间的“平均时间”是午夜还是中午。这具体取决于这两个时间是单个夜晚的一部分还是单个日历日的一部分。

## circular mean

循环均值(circular mean)是方向统计(directional statistics)中最简单的示例之一。

循环均值的计算(角度值 $\alpha_1,\alpha_2,...,\alpha_n$ )
- 将所有角度转换为单位向量。比如，角度为 $\theta$ 的单位向量是 $(\cos(\theta), \sin(\theta))$。
- 将所有单位向量相加，得到一个总向量。
- 再计算总向量的角度，即为循环均值。

$$
\bar{\alpha}=\arctan2\left(\frac{1}{n}\sum_{j=1}^{n}\sin\alpha_{j},\frac{1}{n}\sum_{j=1}^{n}\cos\alpha_{j}\right)=\arctan2\left(\sum_{j=1}^{n}\sin\alpha_{j},\sum_{j=1}^{n}\cos\alpha_{j}\right)
$$

方向统计书籍：Mardia, Kanti; Jupp, P. E. (1999). Directional Statistics. John Wiley & Sons Ltd. ISBN 978-0-471-95333-3.