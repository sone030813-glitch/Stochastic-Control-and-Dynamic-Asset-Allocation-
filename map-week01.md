mindmap
  root((随机微积分<br/>Stochastic Calculus))
    (基础规则<br/>Itô Basics)
      ::icon(fa fa-book)
      [乘法表核心]
        dW * dW = dt
        dt * dW = 0
        dt * dt = 0
      [机械化流程]
        1. 算偏导 fx, fxx
        2. 代入 dX
        3. 展开并查表
      [凸性修正]
        因为 dW 太抖了
        需要二阶项 0.5 * sigma^2

    (关键推导<br/>Derivations)
      ::icon(fa fa-calculator)
      [ln S 凹函数]
        漂移项减小
        mu - 0.5*sigma^2
      [1/S 凸函数]
        漂移项增加
        sigma^2 - mu
      [本质区别]
        二阶导的正负
        决定了漂移项的修正方向

    (乘法法则<br/>Product Rule)
      ::icon(fa fa-times)
      [固定骨架]
        d(XY) = XdY + YdX + dXdY
      [可变零件 dXdY]
        同源噪声: sigma^2 dt
        独立噪声: 0
        含确定性项: 0

    (金融含义<br/>Finance)
      ::icon(fa fa-money)
      [分离漂移项]
        Isolate Drift
        如果 Drift=0 则为鞅
      [参数来源]
        mu 来自股票定义 dS
        r 来自债券定义 dB
      [例子 S/B]
        结合了乘法法则
        和模型假设
