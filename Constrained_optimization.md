* What is constrained optimization
https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/lagrange-multipliers-and-constrained-optimization/v/constrained-optimization-introduction
* Solution
    * gradient descent for constrained optimization
        * tangent plane:（https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/lagrange-multipliers-and-constrained-optimization/v/lagrange-multipliers-using-tangency-to-solve-constrained-optimization） 
         * 理解成切面：对于输入的X点对应的Y输出的graph上的切面。
        * 有约束的问题也可以使用梯度下降去优化
        * 或者使用line search的方法进行优化（二者的区别是 梯度下降固定步长寻找梯度方向。线性搜索是已知梯度的情况下寻找最优步长）
    * transform a constrained problem to unconstrained problem, then transform back after get solution from unconstrained problem. 这种方法需要非常精巧的设计，不是所有情况都能够找到合适的解决方案。
    * KKT: general solution for constrained optimization.(http://www.ifp.illinois.edu/~angelia/ge330fall09_nlpkkt_l26.pdf)
      * Generalized Lagrangian/ generalized Lagrange function (广义拉格朗日)
      * Equality constrains and inequality constrains
      * Equality constrains: 拉格朗日乘数（lambda）
      * Example: dual svm optimization:
          - Primal feasibility
            - g(x)=0, h(x)<=0
          - Dual feasibility
            - alpha>=0
          - Complementary slackness
            - alpha*h(x)=0
      * 为什么要最大化constraints：https://www.quora.com/What-is-an-intuitive-explanation-of-the-KKT-conditions/answer/Balaji-Pitchai-Kannu
          - 对于不等式constraints: h(x)<=0, 所规定的constraints space, 最大可能值都是发生在最外围的边界上也就是h(x)=0的x的点。所以要选择最大化h(x).
          - 在所有边界上的点中找到，要优化目标函数L的tangent space。
      * 对于对偶问题为什么multuplier有符号限制
          - 违反的情况下就会导致最大化为无穷的情况
      * 为什么要有complementary slackness
          - 激活状态：激活状态下，constraint取到边界的值这时候h(x)为0.
          - 非激活状态：h(x)不为0，需要用alpha为0控制限制的值。
