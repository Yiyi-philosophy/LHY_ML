# Self-Supervised Learning

## 1.

<img src="note_7.assets/image-20210920183653485.png" alt="image-20210920183653485" style="zoom:50%;" />



- BERT
  - 340 million parameters
  - <img src="note_7.assets/image-20210920183954996.png" alt="image-20210920183954996" style="zoom: 33%;" />
  - <img src="note_7.assets/image-20210920184039380.png" alt="image-20210920184039380" style="zoom: 33%;" />
  - <img src="note_7.assets/image-20210920184140902.png" alt="image-20210920184140902" style="zoom:33%;" />

## 2. Self-supervise Learning

<img src="note_7.assets/image-20210920184635550.png" alt="image-20210920184635550" style="zoom:50%;" />

- $S_{self-supervise}\in S_{un-supervise}$​

 <center class="half">
     <img src="note_7.assets/image-20210920185157478.png" alt="image-20210920185157478" style="zoom:30%;" /><img src="note_7.assets/image-20210920185311965.png" alt="image-20210920185311965" style="zoom:30%;" />

<center class="half">
    <img src="note_7.assets/image-20210920185550110.png" alt="image-20210920185550110" style="zoom:26%;" /><img src="note_7.assets/image-20210920185643312.png" alt="image-20210920185643312" style="zoom:26%;" />

- Bert : A classification
  - **the number of kinds is the number of word vocabulary**
  - Learn to **"fill the blank"**

- Next Sentence Prediction
  - <img src="note_7.assets/image-20210920190202100.png" alt="image-20210920190202100" style="zoom:33%;" />
  - [CLS] | - Sen~1~ - | [SEP] | - Sen~2~ |...
  - <img src="note_7.assets/image-20210920190355394.png" alt="image-20210920190355394" style="zoom:33%;" />
  - the output of [CLS] **judge whether Sen~2~ is next to Sen~1~** 
  - Manybe not work
    - It's too ==easy== for the **BERT**
  - SOP:
    - <img src="note_7.assets/image-20210920190739459.png" alt="image-20210920190739459" style="zoom:33%;" />
- **BERT:**
  - Mask token prediction
  - Next Sentence Prediction
- **Downstream Task**
  - The tasks we care
  - We have a little bit labeled data

<img src="note_7.assets/image-20210920191232611.png" alt="image-20210920191232611" style="zoom:40%;" />

### **Pre-train -> Fine-tune**

- <img src="note_7.assets/image-20210920191336946.png" alt="image-20210920191336946" style="zoom:40%;" />

- Datasets: GLUE 9
  - <img src="note_7.assets/image-20210920191521513.png" alt="image-20210920191521513" style="zoom:40%;" />

- Black Line: human ablility
- Case1: Sentiment analysis
  - <img src="note_7.assets/image-20210920191937261.png" alt="image-20210920191937261" style="zoom:40%;" />
  - ==Init of BERT is pre-trained by **"fill the blank"**== 
  - <img src="note_7.assets/image-20210920192302499.png" alt="image-20210920192302499" style="zoom:40%;" />
- Case2: POS tagging
  - <img src="note_7.assets/image-20210920192749076.png" alt="image-20210920192749076" style="zoom:40%;" />
- Case3: NLI
  - <img src="note_7.assets/image-20210920193045823.png" alt="image-20210920193045823" style="zoom:40%;" />
  - <img src="note_7.assets/image-20210920193158414.png" alt="image-20210920193158414" style="zoom:40%;" />
  - ==[CLS]: classification==
- Case4: Extraction-based Q&A
  - <img src="note_7.assets/image-20210920193418550.png" alt="image-20210920193418550" style="zoom:40%;" />
  - <img src="note_7.assets/image-20210920193737879.png" alt="image-20210920193737879" style="zoom:40%;" />
  - <img src="note_7.assets/image-20210920193759316.png" alt="image-20210920193759316" style="zoom:40%;" />
  - The length of BERT : 512   (Not too long)
  - Divid the long documnet into shorter, and put in in order.
- <img src="note_7.assets/image-20210920194321848.png" alt="image-20210920194321848" style="zoom:40%;" />
- <img src="note_7.assets/image-20210920194402970.png" alt="image-20210920194402970" style="zoom:40%;" />
- What dose BERT learn in pre-train ?
  - The answer is counterintuitive.

### **Seq2seq**

- <img src="note_7.assets/image-20210920194733650.png" alt="image-20210920194733650" style="zoom:40%;" />
- <img src="note_7.assets/image-20210920194811676.png" alt="image-20210920194811676" style="zoom:40%;" />

- Why?



<img src="note_7.assets/image-20210920195125523.png" alt="image-20210920195125523" style="zoom:50%;" />

- BERT is an encoder represent same meaning

<img src="note_7.assets/image-20210920195300878.png" alt="image-20210920195300878" style="zoom:40%;" />

<img src="note_7.assets/image-20210920195328665.png" alt="image-20210920195328665" style="zoom:33%;" />

- In pre-train, BERT seems to "**learn**" the meaning of each word.
- ==You shall know a word by the company it keeps.== 
- <img src="note_7.assets/image-20210920200028704.png" alt="image-20210920200028704" style="zoom:40%;" />
- **Word embedding --> Contextualized word embedding**

### A problem  

- <img src="note_7.assets/image-20210920200245079.png" alt="image-20210920200245079" style="zoom:40%;" />

<img src="note_7.assets/image-20210920200452969.png" alt="image-20210920200452969" style="zoom:40%;" />

- A mass train--> good output

<img src="note_7.assets/image-20210920200602169.png" alt="image-20210920200602169" style="zoom:50%;" />



### Multi-lingual BERT

- <img src="note_7.assets/image-20210920200835125.png" alt="image-20210920200835125" style="zoom:33%;" />
- <img src="note_7.assets/image-20210920200902044.png" alt="image-20210920200902044" style="zoom:33%;" />
- <img src="note_7.assets/image-20210920200944786.png" alt="image-20210920200944786" style="zoom:40%;" />
- <img src="note_7.assets/image-20210920201100294.png" alt="image-20210920201100294" style="zoom:40%;" />
- May be it's very close to the same meaning words in different language





- <img src="note_7.assets/image-20210920201523676.png" alt="image-20210920201523676" style="zoom:40%;" />
- <img src="note_7.assets/image-20210920201541176.png" alt="image-20210920201541176" style="zoom:33%;" />

- Weird
  - <img src="note_7.assets/image-20210920201722592.png" alt="image-20210920201722592" style="zoom:40%;" />
  - If the embedding is language independent.
    - How to correctly reconstruct?
      - There must be language information
  - <img src="note_7.assets/image-20210920201959306.png" alt="image-20210920201959306" style="zoom:40%;" />
  - It seems like English word is a **"small move"** to Chinese word.
  - <img src="note_7.assets/image-20210920202233948.png" alt="image-20210920202233948" style="zoom:40%;" />
  - 

## 4. GPT

- Predict Next Token

- <img src="note_7.assets/image-20210920202639640.png" alt="image-20210920202639640" style="zoom:40%;" />

- <img src="note_7.assets/image-20210920202705694.png" alt="image-20210920202705694" style="zoom:40%;" />

- > https://app.inferkit.com/demo

- <img src="note_7.assets/image-20210920204410458.png" alt="image-20210920204410458" style="zoom:40%;" />

- <img src="note_7.assets/image-20210920204619205.png" alt="image-20210920204619205" style="zoom:40%;" />

<img src="note_7.assets/image-20210920204702319.png" alt="image-20210920204702319" style="zoom:40%;" />

- more task 

<img src="note_7.assets/image-20210920204822346.png" alt="image-20210920204822346" style="zoom:40%;" />

- Image - SimCLR
  - <img src="note_7.assets/image-20210920205052214.png" alt="image-20210920205052214" style="zoom:40%;" />

<img src="note_7.assets/image-20210920205110024.png" alt="image-20210920205110024" style="zoom:40%;" />

### SUPERB - GULE 

<img src="note_7.assets/image-20210920205228294.png" alt="image-20210920205228294" style="zoom:40%;" />

- <img src="note_7.assets/image-20210920205541819.png" alt="image-20210920205541819" style="zoom:40%;" />



---

# Auto-encoder

## Basic idea of Auto-encoder
### Self-supervised learning

<img src="note_7.assets/image-20210921191800225.png" alt="image-20210921191800225" style="zoom:40%;" />

- Auto-encoder == Self-surpervise
- <img src="note_7.assets/image-20210921191935357.png" alt="image-20210921191935357" style="zoom:33%;" />
- 



<center class="half">
    <img src="note_7.assets/image-20210921192050984.png" alt="image-20210921192050984" style="zoom:28%;" /><img src="note_7.assets/image-20210921192238211.png" alt="image-20210921192238211" style="zoom:28%;" />
<img src="note_7.assets/image-20210921192635656.png" alt="image-20210921192635656" style="zoom:40%;" />

- Auto-encoder ~~ Cycle GAN
  - Vector: embedding "bottleneck"
  - **Dimension reduction** 

### Why Auto-encoder ?

- In image, it has  many redundancy (冗余) .
- It can be compressed by few base vector.
- <img src="note_7.assets/image-20210921193849727.png" alt="image-20210921193849727" style="zoom:40%;" />

<img src="note_7.assets/image-20210921193817808.png" alt="image-20210921193817808" style="zoom:40%;" />

### Former study 

<img src="note_7.assets/image-20210921193919528.png" alt="image-20210921193919528" style="zoom:30%;" />

### De-noising Auto-encoder

<img src="note_7.assets/image-20210921194437344.png" alt="image-20210921194437344" style="zoom:40%;" />

- BERT is another "De-noising Auto-encoder"



<img src="note_7.assets/image-20210921194623958.png" alt="image-20210921194623958" style="zoom:40%;" />

## Feature Disentanglemnet

-  **Disentanglemnet** : the act of releasing from a snarled or tangled condition
  - <img src="note_7.assets/image-20210921195214274.png" alt="image-20210921195214274" style="zoom:40%;" />
  - <img src="note_7.assets/image-20210921201611861.png" alt="image-20210921201611861" style="zoom:40%;" />

### Voice Convers

<img src="note_7.assets/image-20210921202134572.png" alt="image-20210921202134572" style="zoom:40%;" />

<img src="note_7.assets/image-20210921202430405.png" alt="image-20210921202430405" style="zoom:40%;" />



## Discrete latent Representation

<img src="note_7.assets/image-20210921202831521.png" alt="image-20210921202831521" style="zoom:40%;" />

<img src="note_7.assets/image-20210921203408077.png" alt="image-20210921203408077" style="zoom:40%;" />

- phonetic : of or relating to speech sounds



- Text: Summary ? 

<img src="note_7.assets/image-20210921203710095.png" alt="image-20210921203710095" style="zoom:40%;" />

- Problem: the "summary" can't be understand.

<img src="note_7.assets/image-20210921204004238.png" alt="image-20210921204004238" style="zoom:40%;" />

- Can't to train --> **RL** 

<img src="note_7.assets/image-20210921204141613.png" alt="image-20210921204141613" style="zoom: 33%;" />

<img src="note_7.assets/image-20210921204235774.png" alt="image-20210921204235774" style="zoom:33%;" />

### Tree Structure

<img src="note_7.assets/image-20210921204256049.png" alt="image-20210921204256049" style="zoom:40%;" />

## More

<img src="note_7.assets/image-20210921204407774.png" alt="image-20210921204407774" style="zoom:40%;" />

### Compress

<img src="note_7.assets/image-20210921204524450.png" alt="image-20210921204524450" style="zoom:40%;" />

### Anomaly Detection

<img src="note_7.assets/image-20210921204937742.png" alt="image-20210921204937742" style="zoom:40%;" />



<img src="note_7.assets/image-20210921205100484.png" alt="image-20210921205100484" style="zoom:40%;" />

- Application
  - Fraud Detection
  - Network Instrusion Detection
  - Cancer Detection
- Binary Classification?
  - NO! We only have one calss.
  - 

<img src="note_7.assets/image-20210921205433632.png" alt="image-20210921205433632" style="zoom:40%;" />

<img src="note_7.assets/image-20210921205526761.png" alt="image-20210921205526761" style="zoom:40%;" />





