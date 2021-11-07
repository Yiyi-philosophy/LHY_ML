## Framework of ML

<img src="https://i.loli.net/2021/07/04/AzqeFR2jt8ifgQ7.png" alt="image-20210704111051303" style="zoom:50%;" />

<img src="https://i.loli.net/2021/07/04/ZKQLFpg4iNhSEzM.png" alt="image-20210704112124330" style="zoom: 50%;" />

- #### From testing data

1. function : $y=f_{\boldsymbol{\theta}}(\mathbf{x})$
2. Loss Fuction : $L(\pmb{\theta})$
3. Optimization : $\boldsymbol{\theta}^*= \arg \min _{\theta} L$
4. 

- #### To training data



### Genral Guide



<img src="https://i.loli.net/2021/07/04/r65xkDQReoFuNW2.png" alt="image-20210704113226949" style="zoom:50%;" />

- #### Model Bias

  - the model is too simple, so that it can't express this task.
  - all more feartures & more deep neurons
  - def the fuction set : $f\in \pmb{S}$
    - $f^*(\pmb{x}) \notin \pmb{S}$

<img src="https://i.loli.net/2021/07/04/3nrXYmtuqVwayR8.png" alt="image-20210704113750985" style="zoom:50%;" />

- ### Optimization Issue

- def the fuction set : $f\in \pmb{S}$

  - $f^*(\pmb{x}) \in \pmb{S}$ but **can't find it**
  - 

![image-20210704114743260](https://i.loli.net/2021/07/04/xiWaHXrOAKQIsle.png)



- ### But which One?

- <img src="https://i.loli.net/2021/07/04/JixymbVhGYtLunr.png" alt="image-20210704115124000" style="zoom: 40%;" />

- ~~Overfitting~~

- ~~model bias~~

- [x] **Optimization** 

  - more insight\shallower--> easy to optimize
  - 

  - ![image-20210704143508090](https://i.loli.net/2021/07/04/fnDUtuZA5HOpWka.png)

- #### Overfitting

- <img src="https://i.loli.net/2021/07/04/mhftIFJNYq87ZyP.png" alt="image-20210704143922522" style="zoom:33%;" />

- 

<img src="https://i.loli.net/2021/07/04/O5BMpKm7kzqVDLx.png" alt="image-20210704144118442" style="zoom:33%;" />

- ### Model's flexibility depends on the scale(规模) of data

  <img src="https://i.loli.net/2021/07/04/dYKlRcevuCb2jVs.png" alt="image-20210704144501599" style="zoom:33%;" />

- **data arugmentation(数据增强)**

- add limitation => **constrained model**

  <img src="https://i.loli.net/2021/07/04/4odzYxspKLfrS7C.png" alt="image-20210704144813827" style="zoom:33%;" />



<img src="https://i.loli.net/2021/07/04/qdIDiVwkS39L7cE.png" alt="image-20210704145517480" style="zoom:33%;" />

- Less parameters, sharing parameters
  - $S_{full-connecter} \supset S_{CNN}$
- Less features
- Early stopping
- Regularization
- Dropout

<img src="https://i.loli.net/2021/07/04/s91oBMRl7UKOEzW.png" alt="image-20210704145801361" style="zoom:33%;" />

- not too much
  - In **information theory** , simple model losses many informations, and complex model can't generalization more condition.

<img src="https://i.loli.net/2021/07/04/JwMHbXu5yLzjdlm.png" alt="image-20210704150222276" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/UZwBlnqNdpyTx2o.png" alt="image-20210704150409235" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/5dkyIbsjZHWlrzF.png" alt="image-20210704151016112" style="zoom:33%;" />

- K-fold cross validation
- <img src="https://i.loli.net/2021/07/04/IXRgv7zjQhFDZxu.png" alt="image-20210704151707188" style="zoom:33%;" />

- ### dismatch

- ![image-20210704152039173](https://i.loli.net/2021/07/04/SsOG9a1UKZndATl.png)

---



## When gredient is small...

## (1)Local minima and saddle point

- In optimization, how to make gradient decent better ?
- <img src="https://i.loli.net/2021/07/04/YUdQE9uAnZvzDtw.png" alt="image-20210704154659973" style="zoom:33%;" />



- 多元函数极值（Extremum of a function of several variables）的定义：

  <img src="https://i.loli.net/2021/07/05/U1oCHOVnDzJu2i9.png" alt="image-20210704165307059" style="zoom:33%;" />

  $$
  H_{ij}=\frac{\partial^2}{\partial \pmb{\theta_i}\partial \pmb{\theta_j}}L(\pmb{\theta \ '})
  $$
  
  
  
  <img src="https://i.loli.net/2021/07/05/5s3EbQJOHeZj9CI.png" alt="image-20210704164957346" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/sRJ42Kg5PwbxQ1V.png" alt="image-20210704165138570" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/ectubndVLX6liaD.png" alt="image-20210704165233838" style="zoom:33%;" />
$$
\left\{\begin{matrix}
 &  
 &  
\end{matrix}\right.
$$

- H 正定 => 特征值 >0 => 局部最小
- H 负定 => 特征值 <0 => 局部最大
- H 有正有负 => 鞍点

<img src="https://i.loli.net/2021/07/05/aAE6M1cXkso2gCH.png" alt="image-20210704170233788" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/tHErDf3x1JvmXPp.png" alt="image-20210704170504499" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/05/GYJhl3P6cwfqKpt.png" alt="image-20210704170848267" style="zoom:33%;" />

- #### 特征向量**u**指向梯度方向，

  <img src="https://i.loli.net/2021/07/05/gSA1vpWDlZzH3Qw.png" alt="image-20210704171110961" style="zoom:33%;" />

<img src="note_2.assets/image-20210704171415809.png" alt="image-20210704171415809" style="zoom: 25%;" />

<img src="note_2.assets/image-20210704171458184.png" alt="image-20210704171458184" style="zoom:25%;" />

### When you have lots of parameters, perhaps local minima is rare ?

<img src="note_2.assets/image-20210704171809548.png" alt="image-20210704171809548" style="zoom:50%;" />

- #### In the rigthest point, though, nearly 55% are positive.

- #### Thus, 45% points are negative, which means it have posibility to decrease.

  ---


### Tip for training: Batch and Momentum-

- Why batch?

  <img src="note_2.assets/image-20210704202223429.png" alt="image-20210704202223429" style="zoom: 50%;" />

- <img src="note_2.assets/image-20210704202611191.png" alt="image-20210704202611191" style="zoom:33%;" />

- 考虑平行，并行
- consider parallel 

<img src="note_2.assets/image-20210704202952587.png" alt="image-20210704202952587" style="zoom:33%;" />

<img src="note_2.assets/image-20210704203141941.png" alt="image-20210704203141941" style="zoom:33%;" />

- So the  big batch needs the less time and more "powerfull"?
- <img src="note_2.assets/image-20210704203522672.png" alt="image-20210704203522672" style="zoom:50%;" />

- Actually, smaller batch size perform better.
- <img src="note_2.assets/image-20210704203751511.png" alt="image-20210704203751511" style="zoom:50%;" />

![image-20210704203940265](note_2.assets/image-20210704203940265.png)

<img src="note_2.assets/image-20210704204106798.png" alt="image-20210704204106798" style="zoom:33%;" />

- better Minima ==> More robustness （steady）

- small batch 
- 

<img src="note_2.assets/image-20210704210224329.png" alt="image-20210704210224329" style="zoom:33%;" />

- ### Momentum

- <img src="note_2.assets/image-20210704210422633.png" alt="image-20210704210422633" style="zoom:33%;" />

<img src="note_2.assets/ITxES69pzdUPgun.png" alt="image-20210704210503132" style="zoom:33%;" />

<img src="note_2.assets/image-20210704210711127.png" alt="image-20210704210711127" style="zoom:33%;" />

<img src="note_2.assets/image-20210704210810670.png" alt="image-20210704210810670" style="zoom:33%;" />

- ####  this gradient direction depends on both this gradient and all past dirctions

<img src="note_2.assets/image-20210704211142815.png" alt="image-20210704211142815" style="zoom:33%;" />

![image-20210704211209029](note_2.assets/image-20210704211209029.png)

---

### Classification (Short Version)

<img src="note_2.assets/image-20210704212640784.png" alt="image-20210704212640784" style="zoom:33%;" />

![image-20210704212843482](note_2.assets/uAsxYcHOar1GCKX.png)







<img src="note_2.assets/image-20210704213121648.png" alt="image-20210704213121648" style="zoom:33%;" />

<img src="https://i.loli.net/2021/07/04/B4IJKP6G2gCqh93.png" alt="image-20210704213319185" style="zoom:33%;" />

- ### Softmax was binding with Cross-entropy

  ![image-20210704213852901](https://i.loli.net/2021/07/04/ESU24iLs5qZxIPz.png)

- 交叉熵：**Cross-entropy => avoid the gradient disappeared**



## Batch Normalizaton

- Changing Landcsape
- <img src="note_2.assets/image-20210705124406765.png" alt="image-20210705124406765" style="zoom:50%;" />

- Feature Nomalization

<img src="note_2.assets/image-20210705124814986.png" alt="image-20210705124814986" style="zoom:50%;" />


$$
\pmb{\tilde{x}^r} \leftarrow \frac{\pmb{x_i^r} - m_i}{\sigma_i}
$$
<img src="note_2.assets/image-20210705125634678.png" alt="image-20210705125634678" style="zoom: 67%;" />

- Feature normalization before\after sigmoid 

<img src="note_2.assets/image-20210705125836973.png" alt="image-20210705125836973" style="zoom:50%;" />

<img src="note_2.assets/image-20210705130106299.png" alt="image-20210705130106299" style="zoom:50%;" />

- In feature normalization, $\tilde{z}^1,\tilde{z}^2,\tilde{z}^3$ is connnected with $z^1$
- **In formal model, each output $a^i$ is independent; but afer normalization, it all taken into a large network.** 
  - if $\tilde{x}^1$ changed, all the output $a^1,a^2,a^3$ will change 
- In real task, this normalization is done in each **batch**, so call it **"batch normalization"**
- <img src="note_2.assets/image-20210705131132870.png" alt="image-20210705131132870" style="zoom:50%;" />

- inference == testing 
- <img src="note_2.assets/image-20210705131834275.png" alt="image-20210705131834275" style="zoom:50%;" />

<img src="note_2.assets/image-20210705132227435.png" alt="image-20210705132227435" style="zoom:50%;" />

- Internal Covariate Shift ?
- <img src="note_2.assets/image-20210705132554762.png" alt="image-20210705132554762" style="zoom:50%;" />

![image-20210705132807338](note_2.assets/image-20210705132807338.png)



