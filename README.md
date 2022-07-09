# Mathematical-modeling
# 如何系统备战数学建模

---

### 1. 数学建模需要的学科知识

- 高等代数：微积分、函数、解析几何
- 概率论与数理统计

- 推荐用书：
《数学建模》姜启源（基础方法+思想）
《数学建模算法与应用》司守奎（操作）

### 2. 如何学习数学模型————三步阅读法

- 模型名字
- 模型类型+能解决哪类特征的问题
- 模型的操作步骤+实现
- ~~模型原理~~

### 3. 如何读论文
    
    比方说，2012年A题葡萄酒评价模型，有篇文章用了回归分析和灰色关联方法对葡萄酒进行了评级，然后比较二者的结果，得出灰色关联的方法更加能够反映理化成分对葡萄酒质量的影响的结论。这就是论文表面上给我们呈现的样子，但是我们就可以多想想以下几个问题：
    
    1．葡萄酒的理化成分数据是怎么一个结构？作者用了哪些数据处理方法，缺失、异常数据怎么处理的？他为什么要这么处理？如果以后遇到类似的问题，数据分析的时候，有没有好的步骤？
    
    简要来说，这道题的理化指标是下个多变量多对象的二维数据表，存在异常数据用spss验证数据功能予以去除，缺失值用插值方法补充，然后用主成分分析法进行了降维，目的是能够减小变量个数。这样一来，数据分析的一套流程就比较清楚了。
    
    2．他为什么选取了回归分析和灰色关联方法来建模？遇到这类评价某事物的问题，共有哪些建模方法？分别能够在什么条件下使用？各有什么特点？
    
    回归分析能够忽略问题机理，只从数据上分析出变量之间的相关关系，进而得出结论；而灰色关联方法能够在机理没有完全摸清的情况下，部分挖掘变量间更深层次的联系，更能够准确地评价葡萄酒的好坏。在评价类问题上，我们还有TOPSIS方法，模糊综合评判等等，各有各的特点和优势，处理的问题类型有较小的差别，大家可以自行学习。
    
    3. 在做模型检验时，他是用什么标准来得到判断灰色关联方法比回归分析要好的结论的？他怎么想法到这一点的？我遇到这种比较时能不能想到这一点上？
    
    该文章直接用了评价误差率指标来判别评价好坏，并且从模型的假设、简化等建立过程中分析出灰色关联方法更加优越的结论，于是我们在对两个模型进行优劣比较的时候，也应该从结果和建立过程分析，进而比较优劣。

### 4. 数学建模赛题常见类别

- **优化类模型**
- 评价类模型
- 预测类模型

### 5. 常见问题

```graphLR
    A[实际问题] --> B[数学模型]
    B --> C[数学求解]
    C --> D[问题回答]
```
    
   
    1.实际问题：题目到底问我们什么？需要解决哪些问题？已知条件是什么？等等
    2.数学模型：需要建立或选择哪些模型来求解题目中的问题？
    3.数学求解：针对已经建好的模型应该采用哪些方法或软件求解
    4.问题回答：对求解结果应该进行怎样的分析和描述才能与问题交相呼应
大家可以想一下自己的问题到底是从哪里来的，无非出自于这四个步骤中间：
  
    1. 对一个实际问题没有思路，找不到一个模型可以解决；
    2. 知道用哪个数学模型，但是模型的建立过程遇到困难，设计不出相应的算法；
    3. 建立模型以后，发现求解有困难，找不到现成的算法或者自己不知道设计；
    4. 发现得到的结果回答问题比较奇怪，却不知问题出在哪里。

### 6. 组队与分工

- 定题+资料查找+问题一建模求解（一起讨论）
- 模型框架+问题二+问题三求解（建模员为主）
- 剩余问题求解+结果检验+论文初稿（程序员+写手）
- 摘要+反复修改全文+翻译（一起讨论）

### 7. 准备工作

- 各类常用算法的模型原理+代码+应用条件
- 硬件软件（matlab、python、word、excel、visio）
- 心态+队友
