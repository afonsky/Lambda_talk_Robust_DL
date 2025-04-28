---
level: 2
zoom: 1.1
---

# Conclusions

* LLMs leverage deep learning architectures, specifically transformer-based models, enabling sophisticated natural language understanding and generation

* Significant improvements are driven by scaling laws, pre-training on large, diverse corpora, and fine-tuning strategies for domain-specific tasks

* Evaluation metrics such as perplexity, BLEU, and human judgment remain critical for benchmarking performance and guiding model development

* Challenges persist in interpretability, bias mitigation, efficient inference, and ensuring robustness against adversarial inputs

* Ongoing research aims to enhance alignment with human values, improve computational efficiency, and extend LLM applications across interdisciplinary domains

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

---

# Position Model vs Training Sample Size

<br>
<div class="grid grid-cols-[2fr_2fr] gap-1">
<div>
<figure>
    <img src="/Energy_A_132_32k_bins_bar_nobar.svg" style="width: 455px !important;">
</figure>
</div>
<div>
<figure>
    <img src="/Energy_B_132_32k_bins_bar_nobar.svg" style="width: 455px !important;">
</figure>
</div>
</div>
