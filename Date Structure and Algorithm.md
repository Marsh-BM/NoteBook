# Date Structure and Algorithm

 

### 赫夫曼树（Huffman Tree）

![image-20220308123505830](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220308123505830.png)

1. **路径和长度**： 在一棵树中，从一个结点往下可以到达孩子或孙子结点之间的通路，称为**路径**。通路中分支的数目为路径的长度。若规定根结点的层数为1，则从根结点到第L层节点的路径长度为L-1.
2. **结点的权以及权带路径长度**： 若将树中的结点给一个具有某种意义的数值，则这个数值称为该结点的**权**。 **结点的带权路径长度为**：从根结点到该节点之间路径的长度与该结点权的乘积。
3. **树的带权路径长度**：树的带权路径长度规定为所有叶子结点的带权路径长度之和，记为WPL（weighted path length), **权值越大的结点离根结点越近的二叉树才是最优二叉树。**
4. ![image-20220308134828525](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220308134828525.png)

#### 构建赫夫曼树的方法

![image-20220308135137875](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220308135137875.png)



