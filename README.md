
# 🧠 Medical Deepfake Detection in Brain MRI

This project is based on the research paper **“Integrating Fourier Analysis and Deep Learning for Robust Detection of Deep Fake Brain Magnetic Resonance Images”** published in *Pattern Recognition Letters (2026)*. The work addresses the growing risk of synthetic medical images generated using GANs and diffusion models, which can mislead clinical diagnosis. The proposed framework detects fake brain MRI images by combining domain-specific handcrafted features with deep learning representations, achieving highly reliable performance. Experimental results show that Fourier-based features capture frequency inconsistencies introduced by synthetic generation and achieve up to **99.8% accuracy**, making them the most effective feature representation ([CompuData Sciences][1]).

The methodology integrates multiple feature extraction techniques such as Error Level Analysis (ELA), wavelet transforms, gradient maps, and Fourier transforms, along with deep embeddings from a pretrained VGG19 model. These features are evaluated using Support Vector Machines (SVM), MobileNetV2 (CNN), and K-Means clustering. While supervised models achieve near-perfect classification, unsupervised methods fail due to overlapping feature distributions between real and fake images. The framework demonstrates that combining domain-aware features with supervised learning provides a robust solution for medical deepfake detection.

---

## 🧪 Dataset Overview

<img width="589" height="266" alt="Screenshot 2026-04-16 112300" src="https://github.com/user-attachments/assets/80266b77-5a83-4199-af00-bb5ad0671774" />


The dataset consists of both real MRI scans and synthetically generated images, including partially tampered images (lesion insertion) and fully generated images using GANs and diffusion models. This diverse dataset enables robust evaluation across multiple fake generation techniques.

---

## 🧠 Methodology

<img width="819" height="373" alt="Screenshot 2026-04-16 111334" src="https://github.com/user-attachments/assets/38a3b8de-d88f-4ba8-abb8-4480eab7e726" />

The pipeline begins with MRI images and extracts multiple feature representations, followed by classification using machine learning and deep learning models. The framework combines both spatial and frequency-domain analysis to improve detection accuracy.

---

## 📊 Results

<img width="1075" height="538" alt="Screenshot 2026-04-16 111844" src="https://github.com/user-attachments/assets/40212250-0ffc-44f3-b534-fda11725c035" />


The classification results clearly show that **Fourier features outperform all other feature types**, achieving near-perfect accuracy across datasets. CNN models perform better with larger data, while SVM combined with VGG embeddings performs strongly even with limited data.

---

## 📉 Feature Space Visualization

<img width="1184" height="373" alt="Screenshot 2026-04-16 111622" src="https://github.com/user-attachments/assets/55a09881-e6a4-446e-a904-ad06ca2f23d7" />


The t-SNE visualization shows that real and fake images are not clearly separable in an unsupervised setting, explaining the poor performance of K-Means clustering. In contrast, supervised models learn strong decision boundaries for classification.

---

## 🔗 Links

* 📄 Paper (ScienceDirect): https://www.sciencedirect.com/science/article/pii/S0167865526001066
* 📘 PDF Version: https://cds.iisc.ac.in/faculty/yalavarthy/Ravi_PRL_2026.pdf

---

## 📚 Citation

```bibtex
@article{RAVI202641,
title = {Integrating Fourier analysis and deep learning for robust detection of deep fake brain magnetic resonance images},
journal = {Pattern Recognition Letters},
volume = {204},
pages = {41-47},
year = {2026},
issn = {0167-8655},
doi = {https://doi.org/10.1016/j.patrec.2026.03.016},
url = {https://www.sciencedirect.com/science/article/pii/S0167865526001066},
author = {Vaishnavi Ravi and Yogesh K. Sahu and Prabhas R. Onteru and Parag Dutta and Dhanshree Warokar and Padma Murali and Rajesh Katta and Ambedkar Dukkipati and Phaneendra K. Yalavarthy},

}
```

[1]: https://cds.iisc.ac.in/faculty/yalavarthy/Ravi_PRL_2026.pdf?utm_source=chatgpt.com "Integrating Fourier Analysis and Deep Learning for Robust ..."
