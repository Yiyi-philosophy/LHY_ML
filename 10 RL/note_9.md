# Introduction of 

# Deep Reinforcemnet learning

## (1)Surpervise Learning ->  RL

<img src="note_9.assets/image-20210925170906401.png" alt="image-20210925170906401" style="zoom:50%;" />

<img src="note_9.assets/image-20210926161807928.png" alt="image-20210926161807928" style="zoom:50%;" />



### What is RL? (3 step)

$$
\text{Input(Obsrvation)}\ \underset{\longrightarrow}{F} \ \text{Output(Action)}\\
\uparrow \ \ \ \ \ \ \  \ \ \ \ \ \ \ \ \Uparrow \text{Reward} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \downarrow\\

\nwarrow \ \ \ \ \ \ \ \ \ \text{Enviromnent} \ \ \ \ \ \ \ \ \swarrow
$$

<img src="note_9.assets/image-20210925171739717.png" alt="image-20210925171739717" style="zoom:50%;" />

#### Space invader

<img src="note_9.assets/image-20210925171858702.png" alt="image-20210925171858702" style="zoom:50%;" />

- $Find \ F^*$

<img src="note_9.assets/image-20210925172350837.png" alt="image-20210925172350837" style="zoom:50%;" />

- Go

<img src="note_9.assets/image-20210925172609649.png" alt="image-20210925172609649" style="zoom:50%;" />

- The reward is hard to analyze

#### Three step

<img src="note_9.assets/image-20210925172629401.png" alt="image-20210925172629401" style="zoom:50%;" />

- Step1
  - <img src="note_9.assets/image-20210925172910549.png" alt="image-20210925172910549" style="zoom:50%;" />
- Step2
  - <img src="note_9.assets/image-20210925204053664.png" alt="image-20210925204053664" style="zoom:50%;" />
  - <img src="note_9.assets/image-20210925204134127.png" alt="image-20210925204134127" style="zoom:50%;" />
    - **episode** 
    - reward: $\max\{R=\sum_{t=1}^{T}r_t\}$​​​ 
- Step3:
  -    
    1. The output is random
    2. Environment is a black box 
    3. Environment is random too
  -    **How to do optimization is becoming big problem.** 
  -    <img src="note_9.assets/image-20210925205749043.png" alt="image-20210925205749043" style="zoom:50%;" />
  -    ==like *GAN*==

### Policy Gradient

- Testing has randomness

<img src="note_9.assets/image-20210925213152163.png" alt="image-20210925213152163" style="zoom:50%;" />

<img src="note_9.assets/image-20210925213226793.png" alt="image-20210925213226793" style="zoom:50%;" />
$$
L=e_1-e_2\\
\theta^*=\arg\underset{\theta}{\min}L
$$

- A **Calssifier** ? 
- A **Supervised Learning** training ?

#### How to control your actor

<center calss="half">
    <img src="note_9.assets/image-20210925213644282.png" alt="image-20210925213644282" style="zoom:34%;" /><img src="note_9.assets/image-20210925213835942.png" alt="image-20210925213835942" style="zoom:33%;" />
</center>
## (2)

### 

- Find $A$ 

- **Version 0**

  - <img src="note_9.assets/image-20210926105803297.png" alt="image-20210926105803297" style="zoom:50%;" />
  - **Greedy** -> **Dynamic planning **
  - <img src="note_9.assets/image-20210926105957847.png" alt="image-20210926105957847" style="zoom:50%;" />
  - 

- **Version  1**

  - **Markv chain** 
  - <img src="note_9.assets/image-20210926110213763.png" alt="image-20210926110213763" style="zoom:50%;" />
  - ==Cumulated reward==  $G_t=\sum_{n=t}^{T}r_n$ 

- **Version 2** 

  - <img src="note_9.assets/image-20210926110514600.png" alt="image-20210926110514600" style="zoom:50%;" />
  - $G_t'=\sum_{n=t}^{T}\gamma^{n-t} r_n$​​​ 
  - 

- **Version 3**

  - reward is "**realtive**" 
  - **Standardization**
  - <img src="note_9.assets/image-20210926111126998.png" alt="image-20210926111126998" style="zoom:50%;" />
  - So how to find  $b$​​  

#### Policy Gradient

  <img src="note_9.assets/image-20210926111440438.png" alt="image-20210926111440438" style="zoom: 50%;" />

  - Data collection cost a lot.
  - Each time we only undate the parameters **once**.

  <img src="note_9.assets/image-20210926111535533.png" alt="image-20210926111535533" style="zoom:50%;" />

  - <img src="note_9.assets/image-20210926111736765.png" alt="image-20210926111736765" style="zoom:50%;" />

  - $\theta^i \leftarrow \theta^{i-1}- \eta\nabla L $ 
  - The former training is best for $\theta^{i-1}$ , but may not for $\theta^i$​ .
  - <img src="note_9.assets/image-20210926112223285.png" alt="image-20210926112223285" style="zoom:50%;" />

#### On Policy && Off Policy

  - <img src="note_9.assets/image-20210926112419308.png" alt="image-20210926112419308" style="zoom:50%;" />
  - <img src="note_9.assets/image-20210926112607706.png" alt="image-20210926112607706" style="zoom:50%;" />


#### Exploration

- It hope to try more actions. -> **Randomness** 
- Enlarge output entropy.
- <img src="note_9.assets/image-20210926112933168.png" alt="image-20210926112933168" style="zoom:50%;" />
  - DeepMind - PPO
  - OpenAl - PPO

## (3)

### Actor Critic

- $V^\theta(s)$​ Predict the value of $s$ 

<img src="note_9.assets/image-20210926114731380.png" alt="image-20210926114731380" style="zoom:50%;" />

- The output value denpends on the actor evaluated.

#### How to estimate $V^\theta(s)$ 

- Monte-Carlo based approach **(MC)**

  - <img src="note_9.assets/image-20210926115058950.png" alt="image-20210926115058950" style="zoom:50%;" />

- Temporal-difference approach **(TD)**

  - $V^\pi(s)$​ 
  - <img src="note_9.assets/image-20210926115506882.png" alt="image-20210926115506882" style="zoom:50%;" />

- MC & TD

  - <img src="note_9.assets/image-20210926115726957.png" alt="image-20210926115726957" style="zoom:50%;" />

  - $$
    V^\theta(s_b)=\frac{3}{4}\\
    V^\theta(s_a)= ?\  {\color{red}0?\ \frac{3}{4}? }
    $$

  - <img src="note_9.assets/image-20210926120116317.png" alt="image-20210926120116317" style="zoom:50%;" />

- **Version 3.5** 

  - <img src="note_9.assets/image-20210926155732600.png" alt="image-20210926155732600" style="zoom:50%;" />

  - $s_t$​  an expected value

  - **We sample the actions based on a distribution .** 

  - <img src="note_9.assets/image-20210926160309042.png" alt="image-20210926160309042" style="zoom:50%;" />

  - $$
    s_t \rightarrow G_1,G_2,...\ \ \rightarrow V^\theta(s_t)=\frac{1}{n}\sum_{i=1}^{n}G_i \\
    A_t=G_t'-V^\theta(s_t)\\ 
    \begin{cases}
    & A_t>0,\ a_t>\bar{a} \\
    & A_t>0,\ a_t<\bar{a} \\
    \end{cases}
    \\\\
    s_t \ \underset{\longrightarrow}{a_t}\  G_t'
    $$

- **Version 4**

  - <img src="note_9.assets/image-20210926161231996.png" alt="image-20210926161231996" style="zoom:50%;" />

  - $$
    A_t=r_t+V^\theta(s_{t+1})-V^\theta(s_t)
    $$

  - **Advantage Actor-Critic** 

  - <img src="note_9.assets/image-20210926161516430.png" alt="image-20210926161516430" style="zoom:50%;" />

  - Shared same parameters

  - 

#### DQN

<img src="note_9.assets/image-20210926161602019.png" alt="image-20210926161602019" style="zoom:50%;" />

## (4)

### Reward Shaping

#### Sparse Reward

- GO ? 
- robot arm to bolt on the screws
- <img src="note_9.assets/image-20210926162254791.png" alt="image-20210926162254791" style="zoom:50%;" />
  - Add extra rewards to guide agents -> **Reward shaping** 

#### Reward Shaping

<img src="note_9.assets/image-20210926162527141.png" alt="image-20210926162527141" style="zoom:50%;" />

- Living: negative
- stay: negative
- **Need Domian knowledge** 
  - <img src="note_9.assets/image-20210926162906027.png" alt="image-20210926162906027" style="zoom:50%;" />
- **Curiosity  Based**
  - <img src="note_9.assets/image-20210926162958554.png" alt="image-20210926162958554" style="zoom:50%;" />
  - See more things **(meaningful)** 
  - <img src="note_9.assets/image-20210926163336789.png" alt="image-20210926163336789" style="zoom:50%;" />

### No reward: Learning from Demonsration

#### Motivation

- Even define reward can be challenging in some tasks.
- Hand-craft rewards may lead to uncontrolled behavior

<img src="note_9.assets/image-20210926163645592.png" alt="image-20210926163645592" style="zoom:50%;" />

#### Imitation Learning 

- Demonstration
  - <img src="note_9.assets/image-20210926163842641.png" alt="image-20210926163842641" style="zoom:50%;" />
- Behavior Cloning
  - <img src="note_9.assets/image-20210926164011709.png" alt="image-20210926164011709" style="zoom:50%;" />
  - Problem : 
    - The expert only sample limited observation.
    - Some irrelevant actions.
    - <img src="note_9.assets/image-20210926164253564.png" alt="image-20210926164253564" style="zoom:50%;" />

#### Inverse RL

Former:

<img src="note_9.assets/image-20210926164452792.png" alt="image-20210926164452792" style="zoom:50%;" />

Later:

<img src="note_9.assets/image-20210926164530285.png" alt="image-20210926164530285" style="zoom:50%;" />

- Back to learn:  **"Counterpropagation Network"**

- **Algorithm**
  - <img src="note_9.assets/image-20210926164945816.png" alt="image-20210926164945816" style="zoom:50%;" />
  - <img src="note_9.assets/image-20210926165055083.png" alt="image-20210926165055083" style="zoom:50%;" />
- GAN && IRL
- <img src="note_9.assets/image-20210926165341376.png" alt="image-20210926165341376" style="zoom:50%;" />
- Robot
  - <img src="note_9.assets/image-20210926165636217.png" alt="image-20210926165636217" style="zoom:50%;" />
  - <img src="note_9.assets/image-20210926165812361.png" alt="image-20210926165812361" style="zoom:50%;" />
    - Set some goal by itself
    - 















