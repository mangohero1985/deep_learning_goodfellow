* What is constrained optimization
https://www.khanacademy.org/math/multivariable-calculus/applications-of-multivariable-derivatives/lagrange-multipliers-and-constrained-optimization/v/constrained-optimization-introduction
* Solution
    * gradient descent for constrained optimization
        * tangent plane: 
         * 理解成切面：对于输入的X点对应的Y输出的graph上的切面。
         * 有约束的问题也可以使用梯度下降去优化
         * 或者使用line search的方法进行优化（二者的区别是 梯度下降固定步长寻找梯度方向。线性搜索是已知梯度的情况下寻找最优步长）
    * transform a constrained problem to unconstrained problem, then transform back after get solution from unconstrained problem. 这种方法需要非常精巧的设计，不是所有情况都能够找到合适的解决方案。
    * KKT: general solution for constrained optimization.
      * Generalized Lagrangian/ generalized Lagrange function
