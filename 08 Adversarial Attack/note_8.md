# Adversarial Attack 

## (1)Local Explation

<img src="note_8.assets/image-20210922211447042.png" alt="image-20210922211447042" style="zoom:40%;" />

- 

### How to Attack

<img src="note_8.assets/image-20210922211749571.png" alt="image-20210922211749571" style="zoom:40%;" />

- Attack
  - Non-targeted
  - Targeted

<img src="note_8.assets/image-20210922212008405.png" alt="image-20210922212008405" style="zoom:40%;" />

- Normal Noise

<img src="note_8.assets/image-20210922212200789.png" alt="image-20210922212200789" style="zoom: 25%;" />

- Optimization

<center class="half">
    <img src="note_8.assets/image-20210922212658494.png" alt="image-20210922212658494" style="zoom:25%;" /><img src="note_8.assets/image-20210922212905416.png" alt="image-20210922212905416" style="zoom:25%;" />
</center>

- To find
  $$
  \pmb{x^*}=\arg \underset{d(\pmb{x}^0,\pmb{x}) \leq \varepsilon}{\min} L(x)
  $$


  - Find $d$ 
  - <img src="note_8.assets/image-20210922213713491.png" alt="image-20210922213713491" style="zoom:40%;" />
  - **L-infinity > L2-norm** 
  - ==Need to consider human perception== 
  - ==Need domain knowledge== 

### Attack Approach

<img src="note_8.assets/image-20210922214709584.png" alt="image-20210922214709584" style="zoom:40%;" />

#### FGSM

<img src="note_8.assets/image-20210922214921335.png" alt="image-20210922214921335" style="zoom:40%;" />

- simple baseline

#### Interation FGSM

<img src="note_8.assets/image-20210922215050902.png" alt="image-20210922215050902" style="zoom:40%;" />

- medium baseline



## Adversarial Attack (2)

### White & Black box

- Black box attack is **possible** \
- <img src="note_8.assets/image-20210923141703309.png" alt="image-20210923141703309" style="zoom: 40%;" />
- **Use "Proxy"**
- <img src="note_8.assets/image-20210923141755855.png" alt="image-20210923141755855" style="zoom:40%;" />

### If we **don't know** the training data ? 

- Put new data into the model and get  outputs.

<img src="note_8.assets/image-20210923142329969.png" alt="image-20210923142329969" style="zoom:40%;" />

- Ensemble Attack --> Ensemble learning
  - Mixed model

### Why attack is so easy?

- The **weak** derection is narrow for most network.
  - <img src="note_8.assets/image-20210923142952181.png" alt="image-20210923142952181" style="zoom:45%;" />
- problem maybe come from the data
- One pixel attack
  - <img src="note_8.assets/image-20210923143242982.png" alt="image-20210923143242982" style="zoom:45%;" />

- Universal attack

  - <img src="note_8.assets/image-20210923143424881.png" alt="image-20210923143424881" style="zoom:45%;" />

    

### Beyond Image

<img src="note_8.assets/image-20210923143645522.png" alt="image-20210923143645522" style="zoom:45%;" />

### Attack the Physical world

<img src="note_8.assets/image-20210923144449282.png" alt="image-20210923144449282" style="zoom:45%;" />

- Consider
  - Different point of view.
  - Camera's capture accurateness.
  - The color affected by actual world.

<img src="note_8.assets/image-20210923144757172.png" alt="image-20210923144757172" style="zoom:33%;" />

<img src="note_8.assets/image-20210923144853383.png" alt="image-20210923144853383" style="zoom:33%;" />

### Adversarial Reprogramming

<img src="note_8.assets/image-20210923145123434.png" alt="image-20210923145123434" style="zoom:40%;" />

### Blackdoor in Model

<img src="note_8.assets/image-20210923145250213.png" alt="image-20210923145250213" style="zoom:40%;" />

- **Be careful of unknown dataset ......**



### defense

- Passive Defense
  - <img src="note_8.assets/image-20210923145702741.png" alt="image-20210923145702741" style="zoom:40%;" />
- <img src="note_8.assets/image-20210923145830747.png" alt="image-20210923145830747" style="zoom:40%;" />
- Fliter : Smoothing
  - Side effect
- <img src="note_8.assets/image-20210923145914397.png" alt="image-20210923145914397" style="zoom:40%;" />
- If attacker known the method, it can't work soon.
- **Add Randomization Defend method**
  - <img src="note_8.assets/image-20210923150035105.png" alt="image-20210923150035105" style="zoom:40%;" />
  - **Universal attack**

### Proactive Defense

- Adversarial training
  - <img src="note_8.assets/image-20210923153638430.png" alt="image-20210923153638430" style="zoom:40%;" />
  - ==Data Augmentation== 
  
  > Adversarial Training for free!
  >
  > 1904.12843

<img src="note_8.assets/image-20210923153927659.png" alt="image-20210923153927659" style="zoom:50%;" />



# Explainable Machine Learning

## (1)

### Why we need explainable ML?

<img src="note_8.assets/image-20210923154541144.png" alt="image-20210923154541144" style="zoom:40%;" />

-  We want to the reason behind decision
- <img src="note_8.assets/image-20210923154708580.png" alt="image-20210923154708580" style="zoom:40%;" />
- <img src="note_8.assets/image-20210923154830237.png" alt="image-20210923154830237" style="zoom:50%;" />
- 

### Interpretable && Powerful

<img src="note_8.assets/image-20210923155924568.png" alt="image-20210923155924568" style="zoom:40%;" />

<img src="note_8.assets/image-20210923160014072.png" alt="image-20210923160014072" style="zoom:40%;" />



- Explainable && Interpretable
  - Explainable: Black box --> Grey & White
  -  Interpretable： capable of being understood

### Decision Tree

<img src="note_8.assets/image-20210923160319098.png" alt="image-20210923160319098" style="zoom:40%;" />

<img src="note_8.assets/image-20210923160409306.png" alt="image-20210923160409306" style="zoom:40%;" />

- It also a **"Black box"** 

### Goal for explainable ML

- Completely know how the **whole** model works ?
  - But we trust the desicions of huamn. 
  - The **reason** is important.
  - <img src="note_8.assets/image-20210923160916616.png" alt="image-20210923160916616" style="zoom:40%;" />

- <img src="note_8.assets/image-20210923161109906.png" alt="image-20210923161109906" style="zoom:50%;" />

### Case

<img src="note_8.assets/image-20210923161157616.png" alt="image-20210923161157616" style="zoom:40%;" />

### Local Explaination

<img src="note_8.assets/image-20210923161223101.png" alt="image-20210923161223101" style="zoom:50%;" />

<img src="note_8.assets/image-20210923161410279.png" alt="image-20210923161410279" style="zoom:40%;" />

- Find the important component:
  - Removing or change the components
  - Large decision change
  - **-->** Important component

<img src="note_8.assets/image-20210923161857043.png" alt="image-20210923161857043" style="zoom:50%;" />

- Use **shelter** to **confirm** 

- Analyze Gradient
  - <img src="note_8.assets/image-20210923162203636.png" alt="image-20210923162203636" style="zoom:40%;" />
  - Saliency Maps
- <img src="note_8.assets/image-20210923162423705.png" alt="image-20210923162423705" style="zoom:40%;" />
- <img src="note_8.assets/image-20210923162501083.png" alt="image-20210923162501083" style="zoom:40%;" />
- High test accuracy ==98.4%==

<center class="half" >
    <img src="note_8.assets/image-20210923162813755.png" alt="image-20210923162813755" style="zoom:25%;" /><img src="note_8.assets/image-20210923162832184.png" alt="image-20210923162832184" style="zoom:25%;" />
</center>

<img src="note_8.assets/image-20210923162907658.png" alt="image-20210923162907658" style="zoom:40%;" />

<img src="note_8.assets/image-20210923163000581.png" alt="image-20210923163000581" style="zoom:40%;" />

### Limitation

<img src="note_8.assets/image-20210923163109592.png" alt="image-20210923163109592" style="zoom:40%;" />

- Add the random noise and **Take the intersection** 
- Gradient can't **reflect** importance
  - <img src="note_8.assets/image-20210923163440767.png" alt="image-20210923163440767" style="zoom:40%;" />
- How to see the change in input data?
  - <img src="note_8.assets/image-20210923213949066.png" alt="image-20210923213949066" style="zoom:40%;" />
- <img src="note_8.assets/image-20210923214207449.png" alt="image-20210923214207449" style="zoom:40%;" />
- Attention
  - <img src="note_8.assets/image-20210923214415546.png" alt="image-20210923214415546" style="zoom:40%;" />
  - <img src="note_8.assets/image-20210923214522487.png" alt="image-20210923214522487" style="zoom:40%;" />
  - Be careful about the classifier you use.
- <img src="note_8.assets/image-20210923214758901.png" alt="image-20210923214758901" style="zoom:40%;" />
  - Aim to clean the member of voice
    - put the input data (voice)
    - Use probing TTS to reconstruction the voice
    - Compare the reconstruction  voice and input voice
    - To confirm this model understand "non-member" voice

<img src="note_8.assets/image-20210923220214466.png" alt="image-20210923220214466" style="zoom:40%;" />

---



## (2)Global explation: explain the whole world

<img src="note_8.assets/image-20210923220434348.png" alt="image-20210923220434348" style="zoom:50%;" />

### What does a filter detect ?

<img src="note_8.assets/image-20210923220713249.png" alt="image-20210923220713249" style="zoom:40%;" />

- Find $X^*$ ​
  - <img src="note_8.assets/image-20210923220904272.png" alt="image-20210923220904272" style="zoom:40%;" />

<img src="note_8.assets/image-20210924103955733.png" alt="image-20210924103955733" style="zoom:40%;" />

- Each fliter has it direction

- Look Output $y_i$ 

  - <img src="note_8.assets/image-20210924104145443.png" alt="image-20210924104145443" style="zoom:40%;" />
  - Consider Adversarial attack.

- <img src="note_8.assets/image-20210924104442234.png" alt="image-20210924104442234" style="zoom: 50%;" />

  - Make $X^*$ more like "number"
    - Add $R(X)=-\sum_{i,j}|X_{ij}|$​ to **estimate** how it like
    - Less "white point"
    - <img src="note_8.assets/image-20210924104751968.png" alt="image-20210924104751968" style="zoom:50%;" />

  

  ### Constraint from Generator

- <img src="note_8.assets/image-20210924105033361.png" alt="image-20210924105033361" style="zoom:50%;" />

$$
\text{Find} &X^*=\arg \underset{X}{\max}y_i \\
& \Rightarrow z^*=\arg \underset{z}{\max}y_i \\
& \text{Show Image:} \ X^*=G(z)
$$

<img src="note_8.assets/image-20210924105530558.png" alt="image-20210924105530558" style="zoom:50%;" />

> 1612.00005



### Outlook

<img src="note_8.assets/image-20210924105806910.png" alt="image-20210924105806910" style="zoom:50%;" />

