# 高数（下）物理类知识梳理
> [!Caution]
> 本笔记采用的教材是 _高等数学（第二册）（第五版）物理类专用 四川大学数学学院高等数学教研室 编，高等教育出版社，ISBN:978-7-04-053447-4_
> 
> 笔记内会忽略掉教材中的部分$\ast$内容，因为哪些部分由于自身专业的原因没有学，所以忽略

[听个音乐准备开始](<https://open.spotify.com/track/1K22CVUTZanYO63a9Cp9ie?si=6d8bf7792cdb4661>)

## 第七章 重积分
### 7.1二重积分
[7.1二重积分的概念与性质(2).pdf](<assets/7.1二重积分的概念与性质(2)_eO5AMM.pdf>)
#### 二重积分的概念
> * 二重积分的物理意义$\rightarrow \iint\limits_D \rho(x,y)d\sigma$表示面密度为$f(x,y)$占有平面区域$D$的平面薄片的质量
>* 二重积分的几何意义$\rightarrow$曲顶柱体的体积
>> 1) 若$f(x,y)\geq0,\iint_Df(x,y)d\sigma$表示曲顶柱体的体积
>> 2) 若$f(x,y)\leq0,\iint_Df(x,y)d\sigma$表示曲顶柱体的体积的负值
>> 3) 若$f(x,y)=1,\iint_D1d\sigma$表示区域$D$的面积
1. **定义**：
   设$f(x,y)$是定义在有界闭区域$D$上的有界函数，将区域$D$任意分成$n$个小区域$\Delta \sigma_i(i=1,2,……,n)$,任取一点$(x_i,y_i)\in\sigma_i$,若存在一个常数$I$,使

> [!Note]
> $$I=\lim\limits_{\lambda\rightarrow0}\sum\limits_{i=1}^n f(x_i,y_i)\Delta\sigma_i=记作=\iint\limits_D f(x,y)d\sigma$$

> [!Warning]
> 1. 积分存在时，其值与区域的分法和点$(x_i,y_i)$的取法无关
> 2. 存在条件（充分条件）：当$f(x,y)$在有界比区域上连续时，定义中和式的极限必存在，即二重积分必存在
> 3. $f(x,y)在$D$上*有界*是二重积分存在的*必要条件*；*连续*是二重积分存在的*充分条件*

2.**性质：**
> [!Note]
> 1.  $\iint\limits_D kf(x,y)d\sigma=k\iint\limits_Df(x,y)d\sigma.$
> 2.  $\iint\limits_D [f(x,y)\pm g(x,y) ]d\sigma=\iint\limits_D f(x,y)d\sigma\pm g(x,y)d\sigma.$ $$线性性质：\iint\limits_D [kf(x,y)+mg(x,y)]d\sigma=k\iint\limits_D f(x,y)d\sigma+m\iint_D g(x,y)d\sigma$$
> 3.  对区域具有可加性：$$\iint\limits_D f(x,y)d\sigma=\iint\limits_{D_1}f(x,y)d\sigma+\iint\limits_{D_2}f(x,y)d\sigma$$ $$(D=D_1\cup D_2,D_1,D_2无公共内点)$$
> 4.  若$\sigma$为$D$的面积，$\sigma=\iint\limits_D 1\cdot d\sigma=\iint\limits_D d\sigma$
> 5.  若在$D$上$f(x,y)\leq g(x,y),$则有$\iint\limits_D f(x,y)d\sigma\leq \iint\limits_D g(x,y)d\sigma$ $$特殊地：|\iint\limits_D f(x,y)d\sigma|\leq\iint\limits_D |f(x,y)|d\sigma$$
> 6.  设$M、m$分别是$f(x,y)$在闭区间$D$上地最大值和最小值，$\sigma$为$D$地面积，则$$m\sigma\leq\iint\limits_D f(x,y)d\sigma\leq M\sigma$$
> 7. **(二重积分的中值定理)** 设函数$f(x,y)$在闭区间$D$上连续，$\sigma$为$D$的面积，则在$D$上至少存在一点$(\xi,\eta)$使得$$\iint\limits_D f(x,y)d\sigma=f(\xi,\eta)\cdot\sigma$$
>    >证明$$\iint\limits_D f(x,y)d\sigma=f(\xi,\eta)\cdot\sigma$$:
>    >设$m\leq f(x,y)\leq M$
>    >根据估值定理：$m\sigma\leq \iint\limits_D f(x,y)d\sigma\leq M\sigma$
>    >$\therefore m\leq \frac{1}{\sigma}\iint\limits_D f(x,y)d\sigma\leq M$
>    >根据介值定理（*如果函数$f(x,y)$在闭区间$[a,b]$上连续，则可以取到介于最大值和最小值之间的任何值*）
>    >存在点$(\xi,\eta)$,使得$f(\xi,\eta)=\frac{1}{\sigma}\iint\limits_D f(x,y)d\sigma$
>    >$\therefore \iint\limits_D f(x,y)d\sigma=f(\xi,\eta)\cdot \sigma$

---

#### 二重积分的计算

[7.2二重积分的计算法(2).pdf](<assets/7.2二重积分的计算法(2)_QyEVkx.pdf>)
##### 基础知识
**1. 利用直角坐标计算二重积分**
> [!Note]
> * $x$域型：$a<x<b,\varphi_1(x)<y<\varphi_2(x)$ $$\iint\limits_D f(x,y)d\sigma=\int_a^b dx\int_{\varphi_1(x)}^{\varphi_2(x)}f(x,y)dy$$
> * $y$域型：$a<y<b,\psi_1(y)<x<\psi_2(y)$ $$\iint\limits_D f(x,y)d\sigma=\int_a^b dy\int_{\psi_1(y)}^{\psi_2(y)}f(x,y)dx$$

**2.利用极坐标计算二重积分**
> [!Note]
> 面积元素：$d\sigma=rdrd\theta$
> $$\begin{cases}
> \text{$x=r\cos\theta，$}\\
> \text{$y=r\sin\theta.$}\\
> \end{cases}$$
> $$\iint\limits_Df(x,y)d\sigma=\iint\limits_{D'} f(r\cos\theta,r\sin\theta)rdrd\theta$$
> 其中，$D'$表示$D$区域的极坐标表示
* <u>二重积分转化为二次积分的公式</u>
> [!Note]
> 1. 级点$O$在区域$D$的边界曲线之外时
> 
> <div style="display: flex; gap: 10px; justify-content: center;">
>   <img src="https://github.com/ofheikan/image/blob/main/image_WirjSx.png" style="width: 48%; height: auto;">
>   <img src="https://github.com/ofheikan/image/blob/main/image_LpSdhq.png" style="width: 48%; height: auto;">
> </div>
> 
> 区域特征如图
> $$ \begin{cases}
> \text{$\alpha\leq\theta\leq\beta$}\\
> \text{$\varphi_1(\theta)\leq\rho\leq\varphi_2(\theta)$}\\
> \end{cases} $$
> $$\iint\limits_Df(\rho\cos\theta,\rho\sin\theta)\rho d\rho d\theta=\int_{\alpha}^{\beta}d\theta\int_{\varphi_1(\theta)}^{\varphi_2(\theta)}f(\rho\cos\theta,\rho\sin\theta)\rho d\rho$$
> 2.极点$O$刚好在区域$D$的边界曲线上时
> <div style="display:flex;justify-content:center">
>  <img src="https://github.com/ofheikan/image/blob/main/image_6ObX5D.png" style="width:54%;height:auto;">
></div>
>
> $$\begin{cases}
> \text{$\alpha\leq\theta\leq\beta$}\\
> \text{$0\leq\rho\leq\varphi(\theta)$}\\
> \end{cases}$$
> $$\iint\limits_D f(\rho\cos\theta,\rho\sin\theta)\rho d\rho d\theta=\int_{\alpha}^{\beta}d\theta\int_{0}^{\varphi(\theta)}f(\rho\cos\theta,\rho\sin\theta)\rho d\rho$$
> 3. 极点$O$在区域$D$的边界曲线内时
> <div style="display:flex;justify-content:center"><img src="https://github.com/ofheikan/image/blob/main/image_xDCC8J.png" style="width:48%"></img></div>
>
> $$\begin{cases}
> \text{$0\leq\theta\leq2\pi$} \\
> \text{$0\leq\rho\leq\varphi(\theta)$}\\
> \end{cases}$$
> $$\iint\limits_D f(\rho\cos\theta,\rho\sin\theta)\rho d\rho d\theta=\int_{0}^{2\pi}d\theta\int_0^{\varphi(\theta)}f(\rho\cos\theta,\rho\sin\theta)\rho d\rho$$


**3.二重积分的一般变量替换**
设被积函数$f(x,y)$在区域$D$上连续，若变换$x=x(u,v),y=y(u,v)$满足以下条件：
> [!Note]
> <div style="display:flex;justify-content:center"><img src="https://picx.zhimg.com/70/v2-e2ca7a464cb74c8cd9789f5b9d5b4764_1440w.avis?source=172ae18b&biz_tag=Post" style="width:80%"></img></div>
>
> 1. 将$uOv$平面上的区域$D_*$上的点一对一地变为$D$上的点；
> 2. $x(u,v),y(u,v)$在$D_*$上有连续的一偏导数，且雅可比行列式$$J=\frac{\partial(x,y)}{\partial(u,v)}=\left|\begin{array}{c}
> \frac{\partial x}{\partial u}&\frac{\partial x}{\partial v}\\
> \frac{\partial y}{\partial u}&\frac{\partial y}{\partial v}\\
>\end{array}\right|\neq 0$$则$$\iint\limits_D f(x,y)dxdy=\iint\limits_Df[x(u,v),y(u,v)]|J|dudv$$
---

##### 题目练习


---

### 7.2三重积分
[7.3三重积分定义及直角坐标系下的计算.pdf](<assets/7.3三重积分定义及直角坐标系下的计算_rN7J_3.pdf>)
#### 三重积分的概念

#### 三重积分的计算
---
### 7.3重积分的应用
#### 几何应用——曲面面积
#### 在力学中的应用

## 第八章 曲线积分 曲面积分 矢量分析初步
### 8.1 曲线积分
[1.第一型曲线积分.pdf](<assets/8.1第一型曲线积分_tNXCSh.pdf>)
[2.第二型曲线积分.pdf](<assets/8.1第二型曲线积分_fZa4up.pdf>)
[3.格林公式 平面曲线积分与路径无关的条件.pdf](<assets/8.3格林公式 平面曲线积分与路径无关的条件_3uNj3t.pdf>)

**第一型曲线积分和第二型曲线积分的别称（便于分辨）**

| 第一型曲线积分 | 第二型曲线积分 |
| :--: | :--: |
|  对弧长的曲线积分    |   对坐标的曲线积分   |



#### 第一型曲线积分
##### 基础知识
> [!Note]
> 1. **定义**：$$\int\limits_{L}f(x,y)ds=\lim\limits_{d\rightarrow0}\sum\limits_{i=1}^{n}f(\xi_i,\eta_i)$$***物理意义**：线密度为$\mu=f(x,y)$的弧段$L$的质量，即$$M=\int_L f(x,y)ds$$*
> 2. **性质**
> * *线性性质* $$\int\limits_{L}[\alpha f(x,y)\pm \beta g(x,y)]ds=\alpha\int_{L}f(x,y)ds\pm\beta\int_{L}g(x,y)ds$$
> * *可加性*   $$设L_1与L_2首尾相接成L$$ $$\int_{L}f(x,y)ds=\int_{L_1}f(x,y)ds+\int_{L_2}f(x,y)ds,$$
> * *性质3* $$\int_L ds=L$$
> 3. **计算**
>   （1）有参数方程$$x=x(t),y=y(t).$$
>   则有$ds=\sqrt{x'^2(t)+y'^2(t)}dt$  $$\int_L f(x,y)ds=\int_{\alpha}^{\beta}f[x(t),y(t)]\sqrt{x'^2(t)+y'^2(t)}dt$$
>   （2）有参数方程$$y=y(x).$$则有$ds=\sqrt{1+y'^2(x)}dx$ $$\int_L f(x,y)ds=\int_a^b f[x,y(x)]\sqrt{1+y'^2(x)}dx.$$ $$如果是x=x(y)则类似$$
>   （3）如果$L$由方程$\rho=\rho(\varphi)$给出 $$ds=\sqrt{\rho^2(\varphi)+\rho'^2(\varphi)}d\varphi,$$ $$\int_L f(x,y)ds=\int_{\alpha}^{\beta}f[\rho(\varphi)\cos\varphi,\rho(\varphi)\sin\varphi]\sqrt{\rho^2(\varphi)+\rho'^2(\varphi)}d\varphi$$
>   （4）有参数方程$$x=x(t),y=y(t),z=z(t)$$ $$ds=\sqrt{x'^2(t)+y'^2(t)+z'^2(t)}dt$$ $$\int_L f(x,y)=\int_{\alpha}^{\beta} f[x(t),y(t),z(t)]\sqrt{x'^2(t)+y'^2(t)+z'^2(t)}dt$$

> [!Warning]
> 在这些计算中$\int$中的下界一定小于上界

##### 练习题目
###### 例题1 x(t),y(t)参数
计算$I=\int_c xyds$,其中$C$的方程为$x=a\cos t,y=a\sin t,t\in[0,\frac{\pi}{2}]$
> 此式属于$x=x(t),y=y(t)$参数方程类型，
> $\therefore $思路应该为$ds=\sqrt{x'^2(t)+y'^2(t)}dt,$
> $\int_Lf(x,y)ds=\int_0^{\frac{\pi}{2}}f(x_t,y_t)ds.$

> [!Tip]
> $\because x_t=a\cos t,y_t=a\sin t$
> $\therefore ds=a\ dt$
> $\therefore \int_c f(x,y) ds=\int_{0}^{\frac{\pi}{2}}af(a\cos t,a\sin t)dt=\int_0^{\pi/2}a\cdot a\cos t\cdot a\sin t dt=\int_0^{\pi/2}\frac{a^3}{2}\sin 2t\cdot dt=\frac{1}{4}a^3\int_0^{\pi/2}\sin 2t\cdot d(2t)=-\frac{1}{4}a^3\cos 2t|^{\frac{\pi}{2}}_0 =\frac{a^3}{2}$

###### 例题2 y和x多种复合参数
计算$\oint_L\sqrt{y}ds,$其中$L$为抛物线$y=x^2,$直线$x=1$及$x$轴所围成的曲边三角形的整个边界

<image style="width:30%;margin-bottom:20px;" src="https://github.com/ofheikan/image/blob/main/image_jkYVGx.png">


> 因为是闭合的三角形，所以要分成$OB,BA,AO$三段计算
> 其中
> $$\begin{cases}
> \text{OB:$\sqrt{y}=x,ds=\sqrt{1+4x^2}dx$}\\
> \text{OA:$\sqrt{y}=0,ds=dx$}\\
> \text{AB:$\sqrt{y}=\sqrt{y},ds=dy$}\\
> \end{cases}
> $$
>
> $\int_{0}^{1}x\cdot\sqrt{1+4x^2}dx$可以用换元$u=1+4x^2$来求

> [!Tip]
> $\oint_L \sqrt{y}ds=\int_{OB}+\int_{OA}+\int_{AB}=\int_{0}^{1}x\cdot\sqrt{1+4x^2}dx+0+\int_{0}^{1}\sqrt{y}dy=\frac{5\sqrt{5}-1}{12}+\frac{2}{3}=\frac{5\sqrt{5}+7}{12}.$

###### 例题3 x,y可多样解读
计算$\int\limits_L xe^{\sqrt{x^2+y^2}}ds,$其中$L$是从$A(0,1)$沿圆周$x^2+y^2=1$到$B(\frac{\sqrt 2}{2},-\frac{\sqrt 2}{2})$处的一段劣弧
>此题既可以被视作$\rho=\rho(\varphi)$，此时$\rho$为极坐标半径$\rho=1,$
>也可以视作$x=x(t),y=y(t)$

> [!Tip]
> 视作$\rho=\rho(\varphi),\varphi\in (-\frac{\pi}{4},\frac{\pi}{2})$
> 由此可得$ds=\sqrt{\rho^2+\rho'^2}d\varphi=d\varphi,$
> $\therefore \int\limits_L xe^{\sqrt{x^2+y^2}}ds=\int_{-\frac{\pi}{4}}^{\frac{\pi}{2}}e\cos\varphi d\varphi=(1+\frac{\sqrt{2}}{2})e.$

#### 第二型曲线积分
##### 基础知识

> [!Note]
>1.**定义**$$L上定义一个向量函数\vec F(x,y)=(P(x,y),Q(x,y))$$
> 取极限$\lim\limits_{\lambda\rightarrow0}]\sum\limits_{k=1}^{n}[P(\xi_k,\eta_k)\Delta x_k+Q(\xi_k,\eta_k)\Delta y_k]$记作$\int_L P(x,y)dx+Q(x,y)dy$
>
> 其中$\int_L P(x,y)dx=\lim\limits_{\lambda\rightarrow0}\sum\limits_{k=1}^{n}P(\xi_k,\eta_k)\Delta x_k$被称为对$x$的曲线积分
> $\int_L Q(x,y)dx=\lim\sum\limits_{k=1}^{n}Q(\xi_K,\eta_k)\Delta y_k$被称为对$y$的曲线积分
>
> * 类似地对于$\vec F(x,y,z)=[P(x,y,z),Q(x,y,z),R(x,y,z)]$
>  $$\int_L \vec F\cdot d\vec s=\int_L P(x,y,z)dx+Q(x,y,z)dy+R(x,y,z)dz$$
> 2. **性质**
>   （1）若$L$可以被分为$k$条光滑有向曲线弧$L_i $,则$$\int_L P(x,y)dx+Q(x,y)dy=\sum\limits_{i=1}^k \int_{L_i}P(x,y)dx+Q(x,y)dy$$
>   (2)对于反向弧$L^-$有$$\int_{L^-}P(x,y)dx+Q(x,y)dy=-\int_L P(x,y)dx+Q(x,y)dy$$

> [!Warning]
> * 注意分弧段的方向
> * 定积分是第二类曲线积分的特例
> * $\Delta x_k$可正可负

> [!Note]
> 3. **计算**
> _（1）对与有参数方程_$$\begin{cases}
> \text{$x=\varphi(t),$}\\
> \text{$y=\psi(t),$}\\
> \text{$\alpha<t<\beta$}\\
> \end{cases}$$
> $$\int_L P(x,y)dx+Q(x,y)dy=\int_{\alpha}^{\beta} \{P[\varphi(t),\psi(t)]\varphi'(t)+Q[\varphi(t),\psi(t)]\psi'(t)\}dt$$
> _（2）_对于参数为__ $y=\psi(x),x:a\rightarrow b$
> $$\int_L P(x,y)dx+Q(x,y)dy=\int_{a}^{b}\{P[x,\psi(x)]+Q[x,\psi(x)]\psi'(x)\}dx$$
> 若为$x=\varphi(y)$则反之
> _（3）对于空间曲线_ $$\Gamma=\begin{cases}
> \text{$x=\phi(t)$}\\
> \text{$y=\psi(t)$}\\
> \text{$z=\omega(t)$}
> \end{cases}$$
> $$\int_LP(x,y,z)dx+Q(x,y,z)dy+R(x,y,z)dz=\int_{\alpha}^{\beta} \{P[\phi(t),\psi(t),\omega(t)]\phi'(t)+Q[\phi(t),\psi(t),\omega(t)]\psi'(t)+R[\phi(t),\psi(t),\omega(t)]\omega'(t)\}dt$$
> （4）对于空间曲线$$\Gamma=\begin{cases}
> \text{$y=\varphi(x)$}\\
> \text{$z=\psi(x)$}
> \end{cases}$$
> $$\int_L P(x,y,z)dx+Q(x,y,z)dy+R(x,y,z)dz=\int_{a}^{b}\{P[x,\varphi(x),\psi(x)]+Q[x,\varphi(x),\psi(x)]\varphi'(x)+R[x,\varphi(x),\psi(x)]\psi'(x)\}dx$$

##### 练习题目
###### 例题1 
计算$\int_L y^2 dx$,其中
（1）$L$为按逆时针方向绕行的上班圆周$x^2+y^2=a^2;$
（2）$L$为从点$A(a,0)$沿$x$轴到点$B(-a,0)$的直线段.
>在此题目中$P=y^2,Q=0$
> （1）可以把$x,y$看成参数方程$$\begin{cases}
> \text{$x=a\cos t$}\\
> \text{$y=a\sin t$}\\
> \end{cases}$$
>(2)$x,y$的表达式是：
>$$\begin{cases}
>\text{$x=t,$}\\
>\text{$y=0$}\\
>\end{cases}$$

> [!Tip]
> (1)$\int_L y^2 dx=-\int_{\alpha}^{\beta} a^2\sin^2 t \cdot a\sin t \cdot dt=a^3\int_{0}^{\pi} (1-\cos^2 t)d\cos t=a^3 (\cos t-\frac13\cos^3 t)|_0^{\pi}=-\frac{4a^3}{3}$
> (2)$\int_L y^2dx=0$

###### 例题2 x=φ(y)
计算$\int_L xydx,$其中$L$为沿抛物线$y^2=x$从点$A(-1,1)$到$B(1,1)$的一段.
> 该题属于$x=\varphi(y)的类型$
> $\therefore \int_L xydx=\int_{-1}^{1}y^2\cdot yd(y^2)$

> [!Tip]
> $\int_L xydx=\int_{-1}^{1}2y^4dy=\frac{2y^5}{5}|_{-1}^{1}=\frac{4}{5}$

###### 例题3 路径不同，积分结果相同
计算$\int_L 2xydx+x^2dy,$其中$L$为
（1）抛物线$L:y=x^2,x:0\rightarrow1;$
（2）抛物线$L:x=y^2,y:0\rightarrow1;$
（3）有向折线$L:\vec{OA}+\vec{AB},$其中$A(1,0),B(1,1)$
> (1) 属于类型$y=\varphi(x)$,做法应为$\int_L Pdx+Qdy=\int_0^1 [P(x,\varphi(x))+Q(x,\varphi(x))\varphi'(x)]dx$
> (2)属于类型$x=\varphi(y),\int_L Pdx+Qdy=\int_{0}^{1}[P\varphi'(y)+Q]dy$
> (3)分为两段，且两端均视为$$\begin{cases}
> \text{$x=\varphi(t)$}\\
> \text{$y=\psi(t)$}\\
> \end{cases}$$
> 的参数方程类型

> [!Tip]
> (1)$$\because y=x^2,x\in[0,1]$$
> $$\therefore \int_L 2xydx+x^2dy=\int_0^1[2x\cdot x^2+x^2\cdot2x]dx=1$$
> (2)$$\because x=y^2,y\in[0,1]$$
> $$\therefore \int_L2xydx+x^2dy=\int_0^1[2y^3\cdot 2y+y^4]dy=1$$
> （3）$\vec{\text{OA}}$段$$\begin{cases}
> \text{$x=t$}\\
> \text{$y=0$}\\
> \text{$t\in[0,1]$}\\
> \end{cases}$$
> $\vec{\text{OB}}$段$$\begin{cases}
> \text{$x=1$}\\
> \text{$y=t$}\\
> \text{$t\in[0,1]$}\\
> \end{cases}$$
> $$\therefore \int_L 2xydx+x^2dy=\int_0^1 [0+t^2d0]+\int_0^12t\cdot 0 +1dt=1$$

###### 例题4
计算$\int_{\Gamma}x^3dx+3zy^2dy-x^2ydz$,其中$\Gamma$ 是从点$A(3,2,1)$到点$B(0,0,0)$的直线段$AB$
> 此题属于类型$$\begin{cases}
> \text{$x=\varphi(t)$}\\
> \text{$y=\psi(t)$}\\
> \text{$z=\omega(t)$}\\
> \end{cases}$$

> [!Tip]
> 令$$\begin{cases}
> \text{$x=3t$}\\
> \text{$y=2t$}\\
> \text{$z=t$}\\
> \text{$t:1\rightarrow 0$}\\
> \end{cases}$$
> $$\therefore \int_Lx^3dx+3zy^2dy-x^2ydz=\int_1^0 27t^3\cdot 3dt+12t^3\cdot 2dt-18t^3dt=-\frac{87}{4}$$

###### 例题5
设在立场$\vec F=(y,-x,z)$作用下，指点由$A(R,0,0)$沿$\Gamma$移动到$B(R,0,2\pi k),$其中$\Gamma$为
（1）$x=R\cos t,y=R\sin t,z=kt$
（2）沿$\vec{AB}$
求力的做功
>(1)根据体干信息$$\vec{F}\cdot ds=\int_{\Gamma}R\sin t\cdot dx-R\cos t\cdot dy+kt\cdot dz$$
> 该题属于类型$$\begin{cases}
> \text{$x=\varphi(t)$}\\
> \text{$y=\psi(t)$}\\
> \text{$z=\omega(t)$}\\
> \end{cases}$$
>(2)若$\Gamma沿\vec{AB}$移动，则关于$x,y,z$的参数方程为
>$$\begin{cases}
>\text{$x=R$}\\
>\text{$y=0$}\\
>\text{$z=2\pi t$}\\
>\text{$t\in[0,k]$}
>\end{cases}$$

> [!Tip]
> （1）$$由题\begin{cases}
> \text{$x=R\cos t$}\\
> \text{$y=R\sin t$}\\
> \text{$z=kt$}\\
> \end{cases}$$
> 且易得$t\in [0,2\pi]$
> $$\therefore \int_{\Gamma} R\sin tdx-R\cos tdy+ktdz=\int_0^{2\pi} (-R\sin t\cdot Rsint-R\cos t\cdot R\cos t+k^2t)dt$$
> $$=-\int_0^{2\pi} (R^2\sin^2 t+R^2\cos^2 t-k^2 t)dt=\int_0^{2\pi}(-R^2+k^2t)dt=(-R^2t+\frac{k^2t^2}{2})|_0^{2\pi}=2\pi^2k^2-2\pi R^2$$
> （2）
> $\because$
> $$\begin{cases}
>\text{$x=R$}\\
>\text{$y=0$}\\
>\text{$z=2\pi t$}\\
>\text{$t\in[0,k]$}
>\end{cases}$$
> 
> $$\vec{F}\cdot ds=\int_{\Gamma}R\sin t\cdot dx-R\cos t\cdot dy+kt\cdot dz$$
> $\therefore$
> $$\int_{\Gamma}R\sin t\cdot dx-R\cos t\cdot dy+kt\cdot dz=\int_0^{k}2\pi t\cdot2\pi\cdot dt=2\pi t^2|_0^{k}=2\pi^2 k^2$$
> ###### 例题6
求$I=\int_\Gamma (z-y)dx+(x-z)dy+(x-y)dz$,其中$$\Gamma=\begin{cases}
\text{$x^2+y^2=1$}\\
\text{$x-y+z=2$}\\
\end{cases}$$,从z轴看为顺时针方向.
> $$\begin{cases}
> \text{$x=\cos \theta$}\\
> \text{$y=\sin \theta$}\\
> \text{$z=2-\cos \theta+\sin \theta$}\\
> \end{cases}$$
> $z-y=2-\cos\theta+\sin\theta-\sin\theta=2-\cos\theta$
> $x-z=\cos\theta-2+\cos\theta-\sin\theta=2\cos\theta-2-\sin\theta$
> $x-y=\cos\theta-\sin\theta$
> $$\therefore\begin{cases}
> \text{$P=2-\cos\theta$}\\
> \text{$Q=2\cos\theta-2-\sin\theta$}\\
> \text{$R=\cos\theta-\sin\theta$}\\
> \end{cases}$$

> [!Tip]
>$$I=\int_{2\pi}^{0}-(2-\cos\theta)\sin\theta+(2\cos\theta-2-\sin\theta)\cos\theta+(\cos\theta-\sin\theta)(\sin\theta+\cos\theta)$$
> $$=\int_{2\pi}^0(\sin\theta\cos\theta-2\sin\theta+2\cos^2\theta-2\cos\theta-\sin\theta\cos\theta+cos^2\theta-\sin^2\theta)d\theta$$
> $$=\int_{2\pi}^0 (-2\sin\theta+3\cos^2\theta-2\cos\theta-\sin^2\theta)d\theta$$
> $$ =\int_{2\pi}^0(-2\sin\theta-2\cos\theta-2\cos2\theta+1)d\theta=-2\pi$$

#### 两类积分之间的关系
##### 基础知识
1.两类积分之间的联系公式$$\int_L Pdx+Qdy=\int\limits_L (P\cos\alpha+Q\cos\beta)ds$$
> [!Warning]
>有关$\cos\alpha$和$\cos\beta$:
> 令：
> $$\begin{cases}
> \text{$x=\varphi(t)$}\\
> \text{$y=\psi(t)$}\\
> \end{cases}$$
> 曲线弧$L$上的一动点的切向量：$\vec t=\{\varphi'(t),\psi'(t)\}$
> 曲线弧$L$上$(x,y)$处切线向量的方向角为$\alpha,\beta$
> $\vec T=(\varphi'(t),\psi'(t))$为动点$(x,y)$处的一个切向量，切向量的方向余弦：
> $$\cos\alpha=\frac{\varphi'(t)}{\sqrt{\varphi'^2(t)+\psi'^2(t)}}\ \cos\beta=\frac{\psi'(t)}{\sqrt{\varphi'^2(t)+\psi'^2(t)}}$$


再空间$\Gamma$上时$$\int_{\Gamma}Pdx+Qdy+Rdz=\int_{\Gamma}(P\cos\alpha+Q\cos\beta+R\cos\gamma)ds$$
$$\downarrow_{令\vec{A}=(P,Q,R),
d\vec{s}=(dx,dy,dz),
\vec t=(\cos\alpha,\cos\beta,\cos\gamma)}$$
$$\int_L \vec A d\vec s=\int_L\vec A \vec t ds$$
$$\downarrow _{记\vec A在\vec t上的投影为A_t}$$
$$\int_L\vec Ad\vec s=\int_L A_t ds$$

> [!Warning]
> 
>$\vec t$是有向弧元$d\vec s$的单位切向量

##### 题目练习
###### 例题1
设$M=\max\sqrt{P^2+Q^2},P(x,y),Q(x,y)$在$L$上连续，曲线段$L$的长度为$s$,证明$$|\int_LPdx+Qdy|\leq Ms$$
> 此题需要使用到令$\vec A=(P,Q),d\vec s=(dx,dy),\vec t=(\cos\alpha,\cos\beta)$相关的内容，也就是要将$\int_L \vec Ad\vec s$变为$\int_L A_t ds$后进行对比

> [!Tip]
>$\int_LPdx+Qdy=\int_L (P\cos\alpha+Q\cos\beta)ds\leq \int_L|P\cos\alpha+Q\cos\beta|ds$
> 令$\vec A=(P,Q),\vec t=(\cos\alpha,\cos\beta)$，两者间的夹角为$\theta$
> $\therefore \int_L|P\cos\alpha+Q\cos\beta|ds=\int_L |\vec A\vec t| ds =\int_L |\vec A||\cos\theta|ds=\int_L\sqrt{P^2+Q^2}|\cos\theta|ds\leq Ms$

###### 例题2
将积分$\int_L P(x,y)dx+Q(x,y)dy$化为对弧长的积分，其中$L$沿上半圆周$x^2+y^2-2x=0$从$O(0,0)$到$B(2,0).$
> <!--啊呀好烦啊，这个怎么这么难搞啊，烦死个人，跟着PPT写的内容怎么还和书上的不一样啊啊啊啊啊啊啊啊好烦人啊，不想写了，一想到高数考的那个鬼样我又不得不做，好像有人快点来安慰我呀，我简直活人微死了，我现在手心全是汗，真的好爆炸了！！！！！！！我现在好像走开啊，再过几天就是我生日了。现在弄这个一点都不开心，为什么高数的进度这么慢啊，真的好难搞啊，暑假都放了好几天了才弄了这么一点，这道题前面写了一堆的思路结果方向直接一个错了好伤心啊，怎么能这样啊，这日子真是一天比一天糟糕了。我恨睡觉，一睡醒就脑子跟浆糊一样，尽写的一些逻辑不通莫名奇妙的东西，为什么这个wj-markdown-editor的备注是这个颜色的啊啊啊啊，太抢眼了，好烦人啊，shale豆沙了🤮.这个部分书上连体力都没有笑死，PPT上还整这些奇奇怪怪的题做，后面的PPT内容还有什么思考与总结，简直放屁！还有几道什么思考题乱七八糟的。zr你看看你做的什么构式-->
> 
> 根据弧长微元公式$ds=\sqrt{1+(\frac{dy}{dx})^2}dx$得出$ds,dx,dy$
> 然后可算出$\cos\alpha,\cos\beta$
> 最终代入$$\int_L P(x,y)dx+Q(x,y)dy=\int_L(P(x,y)\cos\alpha+Q(x,y)\cos\beta)ds$$计算出结果

> [!Tip]
>  由关于$L$的圆周公式可得$y=\sqrt{2x-x^2}$
> $\therefore dy=\frac{1-x}{\sqrt{2x-x^2}}dx,$
> $\therefore ds=\sqrt{1+\frac{1-2x+x^2}{2x-x^2}}dx=\frac{1}{\sqrt{2x-x^2}}dx$
> $$\therefore
> \begin{cases}
> \text{$\cos\alpha=\frac{dx}{ds}=\sqrt{2x-x^2}$}\\
> \text{$\cos\beta=\frac{dy}{ds}=1-x$}\\
> \end{cases}$$
> $I=\int_0^2 [P(x,y)\sqrt{2x-x^2}+Q(x,y)(1-x)]\frac{dx}{\sqrt{2x-x^2}}$

###### 例题3
将$\int_{\Gamma}Pdx+Qdy+Rdz$化为第一类曲线积分，其中，$$\Gamma:\begin{cases}
\text{$x=t$}\\
\text{$y=t^2$}\\
\text{$z=t^3$}\\
\end{cases}$$
相应与$t$从$1$变道$0$的一段曲线弧
> 在空间上将第二型曲线积分化为第一型$$\rightarrow \int_LPdx+Qdy+Rdz=\int_L(P\cos\alpha+Q\cos\beta+R\cos\gamma)ds$$

> [!Tip]
> $$\begin{cases}
> \text{$dx=1$}\\
> \text{$dy=2t$}\\
> \text{$dz=3t^2$}\\
> \end{cases}$$
> $$\cos\alpha=\frac{1}{\sqrt{1+4t^2+9t^4}},\cos\beta=\frac{2t}{\sqrt{1+4t^2+9t^4}},\cos\gamma=\frac{3t^2}{\sqrt{1+4t^2+9t^4}}$$
> $$\therefore\int_LPdx+Qdy+Rdz=\int_1^0(\frac{P}{\sqrt{1+4t^2+9t^4}}+Q\frac{2t}{\sqrt{1+4t^2+9t^4}}+R\frac{3t^2}{\sqrt{1+4t^2+9t^4}})ds$$

#### 与路径无关的积分和格林公式
[8.3格林公式 平面曲线积分与路径无关的条件.pdf](<assets/8.3格林公式 平面曲线积分与路径无关的条件_dqpvVw.pdf>)
##### 基础知识
###### 区域连通性分类
$$设D为平面区域$$
> [!Note]
>* 如果$D$内任意闭曲线所围成的部分属于$D$，则称$D$为平面**单连通区域**
>* 如果$D$内存在闭合曲线$l$所围成的区域不完全属于$D$,则称$D$为**复连通区域**
>  
<div style="display: flex; justify-content: center; align-items: flex-start; gap: 30px;">
  <!-- 第一个图片单元 -->
  <div style="text-align: center;">
    <img src="https://github.com/ofheikan/image/blob/main/image_NnH--_.png"
         style="width: 200px; height: auto; display: block; margin: 0 auto;" />
    <p style="font-size:20px; font-family:'Noto Serif SC', serif; margin-top: 8px;">
      单连通区域:<b>没有洞</b>
    </p>
  </div>

  <!-- 第二个图片单元 -->
  <div style="text-align: center;">
    <img src="https://github.com/ofheikan/image/blob/main/image_M18WNM.png"
         style="width: 200px; height: auto; display: block; margin: 0 auto;" />
    <p style="font-size:20px; font-family:'Noto Serif SC', serif; margin-top: 8px;">
      复连通区域:<b>有洞</b>
    </p>
  </div>
</div>


,
