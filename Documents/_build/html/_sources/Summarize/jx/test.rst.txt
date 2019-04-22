Kirchhoff积分公式推导
**********************

如果围绕着震源所在的某一闭合面 Q 上已知波动的位移位 :math:`\varphi(x, y, z)` 及其导数，
且这些值是连续的，那么可以算出 Q 面外任意观测点 :math:`M\left(x_{1}, y_{1}, z_{1}\right)` 上
由源引起的位移位 :math:`\varphi` 的解，该解用Kirchhoff积分公式来计算

.. math::

    \varphi\left(x_{1}, y_{1}, z_{1}\right)=-\frac{1}{4 \pi} \oint_{Q}\left\{[\varphi] \frac{\partial}{\partial n}\left(\frac{1}{r}\right)-\frac{1}{r}\left[\frac{\partial r}{\partial n}\right]-\frac{1}{v r}\left[\frac{\partial \varphi}{\partial t}\right]\right\} d Q

:math:`[\varphi]` 为延时位，
:math:`\varphi\left(x, y, z, t-\frac{r}{V}\right)=[\varphi]`

Kirchhoff积分公式推导：

假设在时刻t，点 :math:`M\left(x_{1}, y_{1}, z_{1}\right)` 上观测到的位函数为
:math:`\varphi\left(x_{1}, y_{1}, z, t\right)` ，
则在前一时刻 :math:`t_{1}=t-\frac{r}{V}` ，在闭合曲面Q上的位移是
:math:`\varphi\left(x, y, z, t-\frac{r}{V}\right)=[\varphi]` ，
称 :math:`[\varphi]` 为“延迟位”，r为点M到Q上点的距离。
