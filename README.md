# data-structures-are-central-to-programming
[转]我是笨人——读Rob Pike的《Notes on C Programming 》（附全文链接）

Rob Pike, 是AT&T Bell Lab前Member of Technical Staff ，现在google研究操作系统，Unix先驱，UTF-8的设计人，The Unix Programming Environment 和 The Practice of Programming 的作者之一。 在《 Notes on C Programming 》中从另一个稍微不同的角度表述了 Unix 的哲学（或者说是程序局部优化6原则）:

1. 你无法断定程序会在什么地方耗费运行时间。瓶颈经常出现在想不到的地方，所以别急于胡乱找个地方改代码，除非你已经证实那儿就是瓶颈所在。
2. 估量。在你没对代码进行估量，特别是没找到最耗时的那部分之前，别去优化速度。
3. 花哨的算法在 n 很小时通常很慢，而 n 通常很小。花哨算法的常数复杂度很大。除非你确定 n 总是很大，否则不要用花哨算法（即使 n 很大，也优先考虑原则 2 ）。比如，解决常见问题时，最简单的树——二叉树（binary tree）,总是比那些复杂的树（AVL树，伸展树（splay tree）和红黑树、B-树（B-tree）,多叉树（trie））来的高效。
4. 花哨的算法比简单算法更容易出 bug 、更难实现。尽量使用简单的算法配合简单的数据结构。
只要掌握了数据结构中的四大法宝，就可以包打天下，他们是：array 、linked list 、hash table、binary tree 。这四大法宝可不是各自为战的，灵活结合才能游刃有余。比如，一个用hash table组织的symbol table，其中是一个个由字符型array构成的linked list。
5. 以数据为中心。如果已经选择了正确的数据结构并且把一切都组织得井井有条，正确的算法也就不言自明。编程的核心是数据结构，而不是算法。
6. 没有原则 6 。

Ken Thompson —— Unix 最初版本的设计者和实现者，禅宗偈语般地对 Pike 的原则4 作了强调：
拿不准就穷举

附：E文原文（节选自《Notes on C Programming 》Rob Pike， February 21, 1989 ）

E文全文地址：http://www.lysator.liu.se/c/pikestyle.html
