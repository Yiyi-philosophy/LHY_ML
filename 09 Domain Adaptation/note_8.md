# Domain Adaptation

## Domain shift

<img src="note_8.assets/image-20210924113734104.png" alt="image-20210924113734104" style="zoom:50%;" />

- Domain adaptation
  - A kind of **Transfer learning** 

<img src="note_8.assets/image-20210924114020506.png" alt="image-20210924114020506" style="zoom:50%;" />

- Different
  - **Kind**
  - Distribution
  - Map

### Case1: Target is little but labeled

<img src="note_8.assets/image-20210924114158521.png" alt="image-20210924114158521" style="zoom:50%;" />

- Training on source data and fine-tune
  - Careful about overfitting

### Case2: Target is large amountof unlabeled data

<img src="note_8.assets/image-20210924114511529.png" alt="image-20210924114511529" style="zoom:50%;" />

- Basic: **Feature Extractor**  

<img src="note_8.assets/image-20210924114606627.png" alt="image-20210924114606627" style="zoom:50%;" />

- Divide the former network layer as "**Feature Extractor** "
  - Expect the middle output will **"filt"** the "color"

<img src="note_8.assets/image-20210924114843664.png" alt="image-20210924114843664" style="zoom:50%;" />

- like **GAN** 

<img src="note_8.assets/image-20210925161819766.png" alt="image-20210925161819766" style="zoom:50%;" />

<img src="note_8.assets/image-20210925162131078.png" alt="image-20210925162131078" style="zoom:50%;" />
$$
\theta_f^*=\underset{\theta_f}{\min}(L-L_d) \\
\theta_p^*=\underset{\theta_p}{\min}(L) \\
\theta_d^*=\underset{\theta_d}{\min}(L_d)
$$
<img src="note_8.assets/image-20210925162421207.png" alt="image-20210925162421207" style="zoom:50%;" />

### limitation

<center class="half">
    <img src="note_8.assets/image-20210925162546637.png" alt="image-20210925162546637" style="zoom:33%;" /><img src="note_8.assets/image-20210925162619220.png" alt="image-20210925162619220" style="zoom:33%;" />
</center>

 

<img src="note_8.assets/image-20210925162750464.png" alt="image-20210925162750464" style="zoom:50%;" />

- boundary

<img src="note_8.assets/image-20210925162853970.png" alt="image-20210925162853970" style="zoom:50%;" />



### Outlook

$$
\text{Maybe } 
\begin{cases}
& S_{Target} \subseteq S_{Sourse}\\
& S_{Target} \supseteq S_{Sourse}\\
& S_{Target} \cap S_{Sourse} \ne \emptyset
\end{cases}
$$

<img src="note_8.assets/image-20210925164353077.png" alt="image-20210925164353077" style="zoom:50%;" />

### Little & Unlabel: TTT



<img src="note_8.assets/image-20210925164934885.png" alt="image-20210925164934885" style="zoom:50%;" />

## Domain Generalizayion

<img src="note_8.assets/image-20210925165129612.png" alt="image-20210925165129612" style="zoom:50%;" />

<img src="note_8.assets/image-20210925165207701.png" alt="image-20210925165207701" style="zoom:50%;" />

 



