# Life Long Learning

## (1) 

<img src="note_10.assets/image-20210926211939627.png" alt="image-20210926211939627" style="zoom:50%;" />

<img src="note_10.assets/image-20210927194001496.png" alt="image-20210927194001496" style="zoom:50%;" />

### LLL

- Self learning

<img src="note_10.assets/image-20210927194055523.png" alt="image-20210927194055523" style="zoom:50%;" />



- **Example 1**
  - Learn task 2 in the base of task 1
  - <img src="note_10.assets/image-20210927194352629.png" style="zoom:50%;" />
  - **Forget**
  - But actually the network has **enough capacity** to learn both tasks.
    - <img src="note_10.assets/image-20210927194513166.png" alt="image-20210927194513166" style="zoom:50%;" />
- **Example 2**
  - <img src="note_10.assets/image-20210927200122575.png" alt="image-20210927200122575" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210927200036535.png" alt="image-20210927200036535" style="zoom:50%;" />
  - Forget ?   No !
  - <img src="note_10.assets/image-20210927200335440.png" alt="image-20210927200335440" style="zoom:50%;" />

### Catastrophic Forgetting

- Multi-task training -> ==Upper bound==
  - Storage issue && Computation
  - <img src="note_10.assets/image-20210927200830739.png" alt="image-20210927200830739" style="zoom:50%;" />
- Train a model for each task
  - <img src="note_10.assets/image-20210927201032821.png" alt="image-20210927201032821" style="zoom:50%;" />
    - We can't store all the model.
    - Knowledge can't transfer across different tasks.
- Life-Long && Transfer
  - <img src="note_10.assets/image-20210927201257471.png" alt="image-20210927201257471" style="zoom:50%;" />
  - More emphasize on **all tasks**

- Evaluation

  - <img src="note_10.assets/image-20210927201501323.png" alt="image-20210927201501323" style="zoom:50%;" />

  - <img src="note_10.assets/image-20210927201822454.png" alt="image-20210927201822454" style="zoom:50%;" />

  - <img src="note_10.assets/image-20210927201910706.png" alt="image-20210927201910706" style="zoom:50%;" />

  - $$
    R_{i,j}:\ \text{after trianing task i, perform on task j}\\
    \text{If}\ \ i>j, \ \text{then the task i's experience was} \pmb{forget}; \\
    \ \ \ \ \ \ \ \ \  \text{else} \ i<j,\ \text{We can transfer the skillof task i to task j}\\
    \\
    BT: \frac{1}{T-1}\sum_{i=1}^{T-1}(R_{T,i}-R_{i,i})
    $$

  - <img src="note_10.assets/image-20210927202650462.png" alt="image-20210927202650462" style="zoom:50%;" />

  - $$
    FT: \frac{1}{T-1}\sum_{i=2}^{T}(R_{i-1,i}\ -\ R_{0,i})
    $$

### Resarch Directions



#### Selective Synaptic Plasticity

<img src="note_10.assets/image-20210927203415313.png" alt="image-20210927203415313" style="zoom:50%;" />

- Why catastrophic fogotting happened ?
  - <img src="note_10.assets/image-20210927205209712.png" alt="image-20210927205209712" style="zoom:50%;" />
- practise
  - <img src="note_10.assets/image-20210927205452697.png" alt="image-20210927205452697" style="zoom:50%;" />
  - $L'(\theta)=L(\theta)+\lambda \sum_{i}b_i\left(\theta_i -\theta_i^b \right)^2 $​ 
  - <img src="note_10.assets/image-20210927205809507.png" alt="image-20210927205809507" style="zoom:50%;" />
- How to decide correct $b_i$​ ?
  - <img src="note_10.assets/image-20210927210115669.png" alt="image-20210927210115669" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210927210210483.png" alt="image-20210927210210483" style="zoom:50%;" />
    - **Limited parameters' direction** 
  - ​	 <img src="note_10.assets/image-20210927210540815.png" alt="image-20210927210540815" style="zoom:50%;" />
    - <img src="note_10.assets/image-20210927210602025.png" alt="image-20210927210602025" style="zoom:50%;" />

==Different task order affect the perfomer== 

- GEM
  - <img src="note_10.assets/image-20210927211116364.png" alt="image-20210927211116364" style="zoom:50%;" />
  - It's **accepted** if GEM **don't** save much data of previous tasks.



#### Additional Neural Resource Allocation

- Progressive NN
- <img src="note_10.assets/image-20210927211448825.png" alt="image-20210927211448825" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210927211726181.png" alt="image-20210927211726181" style="zoom:50%;" />

- 



#### Memory Reply

<img src="note_10.assets/image-20210927211849108.png" style="zoom:50%;" />

- Generating Data
- <img src="note_10.assets/image-20210927211953980.png" alt="image-20210927211953980" style="zoom:50%;" />
- 

#### Curruculum Learning

<img src="note_10.assets/image-20210927212133257.png" alt="image-20210927212133257" style="zoom:50%;" />

  

## (2) Network Compression

### Smaller Model

<img src="note_10.assets/image-20210928152842450.png" alt="image-20210928152842450" style="zoom:50%;" />

<img src="note_10.assets/image-20210928152925415.png" alt="image-20210928152925415" style="zoom: 50%;" />

Only on soft-ware solution.

### Network Pruning





<img src="note_10.assets/image-20210928153117803.png" alt="image-20210928153117803" style="zoom:50%;" />

<img src="note_10.assets/image-20210928153240800.png" alt="image-20210928153240800" style="zoom:50%;" />

-  Human brain : less-> more->medium

<img src="note_10.assets/image-20210928161413677.png" alt="image-20210928161413677" style="zoom:50%;" />

- Practical issue
  - <img src="note_10.assets/image-20210928161727808.png" alt="image-20210928161727808" style="zoom:50%;" />
  - hard to speed up
  - <img src="note_10.assets/image-20210928163152551.png" alt="image-20210928163152551" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210928163210711.png" alt="image-20210928163210711" style="zoom:50%;" />
- Train small network -> Enlarge then 
- Why not train a small network?
  - <img src="note_10.assets/image-20210928163957722.png" alt="image-20210928163957722" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210928164155725.png" alt="image-20210928164155725" style="zoom:50%;" />
  - Lottery Ticket Hypothesis
  - <img src="note_10.assets/image-20210928164341105.png" alt="image-20210928164341105" style="zoom:50%;" />

**"我只是把困在石头里的大卫释放出来了"** 

- <img src="note_10.assets/image-20210928165045279.png" alt="image-20210928165045279" style="zoom:50%;" />

- <img src="note_10.assets/image-20210928165244620.png" alt="image-20210928165244620" style="zoom:50%;" />



### Knowledge Distillation

- Student Network study from teacher

  - <img src="note_10.assets/image-20210928183713691.png" alt="image-20210928183713691" style="zoom:50%;" />
    - It can learn some classifies never seen.
    - <img src="note_10.assets/image-20210928183958405.png" alt="image-20210928183958405" style="zoom:50%;" />

  -  **Softmax - trick** 
  - Train from each network
  - <img src="note_10.assets/image-20210928184146775.png" alt="image-20210928184146775" style="zoom:50%;" />
  - 

### Parameter Quantization

- Less accuracy
- Weight clustering
- Huffman Encoding
- <img src="note_10.assets/image-20210928185032458.png" alt="image-20210928185032458" style="zoom:50%;" />
-  Binary Weight
  - <img src="note_10.assets/image-20210928185114042.png" alt="image-20210928185114042" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210928185206220.png" alt="image-20210928185206220" style="zoom:50%;" />
    - More limit - > Less overfitting
  - 

### Architecture Design

- Depthwise Separable Convolution
  - <img src="note_10.assets/image-20210928190729322.png" alt="image-20210928190729322" style="zoom:50%;" />

<center class="half">
    <img src="note_10.assets/image-20210928190933347.png" alt="image-20210928190933347" style="zoom:41%;" /><img src="note_10.assets/image-20210928191022217.png" alt="image-20210928191022217" style="zoom:40%;" />
</center>
<center class="half">
    <img src="note_10.assets/image-20210928191526912.png" alt="image-20210928191526912" style="zoom:33%;" /><img src="note_10.assets/image-20210928191456179.png" alt="image-20210928191456179" style="zoom:33%;" />
</center>

- Compress

<img src="note_10.assets/image-20210928191941562.png" alt="image-20210928191941562" style="zoom:50%;" />

- Low rank approximation
  - <img src="note_10.assets/image-20210928192234667.png" alt="image-20210928192234667" style="zoom:50%;" />
  - $W=U\times V$​​ but $Rank(W)<k$​​  
  - <img src="note_10.assets/image-20210928192711497.png" alt="image-20210928192711497" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210928192722357.png" alt="image-20210928192722357" style="zoom:50%;" />
  - 

### Dynamic Computation

<img src="note_10.assets/image-20210928213635561.png" alt="image-20210928213635561" style="zoom:50%;" />

- Auto-controled Layer : Depth & Width
  - <img src="note_10.assets/image-20210928214249138.png" alt="image-20210928214249138" style="zoom:50%;" />
  - <img src="note_10.assets/image-20210928214355556.png" alt="image-20210928214355556" style="zoom:50%;" />
- <img src="note_10.assets/image-20210928214521741.png" alt="image-20210928214521741" style="zoom:50%;" />
  - 









