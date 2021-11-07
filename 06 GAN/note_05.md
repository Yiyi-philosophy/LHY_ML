## GAN (1)

- Network as Generator

- <img src="note_05.assets/image-20210722092900008.png" alt="image-20210722092900008" style="zoom:50%;" />
- Simply Distribution-->Complex Distribution
-  <img src="note_05.assets/image-20210722093217825.png" alt="image-20210722093217825" style="zoom:33%;" />

<center class="two">
    <img src="note_05.assets/image-20210722093551098.png" alt="image-20210722093551098" style="zoom:28%;" /><img src="note_05.assets/image-20210722094139308.png" alt="image-20210722094139308" style="zoom:30%;" />
</center>

- In formal network structure, the training data have different directions.
- For many tasks, outputs should have some **limitation**.
- Thus change the output to Distribution




- ### Why distribution?

<img src="note_05.assets/image-20210722094716114.png" alt="image-20210722094716114" style="zoom:33%;" />

- Especially for the tasks needs =="creativity"==
  - The same input has **different outputs**
  - E.g. Drawing, Chatbot
  - 

### Generative Adversarial Network (GAN)

<img src="note_05.assets/image-20210722095356201.png" alt="image-20210722095356201" style="zoom:50%;" />

<img src="note_05.assets/image-20210722095733785.png" alt="image-20210722095733785" style="zoom:33%;" />

- Anime Face Generation
  - Unconditioanl generation
    - without $$x$$
  - **Discriminator**
  - <img src="note_05.assets/image-20210722095929793.png" alt="image-20210722095929793" style="zoom:33%;" />
<center class="half">
  - <img src="note_05.assets/image-20210722100143465.png" alt="image-20210722100143465" style="zoom: 24%;" /><img src="note_05.assets/image-20210722100328608.png" alt="image-20210722100328608" style="zoom:24%;" />
</center> 
- **adversarial**

- <img src="note_05.assets/image-20210722100819764.png" alt="image-20210722100819764" style="zoom: 40%;" />

- Regression && Classification

- <img src="note_05.assets/image-20210722102029500.png" alt="image-20210722102029500" style="zoom:40%;" />

- **Step3:**

- <img src="note_05.assets/image-20210722102130780.png" alt="image-20210722102130780" style="zoom:40%;" />

- <img src="note_05.assets/image-20210722102410261.png" alt="image-20210722102410261" style="zoom:33%;" />

  <center class="half">
  <img src="note_05.assets/image-20210722102520225.png" alt="image-20210722102520225" style="zoom: 24%;" /><img src="note_05.assets/image-20210722102630770.png" alt="image-20210722102630770" style="zoom:26%;" />
  </center>
  
  
- <img src="note_05.assets/image-20210722102904549.png" alt="image-20210722102904549" style="zoom:33%;" />

- <img src="note_05.assets/image-20210722102930076.png" alt="image-20210722102930076" style="zoom: 25%;" />

- 

---

## Theory behind GAN （2）

<img src="note_05.assets/image-20210722195936966.png" alt="image-20210722195936966" style="zoom: 33%;" />



- $$
  G^{*}=\arg \min _{G} \textit{Div}\left(P_{G}, P_{\text {data }}\right)
  $$

  

- **Divergence**-->==How to compare the divergence ?==

  <img src="note_05.assets/image-20210722200931781.png" alt="image-20210722200931781" style="zoom:33%;" />

- We can **sample** the data to esitimate divergence.

<img src="note_05.assets/image-20210722201609225.png" alt="image-20210722201609225" style="zoom:33%;" />

> 1406.2661

- Discriminator-->binary classifier
- $$G^{*}=\arg \min _{G} \textit{Div}\left(P_{G}, P_{\text {data }}\right)\ \rightarrow D^{*}=\arg \max _{D} \textit{V}\left(D, G\right) $$
- $$V(G, D)=E_{y \sim P_{\text {data }}}[\log D(y)]+E_{y \sim P_{G}}[\log (1-D(y))]$$

<img src="note_05.assets/image-20210722202816357.png" alt="image-20210722202816357" style="zoom:33%;" />

<img src="note_05.assets/image-20210722203245962.png" alt="image-20210722203245962" style="zoom:40%;" />

- $$G^{*}=\arg \min _{G} \textit{Div}\left(P_{G}, P_{\text {data }}\right)\ \rightarrow G^{*}=\arg \min _{G} \max _{D} V\left(G,D\right)\ $$

<img src="note_05.assets/image-20210722203547784.png" alt="image-20210722203547784" style="zoom:33%;" />

> 1606.00709



### Tips for GAN



<img src="note_05.assets/image-20210722204555460.png" alt="image-20210722204555460" style="zoom:33%;" />

- **JS divergence has problem.**

<img src="note_05.assets/image-20210722205946027.png" alt="image-20210722205946027" style="zoom:33%;" />

<center class="half">
    <img src="note_05.assets/image-20210722210300298.png" alt="image-20210722210300298" style="zoom:25%;" /><img src="note_05.assets/image-20210722210406865.png" alt="image-20210722210406865" style="zoom:25%;" />
</center>

- **Wasserstein distance** is better
  - but it needs solving a **optimization problem**
  - <img src="note_05.assets/image-20210722210915661.png" alt="image-20210722210915661" style="zoom:33%;" />
- <img src="note_05.assets/image-20210722211351900.png" alt="image-20210722211351900" style="zoom:33%;" />
  
  - eye sight evolution
  
- WGAN

  - <img src="note_05.assets/image-20210722211857593.png" alt="image-20210722211857593" style="zoom:33%;" />

    

  - $$
    \max _{D \in 1-Lipschitz}\{E_{y\sim P_{data}}[D(x)] - E_{y\sim P_G}[D(x)]\}
    $$

  - <img src="note_05.assets/image-20210722212658746.png" alt="image-20210722212658746" style="zoom:33%;" />

  - 

---

## GAN(3)

- Spectral Normalization: **SNGAN**

- Problem:
  1. D can't tell the difference
  2. G fail to improve
  3. D fail to improve
  4. G can't fool the D

- <img src="note_05.assets/image-20210723132728489.png" alt="image-20210723132728489" style="zoom:33%;" />

- <img src="note_05.assets/image-20210723132856691.png" alt="image-20210723132856691" style="zoom:33%;" />

- > 1511.06434
  >
  > 1606.03498
  >
  > 1809.11096

- GAN for Sequence Generation

- Decoder->(max)-> Discriminator: unchanged

- <img src="note_05.assets/image-20210723133346926.png" alt="image-20210723133346926" style="zoom:33%;" />

- Why CNN(Max pooling) can ?

- Use **Reinforcement Learning**

  - <img src="note_05.assets/image-20210723133558202.png" alt="image-20210723133558202" style="zoom:33%;" />
  - <img src="note_05.assets/image-20210723133732076.png" alt="image-20210723133732076" style="zoom:33%;" />

- more : VAE Flow-based Model

- Why can't use **Surpervise**(under observation) **Learning**

- <img src="note_05.assets/image-20210723134348059.png" alt="image-20210723134348059" style="zoom:33%;" />

  

  ### Evaluation of Generation

  <center class="half">
  <img src="note_05.assets/image-20210723134555944.png" alt="image-20210723134555944" style="zoom: 25%;" /><img src="note_05.assets/image-20210723134743335.png" alt="image-20210723134743335" style="zoom:25%;" />
  </center>

- Mode Collapse

- <img src="note_05.assets/image-20210723135049530.png" alt="image-20210723135049530" style="zoom:33%;" />

- Mode Dropping

- <img src="note_05.assets/image-20210723135302602.png" alt="image-20210723135302602" style="zoom:33%;" />

- <center class="half">
  <img src="note_05.assets/image-20210723135403876.png" alt="image-20210723135403876" style="zoom: 26%;" /><img src="note_05.assets/image-20210723135709106.png" alt="image-20210723135709106" style="zoom: 20%;" />
  </center>
  
  - High **Quality** : more ==concentrate== for **each output classify**
  - High **Diversity** : more ==average== for **one input's outputs classify** in different stage

- <img src="note_05.assets/image-20210723140444258.png" alt="image-20210723140444258" style="zoom:50%;" />

- FID
- <img src="note_05.assets/image-20210723141208309.png" alt="image-20210723141208309" style="zoom:33%;" />

> [弗朗明歇距离（frechet distance） - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/265457722)

<img src="note_05.assets/image-20210723141255494.png" alt="image-20210723141255494" style="zoom:33%;" />

> 1711.10337

- <img src="note_05.assets/image-20210723141612776.png" alt="image-20210723141612776" style="zoom:33%;" />

- >  evaluation: 1802.03446

   

### Condition Generation

<img src="note_05.assets/image-20210723143159385.png" alt="image-20210723143159385" style="zoom:33%;" />

- Conditional GAN
- <img src="note_05.assets/image-20210723143348362.png" alt="image-20210723143348362" style="zoom: 40%;" />
- <img src="note_05.assets/image-20210723144855000.png" alt="image-20210723144855000" style="zoom:33%;" />
- Besides,  tell the discriminator bad output **if the image donot corrospond with text**

<img src="note_05.assets/image-20210723145117737.png" alt="image-20210723145117737" style="zoom:33%;" />

<img src="note_05.assets/image-20210723145630503.png" alt="image-20210723145630503" style="zoom:33%;" />

- GAN+Supervised

- <img src="note_05.assets/image-20210723145832486.png" alt="image-20210723145832486" style="zoom:33%;" />

- > 1808.04108

  <img src="note_05.assets/image-20210723150037833.png" alt="image-20210723150037833" style="zoom:33%;" />



---

## GAN(4) Cycle GAN

###  Learning from Unpaired Data

- In unsupervise learning
- <img src="note_05.assets/image-20210723150824225.png" alt="image-20210723150824225" style="zoom:33%;" />
- <img src="note_05.assets/image-20210723150936834.png" alt="image-20210723150936834" style="zoom:33%;" />
- ==Idea: Domain $$x, y$$ is also  a distribution==
- <img src="note_05.assets/image-20210723151358982.png" alt="image-20210723151358982" style="zoom:33%;" />
- The output of $G_{x \rightarrow y}$ should be similar to domain $y$ 
- <img src="note_05.assets/image-20210723151813750.png" alt="image-20210723151813750" style="zoom:33%;" />
- So add the check: $G_{y \rightarrow x}$ Cycle consistency

<img src="note_05.assets/image-20210723152204056.png" alt="image-20210723152204056" style="zoom:33%;" />

- <img src="note_05.assets/image-20210723152548471.png" alt="image-20210723152548471" style="zoom:33%;" />
  - symmety
  
- <img src="note_05.assets/image-20210723152658019.png" alt="image-20210723152658019" style="zoom:33%;" />

- <img src="note_05.assets/image-20210723152824598.png" alt="image-20210723152824598" style="zoom:33%;" />

- <center class="half">
     <img src="note_05.assets/image-20210723153005884.png" alt="image-20210723153005884" style="zoom:25%;" /><img src="note_05.assets/image-20210723153315509.png" alt="image-20210723153315509" style="zoom:25%;" />


- <img src="note_05.assets/image-20210723153702767.png" alt="image-20210723153702767" style="zoom:33%;" />

     

     ---

     























