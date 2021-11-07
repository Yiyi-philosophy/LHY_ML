

## Convolutoinal Neural Network (CNN)

- input 100*100
- output : one hot vector $\hat{y}$

- dimention of  $\hat{y}$ decide how many kinds model can classify

  <img src="note_03.assets/image-20210709092819918.png" alt="image-20210709092819918" style="zoom: 33%;" />

- Image in computer:
  - ```tensor```
  - RGB : 3 channel

<img src="note_03.assets/image-20210709093157070.png" alt="image-20210709093157070" style="zoom:33%;" />

<img src="note_03.assets/image-20210709093326943.png" alt="image-20210709093326943" style="zoom:33%;" />

- **Too many parameters=>Overfitting**

- ### consider the image's feature, there's no need to "fully connected"

  - #### Observation1

    - Identifying some critical patterns (like human)
    - Some pattern are much smaller => **no need to see whole image**
    - <img src="note_03.assets/image-20210709094616308.png" alt="image-20210709094616308" style="zoom:33%;" />

  - #### Simplification1

    - receptive field (感受野)
    - <img src="note_03.assets/image-20210709094911738.png" alt="image-20210709094911738" style="zoom:25%;" />
    - <img src="note_03.assets/image-20210709095050161.png" alt="image-20210709095050161" style="zoom:25%;" />
      - there appears **Same receptive field, Overlapped receptive field** 
      - different sizes of receptive field, just in some channels  ...
    - Simplification1--**Tipical Setting**
      - all channels, kernal size (3*3) 
      - each receptive field has **a set of neurons**
      - stride=1, 2
      - overlap--padding (补值)
      - <img src="note_03.assets/image-20210709100614085.png" alt="image-20210709100614085" style="zoom:25%;" />

  - #### Observation2

    - The same patterns appear in different regions
    - <img src="note_03.assets/image-20210709100842481.png" alt="image-20210709100842481" style="zoom:25%;" />
    - sharing parameter
    - <img src="note_03.assets/image-20210709100916089.png" alt="image-20210709100916089" style="zoom:33%;" />
    - <img src="note_03.assets/image-20210709101122238.png" alt="image-20210709101122238" style="zoom:25%;" />
    - Two receptive field would sharing parameters 
    - Simplification 2--Typical Setting
    - <img src="note_03.assets/image-20210709104506093.png" alt="image-20210709104506093" style="zoom:25%;" />
    - <img src="note_03.assets/image-20210709105951033.png" alt="image-20210709105951033" style="zoom:33%;" />

- #### Another narrative way

- <img src="note_03.assets/image-20210709110226397.png" alt="image-20210709110226397" style="zoom:33%;" />

- <img src="note_03.assets/image-20210709110440952.png" alt="image-20210709110440952" style="zoom:33%;" />

- the parameters in Filters are learned by Gradient decent

- <img src="note_03.assets/image-20210709110713110.png" alt="image-20210709110713110" style="zoom:33%;" />

- <img src="note_03.assets/image-20210709110820087.png" alt="image-20210709110820087" style="zoom:33%;" />

- <img src="note_03.assets/image-20210709111018540.png" alt="image-20210709111018540" style="zoom:33%;" />

- 3 channels image => 64fliter convolution 1 => 64 channels image

- **each convolution-> a compress (压缩) of information in image**

- <img src="note_03.assets/image-20210709111620146.png" alt="image-20210709111620146" style="zoom:33%;" />

- <img src="note_03.assets/image-20210709111718710.png" alt="image-20210709111718710" style="zoom:50%;" />



- Observation3
  - <img src="note_03.assets/image-20210709111825757.png" alt="image-20210709111825757" style="zoom:33%;" />
  - Pooling
  - <img src="note_03.assets/image-20210709111958094.png" alt="image-20210709111958094" style="zoom:33%;" />
  - <img src="note_03.assets/image-20210709112103508.png" alt="image-20210709112103508" style="zoom:33%;" />
  - may no pooling
  - <img src="note_03.assets/image-20210709112227673.png" alt="image-20210709112227673" style="zoom:33%;" />
  - 

---

### Self-attention (1)

<img src="note_03.assets/image-20210715083045415.png" alt="image-20210715083045415" style="zoom: 50%;" />

<img src="note_03.assets/image-20210715083248037.png" alt="image-20210715083248037" style="zoom:50%;" />

- One-hot Encoding
  - No relatoin
- Word Embedding
  - cluster (a group)

<img src="note_03.assets/image-20210715083622899.png" alt="image-20210715083622899" style="zoom:50%;" />



- rolling window

  <img src="note_03.assets/image-20210715083741325.png" alt="image-20210715083741325" style="zoom:33%;" />

  <img src="note_03.assets/image-20210715083811417.png" alt="image-20210715083811417" style="zoom:33%;" />

  #### Output

<img src="note_03.assets/image-20210715084247781.png" alt="image-20210715084247781" style="zoom:50%;" />

- POS tagging (part-of-speech label )

<img src="note_03.assets/image-20210715084451823.png" alt="image-20210715084451823" style="zoom:50%;" />

<img src="note_03.assets/image-20210715085011538.png" alt="image-20210715085011538" style="zoom:50%;" />

- **Output**

  - Each vector has a label *(focus of)*
  - The whole sequence has a label
  - Model decides the number of labels itself (**seq2seq**)

- Sequence labeling (Each vector has a label)

  - <img src="note_03.assets/image-20210715085521042.png" alt="image-20210715085521042" style="zoom:50%;" />

  - Consider the context ?

  - <img src="note_03.assets/image-20210715085656454.png" alt="image-20210715085656454" style="zoom:50%;" />

  - Consider the Sequence ?

    - ~~a window cover the whole sequence~~

    - **Self - attention**

    - <img src="note_03.assets/image-20210715090015247.png" alt="image-20210715090015247" style="zoom:50%;" />

    - How self attention consider the whole sequence ?

    - <img src="note_03.assets/image-20210715090458780.png" alt="image-20210715090458780" style="zoom:50%;" />

    - <img src="note_03.assets/image-20210715090543143.png" alt="image-20210715090543143" style="zoom:50%;" />

    - > Attention is all you need:https://arxiv.org/abs/1706.03762

      <img src="note_03.assets/image-20210715091245089.png" alt="image-20210715091245089" style="zoom:50%;" />

  - Self attention principle

    <img src="note_03.assets/image-20210715091525250.png" alt="image-20210715091525250" style="zoom:50%;" />

  - <img src="note_03.assets/image-20210715091913717.png" alt="image-20210715091913717" style="zoom:50%;" />

  - Find the relevant vectors in a sequence 

    - Dot-product   $\alpha=\pmb{q\cdot k}$
    - Additive

  - <img src="note_03.assets/image-20210715092746726.png" alt="image-20210715092746726" style="zoom:50%;" />

  - $$
    \alpha_{i,j}=W^q\pmb{a^i}\cdot W^k\pmb{a^j} \\
    \alpha_{i,j}'=\frac{e^{\alpha_{i,j}}}{\sum_j e^{\alpha_{i,j}}}
    $$

  - <img src="note_03.assets/image-20210715093321494.png" alt="image-20210715093321494" style="zoom:50%;" />

  - $$
    \pmb{b^i}=\sum_{j} \alpha_{i,j}' \pmb{v^i}\\
    \pmb{v^i}= W^v \pmb{a^i}
    $$

  - All in one :

  - $$
    Attention:
    \left\{\begin{matrix}
     \pmb{b^i}=\sum_{j} \alpha_{i,j}' \pmb{v^i}\\
    \pmb{v^i}= W^v \pmb{a^i} \\
    \alpha_{i,j}'=\frac{e^{\alpha_{i,j}}}{\sum_j e^{\alpha_{i,j}}} \\
    \alpha_{i,j}=W^q\pmb{a^i}\cdot W^k\pmb{a^j} \\
    
    \end{matrix}\right.
    $$

  - 

  - <img src="note_03.assets/image-20210715101711029.png" alt="image-20210715101711029" style="zoom:50%;" />
  
  - 
  
  - $$
    Matrix\left\{\begin{matrix}Q=W^q I &(\pmb{q^i}=W^q\pmb{a^i})\\K=W^k I &(\pmb{k^i}=W^k\pmb{a^i})\\V=W^v I &(\pmb{v^i}=W^v\pmb{a^i})\end{matrix}\right.
    $$
    
  - 
  
  - <img src="note_03.assets/image-20210715102046787.png" alt="image-20210715102046787" style="zoom:50%;" />
  
  - 
  - $A=K^T Q,\ A'=softmax(A)$
  - <img src="note_03.assets/image-20210715102200830.png" alt="image-20210715102200830" style="zoom:67%;" />
  - <img src="note_03.assets/image-20210715102355187.png" alt="image-20210715102355187" style="zoom:50%;" />
  - $O=VA'$
  
  - <img src="note_03.assets/image-20210715102517039.png" alt="image-20210715102517039" style="zoom:50%;" />
  
  - $$
    \text{Self-attention on Matrix}\left\{\begin{matrix}Q=W^q I &(\pmb{q^i}=W^q\pmb{a^i})\\K=W^k I &(\pmb{k^i}=W^k\pmb{a^i})\\
    V=W^v I &(\pmb{v^i}=W^v\pmb{a^i})\\
    A=K^T Q,\ A'=softmax(A)\\
    O=VA'
    \end{matrix}\right.
    $$
  
  - 
  
  - **Multi-head Self-attention**
  
  - <img src="note_03.assets/image-20210715103210459.png" alt="image-20210715103210459" style="zoom:50%;" />
  
  - <img src="note_03.assets/image-20210715103308931.png" alt="image-20210715103308931" style="zoom:67%;" />
  
  - **Positional Encoding**
  
  - <img src="note_03.assets/image-20210715103608060.png" alt="image-20210715103608060" style="zoom:67%;" />
  
  - <img src="note_03.assets/image-20210715104016344.png" alt="image-20210715104016344" style="zoom:67%;" />
  
  - > 2003.09229
  
  - Self-attention for speech
  
  - <img src="note_03.assets/image-20210715104238678.png" alt="image-20210715104238678" style="zoom: 67%;" />
  
  - > Truncated Self-attention:1910.12977
  
  - Self-attention for Image
  
  - ![image-20210715104821944](note_03.assets/image-20210715104821944.png)
  
  - **Set of vector**-->Self attention
  
  - <img src="note_03.assets/image-20210715104910932.png" alt="image-20210715104910932" style="zoom:67%;" />
  
  - > 1805.08318
    >
    > 2005.12872
  
  - Self-attention v.s. CNN
  
    - Self-attention consider the whole Image's information 
  
    - CNN only consider the receptive fields' information
  
    - **It likes Self-attention learn to find  a "receptive field"**
  
    - <img src="note_03.assets/image-20210715105439340.png" alt="image-20210715105439340" style="zoom:67%;" />
  
    - > 1911.03584
      >
      > 2010.11929
  
    - <img src="note_03.assets/image-20210715105521617.png" alt="image-20210715105521617" style="zoom:67%;" />
  
    - <img src="note_03.assets/image-20210715105730685.png" alt="image-20210715105730685" style="zoom:67%;" />
  
    - On overfitting
  
      - CNN is "tight", it's model is simply
      - Self-attention is "loose", it's model is complex
  
  - <img src="note_03.assets/image-20210715110049983.png" alt="image-20210715110049983" style="zoom:67%;" />
  
    - RNN->with **Positional Encoding** in itself
  
    - Self-attention ->add **Positional Encoding**
  
    - <img src="note_03.assets/image-20210715110411296.png" alt="image-20210715110411296" style="zoom:67%;" />
  
    - Easy to parallel 
  
    - > 2006.16236
  
  - <img src="note_03.assets/image-20210715110744943.png" alt="image-20210715110744943" style="zoom:67%;" />
  
  - > GNN Vedio
  
  - <img src="note_03.assets/image-20210715110900353.png" alt="image-20210715110900353" style="zoom:67%;" />
  
  - > Reduce the calculating of self attention 
    >
    > 2011.04006, 
    >
    > 2009.06732
  
  - 

