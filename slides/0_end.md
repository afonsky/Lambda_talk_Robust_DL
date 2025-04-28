---
level: 2
zoom: 1.1
---

# Conclusions

* We propose a procedure to measure the robustness of machine learning models

* We supplement such a procedure with a meta-algorithm for robust model selection

* The two robust models for two specific problems found using this method have the best convergence and the smallest loss variability among the $2\times6912$ models considered
	* Finding a robust model from a set of $6912$ models with different architectures and hyperparameters requires training $41567$ models and their instances, instead of training $345600$ models and their instances while considering an exhaustive search for the most robust model from the set
 * The models we found are more robust than the models selected by NAS from a similar search space
 * 
---
layout: end
hideInToc: true
---

---
layout: statement
---

## Thank you for the attention!

<br>
<br>

#### Happy to answer your questions by e-mail <a href="mailto:aboldyrev@hse.ru">aboldyrev@hse.ru</a> and via Telegram <a href="https://t.me/aboldyrev">@aboldyrev</a>

<PoweredBySlidev mt-10 />

---
layout: center
class: text-center
---

# Backup slides

---
zoom: 0.95
---

# Application of the ResNet-18 architecture

<center>
<figure>
    <img src="/ResNet-18.png" style="width: 405px !important;">
</figure>
</center>
<br>

<div class="grid grid-cols-[4fr_3fr] gap-10">
  <div>

* **Calo clusters** are considered **as images**
* The first layers of the [ResNet-18](https://arxiv.org/abs/1512.03385) are **adjusted**<br> to actual input dimensions 15x15
* The number of residual blocks is optimized
	* Model with 11M of trainable params
* Hyperparameters are selected using a grid search with cross-validation
</div>
<div>
<figure>
    <img src="/ResNet-18_results.png" style="width: 405px !important;">
</figure>
</div>
</div>

---

# Energy Model vs Training Sample Size

<br>
<div class="grid grid-cols-[2fr_2fr] gap-1">
<div>
<figure>
    <img src="/Energy_A_132_32k_bins_sum_nosum.svg" style="width: 455px !important;">
</figure>
</div>
<div>
<figure>
    <img src="/Energy_B_132_32k_bins_sum_nosum.svg" style="width: 455px !important;">
</figure>
</div>
</div>

* Boxplots of the losses for the energy reconstruction problem for Model 1 and Model 2 as a function of the training sample size for Dataset A (top) and Dataset B (bottom)
* Model 2 uses the sum of the energies in the cells transferred after the first convolution layer
* 50 instances of the corresponding model are used for each box plot

---

# Position Model vs Training Sample Size

<br>
<div class="grid grid-cols-[2fr_2fr] gap-1">
<div>
<figure>
    <img src="/Position_A_132_32k_bins_bar_nobar.svg" style="width: 455px !important;">
</figure>
</div>
<div>
<figure>
    <img src="/Position_B_132_32k_bins_bar_nobar.svg" style="width: 455px !important;">
</figure>
</div>
</div>

* Boxplots of the losses for the position reconstruction problem for Model 3 and Model 4 as a function of the training sample size for Dataset A (top) and Dataset B (bottom)
* Model 4 uses the barycenter position of the energy deposits after the first fully connected layer
* 50 instances of the corresponding model are used for each box plot

---

# Optimizer Paths for Different Initializations

<br>
<center>
<figure>
    <img src="/weights_pca_0_2_11_with_path_20250427_3.svg" style="width: 555px !important;">
</figure>
</center>
