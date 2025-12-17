<div align="center">

<!-- Replace with your own banner/logo path -->
<img src="banner.svg" alt="Regressive Reasoning Logo">

*Brand Logo Classification (10 Classes) — Trained & Evaluated on HiPerGator*

<!-- Badges (edit links as needed) -->
![Python](https://img.shields.io/badge/python-3.10-orange)
[![Framework](https://img.shields.io/badge/framework-TensorFlow%202.7.0-FF6F00?logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
<a href="EEL5840_Project_Report.pdf">
  <img alt="Project Report PDF" src="https://img.shields.io/badge/Project%20Report-PDF-red?logo=adobeacrobatreader&logoColor=white">
</a>

</div>

---

### 🧠 Overview

**Regressive Reasoning** is a computer vision project for **classifying 10 brand logos** using a TensorFlow-based pipeline developed on the **HiPerGator** supercomputing environment.  
The model predicts an integer label corresponding to a brand:

- **0**: Nike  
- **1**: Adidas  
- **2**: Ford  
- **3**: Honda  
- **4**: General Mills  
- **5**: Unilever  
- **6**: McDonald's  
- **7**: KFC  
- **8**: Gator  
- **9**: 3M  


## Quick Start

This project was run on HiPerGator (UF's supercomputer) using the **Tensorflow-2.7.0** kernel. Below is the minimal setup to reproduce.

### (1) 🧰 Dependencies

Tensorflow-2.7.0 kernel library versions:

- Numpy **1.22.3**
- Tensorflow **2.7.0**
- sklearn **0.24.2**
- Matplotlib

### (2) 📦 Files to Place in One Folder

Upload these into your HiPerGator storage:

- `train.ipynb`
- `test.ipynb`
- `efficientnetv2-s.tar.gz` (download: https://drive.google.com/file/d/1JoS2xVaANyANP1EN6pCxgo1rcBlN2XRz/view?usp=sharing)
- dataset folder (download: https://drive.google.com/drive/folders/1nr8YHapqXVqLthvaC2O4IZgH1-79XQ_P?usp=sharing)
- test arrays (examples):
  - `easy_data.npy`
  - `easy_labels.npy`

Example directory layout:

- Folder  
  - `train.ipynb`  
  - `test.ipynb`  
  - `efficientnetv2-s.tar.gz`  
  - `easy_data.npy`  
  - `easy_labels.npy`  

### (3) ⚙️ Uncompress the Model

Run on the HiPerGator terminal:

```bash
tar -xvzf efficientnetv2-s.tar.gz
```

Make sure the extracted `efficientnetv2-s/` folder sits alongside the notebooks and data files.

### (4) ▶️ Run the Notebooks

Launch Jupyter on HiPerGator using the **Tensorflow-2.7.0** kernel and run:

- `train.ipynb` for training
- `test.ipynb` for evaluation


## 📊 Confusion Matrix

![Confusion Matrix](figs/confusion_matrix.png)


## 🧭 Usage Notes

- Keep **only one active kernel** at a time to avoid crashes.
- **Easy dataset:** In `test.ipynb`, use the `test` function and update:
  - `data_path`
  - `labels_path`
- **Hard dataset (extra credit):** Use `test_hard` and update:
  - `hard_data_path`
  - `hard_labels_path`
  - Uncomment the hard data loading functions when running.

## 🛣️ Roadmap

1. Improve handling/reporting of unclassifiable objects (label as **-1**).  
2. Increase accuracy with image augmentation.  
3. Compare additional model architectures.  


## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.


## 👥 Authors

- Matheus Kunzler Maldaner — [GitHub](https://github.com/matheusmaldaner)  
- Pedro Moss — [GitHub](https://github.com/p4moss12)  
- Ruo Chen — chenruo@ufl.edu  

