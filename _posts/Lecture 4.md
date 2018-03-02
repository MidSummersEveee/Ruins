# Philosophies of UCS, Greedy, and A*
## UCS, 贪心和A*的人生哲学
#### 1. UCS 统一开销算法
UCS中的核心概念是“开销”。在用General 的Tree Search中，我们根据路径累计cost去选择扩展哪个节点。必如，选定某点为起点，根据候选函数Successor Function，我们发现有A、B两个可扩展节点，且扩展到两个位置的动作开销Action Cost分别为1，3，起点处Cost为0，因此两支的路径累积开销分别为1、3.
