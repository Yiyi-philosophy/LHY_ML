## 04: Transformer-->BERT

- Sequence-to-sequence(Seq2seq)

- The output length is determined by model
- Application

<img src="note_04.assets/image-20210720110502014.png" alt="image-20210720110502014" style="zoom: 33%;" />

- language without text

- <img src="note_04.assets/image-20210720110728955.png" alt="image-20210720110728955" style="zoom:33%;" />

- <img src="note_04.assets/image-20210720110823995.png" alt="image-20210720110823995" style="zoom:33%;" />

- <img src="note_04.assets/image-20210720111119979.png" alt="image-20210720111119979" style="zoom:33%;" />

- <img src="note_04.assets/image-20210720111240939.png" alt="image-20210720111240939" style="zoom:33%;" />

- <img src="note_04.assets/image-20210720111651678.png" alt="image-20210720111651678" style="zoom:33%;" />

- **Most Natural language Processing applications is Q&A**

- > <img src="note_04.assets/image-20210720111846734.png" alt="image-20210720111846734" style="zoom:33%;" />
  >
  > http://speech.ee.ntu.edu.tw/~hylee/dlhlp/2020-spring.html

<img src="note_04.assets/image-20210720112232438.png" alt="image-20210720112232438" style="zoom:33%;" />

- Tree-->Seq2seq

- > <img src="note_04.assets/image-20210720112309362.png" alt="image-20210720112309362" style="zoom:33%;" />
  >
  > 1412.7449

<img src="note_04.assets/image-20210720112616648.png" alt="image-20210720112616648" style="zoom:33%;" />

- Multi-label Classification

- <img src="note_04.assets/image-20210720112829167.png" alt="image-20210720112829167" style="zoom:33%;" />

- > 2005.12872

- <img src="note_04.assets/image-20210720112945810.png" alt="image-20210720112945810" style="zoom:45%;" />

- Encoder
<center  class="half">
	<img src="note_04.assets/image-20210720113158909.png" alt="image-20210720113158909" style="zoom:25%;" /><img src="note_04.assets/image-20210720113318086.png" alt="image-20210720113318086" style="zoom:26%;" />
</center>

<img src="note_04.assets/image-20210720113912639.png" alt="image-20210720113912639" style="zoom:33%;" />

<img src="note_04.assets/image-20210720114116879.png" alt="image-20210720114116879" style="zoom:33%;" />

- BERT : transformer encoder

- <img src="note_04.assets/image-20210720114213129.png" alt="image-20210720114213129" style="zoom:50%;" />

- Other designer

  - > 2003.07845

---

### Decoder Autoregressive (AT)

- <img src="note_04.assets/image-20210720150140252.png" alt="image-20210720150140252" style="zoom:33%;" />\

- Error Propagation-->mistake transmit to later output

- <img src="note_04.assets/image-20210720150332542.png" alt="image-20210720150332542" style="zoom: 50%;" />

- <img src="note_04.assets/image-20210720150742554.png" alt="image-20210720150742554" style="zoom:33%;" />

- Masked self-attention


<center class="half">
	<img src="note_04.assets/image-20210720151044281.png" alt="image-20210720151044281" style="zoom: 25%;" /><img src="note_04.assets/image-20210720151020750.png" alt="image-20210720151020750" style="zoom:25%;" />
</center>

- Time sequence

<img src="note_04.assets/image-20210720151609071.png" alt="image-20210720151609071" style="zoom:33%;" />

- **How to find the correct out put length ?**
<center class="half">
<img src="note_04.assets/image-20210720151942381.png" alt="image-20210720151942381" style="zoom:25%;" /><img src="note_04.assets/image-20210720152021937.png" alt="image-20210720152021937" style="zoom:26%;" />
</center>

- - -->output:"End"

### Decoder Non-autoregressive (NAT)

<img src="note_04.assets/image-20210720152819234.png" alt="image-20210720152819234" style="zoom:50%;" />

- How to end ?
  - Another predictor
  - Output a very long sequence
- Advantage: parallel, fast



### Encoder-Decoder

<img src="note_04.assets/image-20210720153105211.png" alt="image-20210720153105211" style="zoom: 33%;" />

<img src="note_04.assets/image-20210720153200413.png" alt="image-20210720153200413" style="zoom:50%;" />

- **Cross attention**

- <img src="note_04.assets/image-20210720153403506.png" alt="image-20210720153403506" style="zoom: 50%;" />

- <img src="note_04.assets/image-20210720153512273.png" alt="image-20210720153512273" style="zoom:33%;" />

- <img src="note_04.assets/image-20210720153818783.png" alt="image-20210720153818783" style="zoom:33%;" />

- > 2005.08081



### Training

<img src="note_04.assets/image-20210720154106822.png" alt="image-20210720154106822" style="zoom:33%;" />

- output--real data 
  - min{cross entropy}
    - don't forget "End"
  - like classification

<img src="note_04.assets/image-20210720154514231.png" alt="image-20210720154514231" style="zoom: 33%;" />

- Teacher Forcing

- Tips:
  - Copy Mechanisum
    
    - Chat-bot
    - Summarization
    
    <center class="half">
    	<img src="note_04.assets/image-20210720154807407.png" alt="image-20210720154807407" style="zoom:26%;" /><img src="note_04.assets/image-20210720154859387.png" alt="image-20210720154859387" style="zoom:25%;" />
    </center>

<img src="note_04.assets/image-20210720155338831.png" alt="image-20210720155338831" style="zoom:33%;" />

- ### Guided Attention

  - TTS as example

  - <img src="note_04.assets/image-20210720155751809.png" alt="image-20210720155751809" style="zoom:33%;" />

  - Add prior knowledge: left to right

    - Monotonic Attention
    - Locatoin-aware attention

  - Beam search

    -  heuristic algorithm
    - <img src="note_04.assets/image-20210720160432036.png" alt="image-20210720160432036" style="zoom:33%;" />
    - <img src="note_04.assets/image-20210720160625014.png" alt="image-20210720160625014" style="zoom:33%;" />
    - TTS: Decoder should add noise **in testing**
      - see more possibility
      - more robust

  - <img src="note_04.assets/image-20210720161030865.png" alt="image-20210720161030865" style="zoom:33%;" />

  - testing: BLEU

  - training: Cross entropy

  - >  <img src="note_04.assets/image-20210720161246491.png" alt="image-20210720161246491" style="zoom: 50%;" />
    >
    > 1511.06732

- Exposure bais
- <img src="note_04.assets/image-20210720161446905.png" alt="image-20210720161446905" style="zoom:33%;" />
- After groud truth training, and when in tesing the output may wrong; 
  - **Why not using data with noise in training ?**
  - <img src="note_04.assets/image-20210720161744236.png" alt="image-20210720161744236" style="zoom:33%;" />
  - Scheduled Sampling



















