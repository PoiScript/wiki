系统的时域分析
  LTI系统的描述及特点
    连续时间LTI系统的数学描述
      连续时间系统的输入输出关系可以用N阶的微分方程描述。
    连续时间LTI系统的特点
      由于LTI系统具有线性特性和时不变特性:
      微分特性或差分特性：
      若 T{f(t)}=y(t)
      则 T{\frac{df(t)}{dt}}=\frac{dy(t)}{dt}
      积分特性或求和特性：
      若 T{f(t)}=y(t)
      则 T{\int{\intfy}f(\tau}d\tau)}=\int{\intfy}y(\tau)d\tau
    连续时间LTI系统的响应
      输入f(t) => 连续时间LTI => 输出y(t)
        经典时域分析方法
        齐次解求解
        特解求解
        卷积法
        零输入响应求解
        零状态响应求解
      经典时域分析方法
        微分方程的全解即系统的完全响应, 由齐次解yh(t)和特解yp(t)组成
        y(t)=yh(t)+yp(t)
        齐次解yh(t)的形式由齐次方程额特征根确定
        特解yp(t)的形式由方程右边的激励信号的形式确定
        齐次解yh(t)的形式
          特征根是不等实根 s1, s2, ..., sn
          yh(t)=K1e^{s1t}+K2e^{s2t}+...+Kne^{snt}
          特征根是等实根 s1=s2=...=sn =s
          yh(t)=K1e^{s1t}+K2te^{s2t}+...+Knt^n-1e^{snt}
          特征根是成对共轭复根 s_i=\tau_i+-j\omega_i, i=n/2
          yh(t)=e^\tau_1t(K_1\cos\omega_1t+K_2\sin\omega_1t)+...+e^\tau_it(K_n-1\cos\omega_it+K_n\sin\omega_it)
        常用激励信号对应的特解形式:
          输入信号 特解
          K A
          K_t A+Bt
          Ke^{at}(特征根s\neqa) Ae^{at}
          Ke^{at}(特征根s=a) Ate^{at}
          K\sin\omega_0或K\cos\omega_0t A\sin\omega_0t+B\cos\omega_0t
          Ke^{at}\sin\omega_0t或Ke^{at}\cost Ae^{at}\sin\omega_0t+Be^{at}\cos\omega_0t
        系统完全响应 = 固有响应 + 强迫响应
          固有响应：仅依赖于系统本身的特性，而和激励信号的形式无关的部分，也即是齐次解。
          强迫响应：由激励信号确定的部分，即是特解。
        系统完全响应 = 暂态响应 + 稳态响应
          暂态响应：指系统完全响应中随时间的增加而很快衰减趋于零的部分。
          稳态响应：指系统完全响应中不随时间的增加而衰减的部分。
        经典法不足之处经典法不足之处
          若激励信号发生变化，则须全部重新求解。
          若初始条件发生变化，则须全部重新求解。
          若微分方程右边激励项较复杂，则难以处理。
          这种方法是一种纯数学方法，无法突出系统响  应的物理概念。
          连续时间系统的冲激响应
      卷积法
        系统完全响应 = 零输入响应 + 零状态响应
        系统的零输入响应是输入信号为零，仅由系统的初始状态单独作用而产生的输出响应。
          数学模型:
            y^{(n)}(t)+a_{n-1}y^{{n-1}}(t)+...+a_1y'(t)+a_0y(t)=0
          求解方法：
            根据微分方程的特征根确定零输入响应的形式
            再由初始条件确定待定系数。
        系统的零状态响应
          当系统的初始状态为零时，由系统的外部激励f(t)产生的响应称为系统的零状态响应，用yf (t)表示。
          求解系统的零状态响应yf (t)方法:
            直接求解初始状态为零的微分方程。
            卷积法：利用信号分解和线性时不变系统的特性求解。
          卷积法求解系统零状态响应的思路
            将任意信号分解为单位冲激信号的线性组合
            求出单位冲激信号作用在系统上的响应— 冲激响应
            利用线性时不变系统的特性，即可求出任意信号f(t)激励下系统的零状态响应yf (t) 。
    连续时间系统的冲激响应
      连续系统的冲激响应定义
        在系统初始状态为零的条件下，以冲激信号d(t)激励系统所产生的输出响应，称为系统的冲激响应，以符号h(t)表示。
        N 阶连续时间LTI系统的冲激响应h(t)满足 h^{(n)}(t)+a_{n-1}h^{(n-1)}(t)+...+a_1h'(t)+a_0h(t)
          = b_m\delta^{(m)}(t)+b_(m-1)\delta^{(m-1)}(t)+...+b_1\delta'(t)+b_0\delta(t)
        冲激平衡法求系统的单位冲激响应
          由于t >=0+后,  方程右端为零，方程变为齐次微分方程，这样h(t)形式与齐次解的形式相同。
          h(t)=(\sum^{n}{i=1}K_ie^{s_it}u(t))
          将h(t)代入微分方程，使方程两边平衡，确定系数Ki
        连续系统的阶跃响应
          g^{(n)}+a_{n-1}g^{(n-1)}(t)+...+a_1g'(t)+a_0g(t)
          = b_mu^{(m)}(t)+b_{m-1}u^{(m-1)}(t)+..+b_1u'(t)+b_0u(t)
          求解方法:
            求解微分方程的冲激响应
            利用冲激响应与阶跃响应的关系
              h(t)=\frac{dg(t)}{dt} g(t)=\int{}{\infty}h(\tau)d\tau
        冲激平衡法求系统的单位冲激响应
          h^{(n)}(t)+a_{n-1}h^{(n-1)}(t)+...+a_1h'(t)+a_0h(t)
          = b_m\delta^{(m)}(t)+b_{m-1}\delta^{(m-1)}(t)+...+b_1\delta'(t)+b_0\delta(t)
          n > m 时 h(t)=(\sum^{n}_{i=1}K_ie^{s_it})u(t)
          n <= m 时 h(t)=(\sum^{n}_{i=1}K_ie^{s_it})u(t)+\sum^{m-n}_{j=0}A_j\delta^{(j)}(t)
          将h(t)代入方程，使两边平衡，确定系数Ki ， Aj
          h(t)=(\sum^{n}_{i=1}K_ie^{s_it})u(t)+\sum^{m-n}_{j=0}A_j\delta^{(j)}(t)
           1. 由系统的特征根来确定u(t)前的指数形式
           2. 由动态方程右边 \deta(t) 的最高阶导数 与方程左边 h(t) 的最高阶导数确定\delta^{(j)}(t)
 卷积积分及其性质
  卷积方法的原理
    就是将信号分解为冲击信号之和，借助系统的冲激响应h(t)，求解系统对任意信号的零状态响应。
  卷积积分的计算
    卷积的定义：
      y(t)=f(t)*h(t)=\int^{\infty}_{-\infty}f(\tau)h(t-\tau)d\tau
    卷积的计算步骤：
      1. 将f(t)和h(t)中的自变量由t改为；
      2. 把其中一个信号h()翻转得h(-)，再平移t；
          h(\tau) =翻折=> h(-\tau) =平移=> h(-(\tau -t)) = h(t-\tau)
      3. 将f(t) 与h(t- t)相乘；对乘积后信号的积分
      4. 不断改变平移量t，计算f(t) h(t- t)的积分
  卷积的性质
    交换律
      f1(t) * f2(t) =   f2(t) * f1(t)
    分配律
      ( f1(t) + f2(t) ) * f3(t) =  f1(t) * f3(t) +  f2(t) * f3(t)
    结合律
      ( f1(t) * f2(t) ) * f3(t) =  f1(t) * (  f2(t) *  f3(t)  )
    平移特性
      已知    f1(t) * f2(t) =  y(t)
      则      f1(t - t1) * f2(t - t2) =  y(t - t1 - t2)
    展缩特性
      已知    f1(t) * f2(t) =  y(t)
      则 f_1(at)*f_2(at) = \frac^{1}_{|a|}y(at)
    微分特性
     已知    y(t) = f(t) * h(t) = h(t) * f(t)
     则      y' (t) = f '(t) * h(t) = h'(t) * f(t)
   积分特性
     已知    y(t) = f(t) * h(t) = h(t) * f(t)
     则     y (-1) (t) = f (-1) (t) * h(t) = h (-1) (t) * f(t)
   等效特性
     已知    y(t) = f(t) * h(t) = h(t) * f(t)
     则     y(t) = f (-1) (t) * h'(t) = h (-1) (t) * f '(t)
   奇异信号的卷积
    延时特性   f (t) * \delta (t -T) = f (t -T)
    微分特性   f (t) * \delta '(t) = f '(t)
    积分特性   f (t) * u(t) = \int_{\infty}f(\tau)d\tau=f^{(-1)}(t)
    等效特性   f1(t) * f2(t) = f^{(-1)}_1(t) * f'_2(t) = f'_1(t) * f^{(-1)}_2(t) = [f'_1(t) * f_2(t)]^{(-1)}
  线性时不变系统的描述及特点
    连续时间系统用N阶常系数微分方程描述
      y^{(n)}(t)+a_{n-1}y^{(n-1)}(t)+...+a_1y'(t)+a_0y(t)
      = b_mf^(m)(t)+b_{m-1}f^{(m-1)}(t)+...+b_1f'(t)+b_0f(t) ai 、 bj为常数。
    离散时间系统用N阶常系数差分方程描述
      \sum^{n}_{i=0}a_iy[k-i]=\sum^{m}_{j=0}b_jf[k-j] ai 、 bj为常数。
    离散LTI系统除具有线性和时不变特性外，还具有:
      差分特性：
        若   T{f[k]}= y[k] 则    T{ f[k] -f[k-1]}= y[k] - y[k-1]
      求和特性：
        若   T{f[k]}= y[k] 则 T{\sum^{k}_{n=\intfy}f{n}} = \sum^{k}_{n=\intfy}y[n]
  离散时间LTI系统的响应
    迭代法求系统响应
      离散时间LTI系统的数学模型为
        \sum^{n}_{i=0}a_iy[k-i]=\sum^{m}_{j=0}b_jf[k-j]
      已知 n 个初始状态{ y[-1], y[-2], y[-3],∙∙∙∙, y[-n] }和输入，由差分方程迭代出系统的输出。
        y[k]=-\sum^{n}_{i=1}a_iy[k-i]+\sum^{m}_{j=0}b_jf[k-j]
    经典时域法求系统响应
      差分方程的全解即系统的完全响应, 由齐次解yh[k]和特解yp[k]组成:
        y[k] = yh[k] + yp[k]
        齐次解yh[k]的形式由齐次方程的特征根确定
        特解yp[k]的形式由方程右边激励信号的形式确定
      齐次解的形式
        特征根是不等实根 r1, r2, ..., rn
          y_h[k]=C_1r_1^k + C_2r_2^k + ... + C_nr_n^k
        特征根是等实根 r1=r2=...=rn
          y_h[k]=C_1r_1^k + C_2k^k + ... + C_nk^{n-1}r^k
        特征根是成对共轭复根 r_{1,2}= a +- jb + pe^{+-j\Omega_0}
          y_h[k]=C_1p^k\cos(\Omega_0k) + C_2p^k\sin\Omega_0k
      常用激励信号对应的特解形式
        输入信号 特解
        a^k(a不是特征根) Aa^k
        a^k(a是特征根) Aka^k
        k^n A_nK^n+A_{n-1}K^{n-1}+...+A_1k+A_0
        a^nK^n a^k(A_nk^n+A_{n-1}k^{n-1}+...+A_1k+A_0)
        \sin\Omega_0k 或 \cos\Omega_0k A_1\cos\Omega_0k+A_2\sin\Omega_0k
        a^k\sin\Omega_0k或a^k\cos\Omega_0k a^k(A_1\cos\Omega_0k+A_2\sin\Omega_0k)
      经典法不足之处
        若差分方程右边激励项较复杂，则难以处理。
        若激励信号发生变化，则须全部重新求解。
        若初始条件发生变化，则须全部重新求解。
        这种方法是一种纯数学方法，无法突出系统响  应的物理概念。
    卷积法求系统响应
      系统完全响应 = 零输入响应 + 零状态响应
      零输入响应求解
        系统的零输入响应是输入信号为零，仅由系统的初始状态单独作用而产生的输出响应。
        数学模型
          \sum^{n}{i=0}a_iy[k-i]=0
        求解方法：
          根据差分方程的特征根确定零输入响应的形式
          再由初始状态确定待定系数。
      零状态响应求解
        当系统的初始状态为零时，由系统的外部激励ｆ[k]产生的响应称为系统的零状态响应，用yf [k]表示。
        求解系统的零状态响应yf [k]方法：
          直接求解初始状态为零的差分方程。
          卷积法: 利用信号分解和线性时不变系统的特性求解。
        卷积法求解系统零状态响应yf [k]的思路
          将任意信号分解为单位脉冲序列的线性组合
          求出单位脉冲序列作用在系统上的响应 — 单位脉冲响应
          利用线性时不变系统的特性，即可求出任意序列f [k]激励下系统的零状态响应yf [k] 。
  离散时间系统的脉冲响应
    单位脉冲响应h[k]定义
      单位脉冲序列h[k]作用于离散时间LTI系统所产生的零状态响应称为单位脉冲响应, 用符号h[k]表示。
      对 N 阶LTI离散时间系统， h[k]满足方程
        \sum^{n}_{i=0}a_ih[k-i]=\sum^{m}_{j=0}b_j\delta[k-j]
    h[k]的求解
      迭代法
         将d [k-j]对系统的瞬时作用转化为系统的等效初始条件。
      等效初始条件法
        等效初始条件由差分方程和h[-1] = h[-2] = ... = h[-n] = 0 递推求出。
    单位阶跃响应g[k]的求解
      单位阶跃序列u[k]作用在离散时间LTI系统上产生的零状态响应称为单位阶跃响应，用符号g[k]表示。
      求解方法:
        迭代法
        经典法
        利用单位阶跃响应与单位脉冲响应的关系
          g[k]=\sum^{k}_{n=\infty}h[n] h[k]=g[k]-g[k-1]
 卷积和及其性质