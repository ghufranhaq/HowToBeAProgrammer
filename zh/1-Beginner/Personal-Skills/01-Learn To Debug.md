# 学会Debug

调试（Debug）是作为一个程序员的基石。调试这个词第一个含义即是移除错误，但真正有意义的含义是，通过检查来观察程序的运行。一个不能调试的程序员等同于瞎子。

那些认为设计、分析、复杂的理论或其他东西是更基本的东西的理想主义者们不是现实的程序员。现实的程序员不会活在理想的世界里。即使你是完美的，你周围也会有，并且也需要与主要的软件公司或组织，比如GNU，或者与你的同事，写的代码打交道。这里面大部分的代码以及它们的文档是不完美的。如果没有获得代码的执行过程可见性的能力，最轻微的颠簸都会把你永远地抛出去。通常这种可见性只能从实验获得，也就是，调试。

调试是一件与程序运行相关的事情，而非与程序本身相关。你从主要的软件公司购买一些产品，你通常不会看到（产品背后的）程序本身。但代码不遵循文档这样的情况（让你整台机器崩掉是一个常见又特殊的例子）或者文档没有说明的情况仍然会出现，不可避免的，这意味着你做的一些假设并不对，或者一些你没有预料到的情况发生了。有时候，神奇的修改源代码的技巧可能会生效。当它无效时，你必须调试了。

为了获得一个程序执行的可见性，你必须能够执行代码并且从这个过程中观察到什么。有时候这是可见的，比如一些正在呈现在屏幕上的东西，或者两个事件之间的延迟。在许多其他的案例中，它与一些不一定可见的东西相关，比如代码中一些变量的状态，当前真正在执行的代码行，或者是否一些断言持有了一个复杂的数据结构。这些隐藏的细节必须被显露出来。


通常的（一些）观察一个正在执行的程序的内部的方法可以如下分类：

- 使用一个调试工具；
- Printlining[(戳这里看释义)](../../4-Glossary.md) - 对程序做一个临时的修改，通常是加一些行去打印一些信息;
- 日志 - 用日志的形式为在程序的运行中创建一个永久的视窗。

当调试工具稳定可用时，它们是非常美妙的，但[Printlining](../../4-Glossary.md)和写日志是更加重要的。调试工具通常落后于编程语言的发展，所以在任何时间点它们都可能是无效的。另外，调试工具可能轻微改变程序实际执行的方式。最后，调试有许多种，比如检查一个断言和一个巨大的数据结构，这需要写代码并改变程序的运行。当调试工具可用时，知道怎样使用调试工具是好的，但学会使用其他两种方式是至关重要的。

当需要修改代码时，一些初学者会害怕调试。这是可以理解的，这有点像探索型外科手术。但你需要学会打破代码，让它跳起来，你需要学会在它上面做实验，并且需要知道你临时对它做的任何事情都不会使它变得更糟。如果你感受到了这份恐惧，找一位导师 - （否则）在许多人面对这种恐惧的脆弱的开始时刻，我们会因此失去很多优秀的程序员。

Next [如何通过分离问题空间来Debug](02-How to Debug by Splitting the Problem Space.md)