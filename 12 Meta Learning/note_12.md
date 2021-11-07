# Meta Learning : Learn to learn

<img src="note_12.assets/image-20210930095507448.png" alt="image-20210930095507448" style="zoom:50%;" />

## (1) Three steps

<img src="note_12.assets/image-20210930095612193.png" alt="image-20210930095612193" style="zoom:50%;" />

<img src="note_12.assets/image-20210930095741177.png" alt="image-20210930095741177" style="zoom:50%;" />

### Machine Learning

<img src="note_12.assets/image-20210930095802692.png" alt="image-20210930095802692" style="zoom:50%;" />

- Step 1

<img src="note_12.assets/image-20210930100620257.png" alt="image-20210930100620257" style="zoom:50%;" />

- Step 2
  - <img src="note_12.assets/image-20210930101026946.png" alt="image-20210930101026946" style="zoom:50%;" />

- Step 3
  - <img src="note_12.assets/image-20210930101157245.png" alt="image-20210930101157245" style="zoom:50%;" />
  - 

### Meta Learning

<img src="note_12.assets/image-20210930101335958.png" alt="image-20210930101335958" style="zoom:50%;" />

- Meta-learning :  **Learn an optimized algorithm **  

  -  *Step 1:*

    - <img src="note_12.assets/image-20210930101737162.png" alt="image-20210930101737162" style="zoom: 50%;" />

  - *Step 2:*

    - <img src="note_12.assets/image-20210930101911919.png" alt="image-20210930101911919" style="zoom:50%;" />
    - Define $L({\color{blue}\phi})$​​​​ ​​ 
    - <img src="note_12.assets/image-20210930102214844.png" alt="image-20210930102214844" style="zoom:50%;" />\
    - <img src="note_12.assets/image-20210930102330633.png" alt="image-20210930102330633" style="zoom:50%;" />
    - <img src="note_12.assets/image-20210930102508734.png" alt="image-20210930102508734" style="zoom:50%;" />
    - Total loss: $L(\phi)=\sum_{n=1}^{N}l^n$​ 

    

<center class="half">
    <img src="note_12.assets/image-20210930102723840.png" alt="image-20210930102723840" style="zoom:30%;" /><img src="note_12.assets/image-20210930102748587.png" alt="image-20210930102748587" style="zoom:30%;" />
</center>

- 
  - *Step 3*	
    - <img src="note_12.assets/image-20210930103031826.png" alt="image-20210930103031826" style="zoom:50%;" />
    - <img src="note_12.assets/image-20210930103257478.png" alt="image-20210930103257478" style="zoom:50%;" />
    - Few-shot learning
    - 

### ML && Meta

- Goal

<img src="note_12.assets/image-20210930103957621.png" alt="image-20210930103957621" style="zoom:50%;" />

- Training Data

<img src="note_12.assets/image-20210930104104555.png" alt="image-20210930104104555" style="zoom: 50%;" />

- Task Training

<img src="note_12.assets/image-20210930104245257.png" alt="image-20210930104245257" style="zoom:50%;" />

- <img src="note_12.assets/image-20210930104547222.png" alt="image-20210930104547222" style="zoom: 50%;" />
- Loss
  - <img src="note_12.assets/image-20210930104658359.png" alt="image-20210930104658359" style="zoom:50%;" />
  - <img src="note_12.assets/image-20210930104843097.png" alt="image-20210930104843097" style="zoom:50%;" />
- The Same
- <img src="note_12.assets/image-20210930104904963.png" alt="image-20210930104904963" style="zoom:50%;" />
  - Also need hyperparameter ... ...
-  

## (2) Everything can Meta

### What is Learnable in a learning algorithm ?

<img src="note_12.assets/image-20210930155725562.png" alt="image-20210930155725562" style="zoom:50%;" />

<img src="note_12.assets/image-20210930155820789.png" alt="image-20210930155820789" style="zoom:50%;" />

- Training MAML

<img src="note_12.assets/image-20210930160331263.png" alt="image-20210930160331263" style="zoom:50%;" />

- MAML
  - Self-supervised Learning
  - <img src="note_12.assets/image-20210930160606796.png" alt="image-20210930160606796" style="zoom:50%;" />
  - <img src="note_12.assets/image-20210930160723350.png" alt="image-20210930160723350" style="zoom:50%;" />
  - **Multi-task Learning** 
  - <img src="note_12.assets/image-20210930160808471.png" alt="image-20210930160808471" style="zoom:50%;" />
  - Isn't it domain adaption / transfer learning ?
  - <img src="note_12.assets/image-20210930161155594.png" alt="image-20210930161155594" style="zoom:50%;" />
    - <img src="note_12.assets/image-20210930161208140.png" alt="image-20210930161208140" style="zoom:50%;" />

### Optimizer

<img src="note_12.assets/image-20210930161250950.png" alt="image-20210930161250950" style="zoom:50%;" />

<img src="note_12.assets/image-20210930161326664.png" alt="image-20210930161326664" style="zoom:50%;" />

- LSTM -> Optimize

### Network Architecture Search (NAS)

<img src="note_12.assets/image-20210930161508990.png" alt="image-20210930161508990" style="zoom:50%;" />

<img src="note_12.assets/image-20210930161614935.png" alt="image-20210930161614935" style="zoom:50%;" />
$$
\hat{\phi}=\arg \underset{\phi}{\min} L(\phi)\\
BUT: \nabla_\phi L(\phi)=?
$$
<img src="note_12.assets/image-20210930161930039.png" alt="image-20210930161930039" style="zoom:50%;" />

<img src="note_12.assets/image-20210930162005054.png" alt="image-20210930162005054" style="zoom:50%;" />

<img src="note_12.assets/image-20210930162027309.png" alt="image-20210930162027309" style="zoom:50%;" />

- DARTS: Can analyze Gradient
- Data Augmetation

<img src="note_12.assets/image-20210930162121771.png" alt="image-20210930162121771" style="zoom:50%;" />



<img src="note_12.assets/image-20210930162152859.png" alt="image-20210930162152859" style="zoom:50%;" />

- Sample Reweighting

<img src="note_12.assets/image-20210930162253365.png" alt="image-20210930162253365" style="zoom:50%;" />

- Beyond Gradient Decent

<img src="note_12.assets/image-20210930162422372.png" alt="image-20210930162422372" style="zoom:50%;" />

- Not divided Training data and Testing data

<img src="note_12.assets/image-20210930162512087.png" alt="image-20210930162512087" style="zoom:50%;" />

### Application

- Few-shot Image Classification
  - N-ways K-shot
  - <img src="note_12.assets/image-20210930162739339.png" alt="image-20210930162739339" style="zoom:50%;" />
  - <img src="note_12.assets/image-20210930162810323.png" alt="image-20210930162810323" style="zoom:50%;" />
  - <img src="note_12.assets/image-20210930163124164.png" alt="image-20210930163124164" style="zoom:50%;" />
  - <img src="note_12.assets/image-20210930163157466.png" alt="image-20210930163157466" style="zoom:50%;" />
  - 



















































































