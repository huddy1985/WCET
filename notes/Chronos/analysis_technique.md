# 分析技术

程序的 WCET 分析主要有两步—— **程序路径分析** 和 **微处理器建模**，微处理器建模捕获到增强微处理器特性对时间性能的影响，这一步通常返回的是程序控制流图中每个控制块的测评 WCET 结果。注意，基本块 B 的测评结果应该是 B 所有可能执行上下文的执行时间的一个上界。我们如何将每个基本块的 WCET 测评结果结合起来得到整个程序的 WCET 呢？这就是路径分析来完成的。通常大多 WCET 工具使用整数线性规划（ILP）方法来计算。定义 **B** 为程序的基本块集合，那么程序的 WCET 用下面的公式得到：

	maximize(ENB*CB)

<<<<<<< HEAD
这里 NB 是 ILP 的变量，代表基本块 B 执行的次数；CB 是一个常数，代表基本块 B 的 WCET 测评结果。对于 NB 的线性限制是由下面基于控制流图（CFG）来得到的等式。
=======
这里 NB 是 ILP 的变量，代表基本块 B 执行的次数；CB 是一个常数，代表基本块 B 的 WCET 测评结果。对于 NB 的线性限制是由下面基于控制流图（CFG）来得到的等式。
>>>>>>> a3d5db5ab434ce46e3c1be78ffc976f2c3bf04cd