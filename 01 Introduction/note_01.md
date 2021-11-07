###  小贴士  

![](D:\02neural network\01李宏毅\Lhy_Machine_Learning-main\01 Introduction\chapter1\res\chapter1-50.png)

 大家注意一下这个不同的方块，我是用不同的颜色来表示。同样的颜色不同的方块是同一个类型的，这边的蓝色的方块，指的是学习的情景，通常学习的情景是你没有办法控制的。比如，因为我们没有data做监督学习，所以我们才做reinforcement learning。现在因为Alpha Go比较火，所以Alpha Go中用到的reinforcement learning会被认为比较潮。所以说有学生去面试，说明自己是做监督学习的，就会被质疑为什么不做reinforcement learning。那这个时候你就应该和他说，如果我今天可以监督学习，其实就不应该做reinforcement learning。reinforcement learning就是我们没有办法做监督学习的时候，我们才做reinforcement learning。红色的是指你的task，你要解的问题，你要解的这个问题随着你用的方程的不同，有regression、有classification、有structured。所以在不同的情境下，都有可能要解这个task。最后，在这些不同task里面有不同的model，用绿色的方块表示。





## 找函数

![image-20210703161716900](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703161716900.png)

![image-20210703164948999](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703164948999.png)

预测明天的youtube订阅人数：

1. gess$$f$$ :
   - **Model**: $$y=b+wx_1$$   base on domain(field) knowledge
   - $$y$$: predict number, $$x_1$$: past number(**feature**)
   - $$w,b$$ are unknown parameters (learn from data)(**weight,bias**)
   - <img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703165905755.png" alt="image-20210703165905755" style="zoom: 33%;" />
2. def $$Loss(b,w)$$ :
   - **label** : $$\hat{y}$$   ,   $$e_1=|y-\hat{y}|$$ （MAE）,  $$e'_1=(y-\hat{y})^2$$(MSE)
   - $\textbf{L}=\frac{1}{n}\sum_{1}^{n}e_i$
3. Optimization:**<u>Gradient Decent</u>**
   - find: $$w^{*}, b^{*}=\arg \min _{w, b} L$$ 

   - Pick an initial value $$w^0$$ 

   - Compute $$\left.\frac{\partial L}{\partial w}\right|_{w=w^{0}}$$ 
     - **hyperparameters** : $$\eta$$ : learning rate
     
   - Update $$w$$ itertively

     $$
     w^{i+1} \leftarrow  w^{i} -  \eta\left.\frac{\partial L}{\partial w}\right|_{w=w^{i}}
     $$

   - ##local minia & global minia



![image-20210703173055742](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703173055742.png)



![image-20210703173345240](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703173345240.png)



![image-20210703173423122](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703173423122.png)



- #### Nearly move the yesterday's data

- ### periodic

- ###  **通常一个模型的修改，来自于你对问题的理解**

![image-20210703174149388](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703174149388.png)



## <u>**Linear Model**</u>

- too simple

- <img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703193600015.png" alt="image-20210703193600015" style="zoom:33%;" />

- **Model's Bias** -->more flexible model

- <img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703193906353.png" alt="image-20210703193906353" style="zoom:33%;" />

- (Fourier)

- #### All piecewice Linear Curves= constant+sum of a set of  "blue function"

- <img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703194305327.png" alt="image-20210703194305327" style="zoom:33%;" />

- Continuous data discretization（离散化）
- <img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703194530602.png" alt="image-20210703194530602" style="zoom:33%;" />

- sigmoid function

  $$
  y=c \frac{1}{1+e^{-\left(b+w x_{1}\right)}}
  $$

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703195630331.png" alt="image-20210703195630331" style="zoom:33%;" />

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703195753168.png" alt="image-20210703195753168" style="zoom:33%;" />


$$
y=b+\sum_{i}c_i sinmoid(b_i+w_i x_1)
$$

> ### 通过sigmoid拟合出任意复杂函数

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703200120759.png" alt="image-20210703200120759" style="zoom:33%;" />
$$
y=b+\sum_{i}c_i sigmoid(b_i+\sum_{j}w_{ij}x_j)
$$


<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703200227950.png" alt="image-20210703200227950" style="zoom:33%;" />

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703200350137.png" alt="image-20210703200350137" style="zoom:33%;" />




$$
\mathbf{r}=\mathbf{b}+\mathbf{w}\cdot \mathbf{x}
$$


<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703200852072.png" alt="image-20210703200852072" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/4Tu8rqcsvhadV6M.png" alt="image-20210703200930737" style="zoom:33%;" />

$$
\left\{\begin{matrix}
 & \mathbf{y=b+c^T \cdot a\\
 a=\sigma(r)
 } 
\end{matrix}\right.
$$
<img src="https://i.loli.net/2021/07/04/SsXwA8rnPfb79m1.png" alt="image-20210703201547845" style="zoom:33%;" />


$$
\mathbf{y=} b \mathbf{+c^T \cdot \sigma(b+w \cdot x)}
$$

<img src="https://i.loli.net/2021/07/04/syTquElYPmiQxK6.png" alt="image-20210703201906090" style="zoom:33%;" />



- ### Loss

- ![image-20210703203021528](C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703203021528.png)

$$
\boldsymbol{g}=\left[\begin{array}{l}\left.\frac{\partial L}{\partial \theta_{1}}\right|_{\boldsymbol{\theta}=\boldsymbol{\theta}^{0}} \\ \frac{\partial L}{\partial \theta_{2}} |\underset{\boldsymbol{\theta}=\boldsymbol{\theta}^{0}}{\vdots}\end{array}\right]
$$



- **gradient** $=\Delta L(\mathbf{\theta^0})\ ，\ \theta^1 \leftarrow \theta^0 - \eta g$

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703204449739.png" alt="image-20210703204449739" style="zoom:33%;" />



<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703205120725.png" alt="image-20210703205120725" style="zoom:33%;" />



- Random Gradient Decent

  - 1 **epoch** = traverse each batches once ( 历元、时期)

  - HyperParamet: Learning rate, Sigmoid, Batch Size ...

  - <img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703205343505.png" alt="image-20210703205343505" style="zoom:25%;" />

  - number of epoch = number of batches

    

- **ReLU**

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703205514835.png" alt="image-20210703205514835" style="zoom:33%;" />
$$
y=b+\sum_{2i}c_i max\{0,(b_i+\sum_{j}w_{ij}x_j)\}
$$

- ​	2ReLU -> hard Sigmoid
- **Activation function**
- 

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703210027094.png" alt="image-20210703210027094" style="zoom:33%;" />

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210703210141449.png" alt="image-20210703210141449" style="zoom:33%;" />

- ### MLP

  <img src="note_01.assets\image-20210703210340597.png" alt="image-20210703210340597" style="zoom:33%;" />

  - result：
  - <img src="note_01.assets\image-20210703210438436.png" alt="image-20210703210438436" style="zoom:33%;" />

<img src="note_01.assets\image-20210703210633632.png" alt="image-20210703210633632" style="zoom:33%;" />



- Deep Learning

### We use ReLu or Sigmoid to fitting a flexible Fuction, but why it needs deeper layers instead of wider layers ?

- over fitting



### HW1：COVID-19 Cases Prediction

> [ML2021Spring-hw1 | Kaggle](https://www.kaggle.com/c/ml2021spring-hw1/submit)
>
> 

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210704101448847.png" alt="image-20210704101448847" style="zoom:33%;" />

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210704101656857.png" alt="image-20210704101656857" style="zoom:33%;" />



<img src="https://i.loli.net/2021/07/04/BfsFaYNVke7IMZd.png" alt="image-20210704101811979" style="zoom: 50%;" />



<img src="https://i.loli.net/2021/07/04/jgYyFQDUSvXARTf.png" alt="image-20210704101920366" style="zoom:50%;" />

<img src="https://i.loli.net/2021/07/04/VBhIycun6EDLf3Q.png" alt="image-20210704101959462" style="zoom:50%;" />



<img src="https://i.loli.net/2021/07/04/9XEMQTvjaSwBOVG.png" alt="image-20210704102032876" style="zoom:50%;" />

<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210704102242191.png" alt="image-20210704102242191" style="zoom:50%;" />



<img src="C:\Users\丁yiran\AppData\Roaming\Typora\typora-user-images\image-20210704102331992.png" alt="image-20210704102331992" style="zoom:50%;" />

![image-20210704102744351](https://i.loli.net/2021/07/04/buTw39LcACq6PHS.png)



<img src="https://i.loli.net/2021/07/04/cEi96UbQahjPWO3.png" alt="image-20210704103238728" style="zoom:50%;" />











