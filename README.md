# Deep Learning Training

A personal learning repository documenting the fundamentals of deep learning with PyTorch — from manual implementation of core concepts to structured model building with PyTorch's API.

---

## Purpose

This repository is built for **understanding, not shortcuts.**  
Each notebook is written to answer the question: *"What is actually happening under the hood?"*

The progression moves from raw, manual implementations to PyTorch's high-level abstractions — making the gap between the two visible and understandable.

---

## Repository Structure

```
Deep-Learning-Training/
│
├── dataset/
│   ├── 06-study_hours_grades.csv       # Regression dataset (study hours → grade)
│   └── 08-email_classification_svm.csv # Binary classification dataset (email features)
│
├── PyTorchTrainingSteps.ipynb          # Manual training loop from scratch
├── PyTorchTrainingStructural.ipynb     # Structured model with nn.Module & nn.Linear
├── LinearandNonlinearDatas.ipynb       # Linear & non-linear classification (2 features)
│
├── .gitignore
└── README.md
```

---

## Notebooks

### 1. `PyTorchTrainingSteps.ipynb` — Manual Training Loop

**Dataset:** `06-study_hours_grades.csv`

The goal here is to understand every step of the training process without relying on PyTorch's built-in layers. No activation functions, no `nn.Module` — just the raw mechanics.

**Covers:**
- Forward pass (manual computation)
- Loss calculation
- Backward pass (`loss.backward()`)
- Parameter update (optimizer step)
- Training loop structure

> **Why manual?** Writing `nn.Linear` is easy. Knowing what it *does* — weight matrix multiplication, gradient flow — requires building it yourself first.

---

### 2. `PyTorchTrainingStructural.ipynb` — Structured PyTorch Model

**Dataset:** `06-study_hours_grades.csv`

After understanding the steps manually, this notebook rebuilds the same process using PyTorch's standard structure. The focus is on *how* PyTorch organizes models, not just that it does.

**Covers:**
- `nn.Module` subclassing
- `nn.Linear` usage (and what it replaces from the manual version)
- `__init__` and `forward` method patterns
- Clean training loop with PyTorch conventions

---

### 3. `LinearandNonlinearDatas.ipynb` — Classification with 2 Features

**Dataset:** `08-email_classification_svm.csv`

A classification problem with two input features — designed to make the decision boundary concept tangible.

**Covers:**
- Binary classification setup
- 2-feature input handling
- Linear vs. non-linear data behavior
- Loss and accuracy tracking

---

## Learning Progression

```
Manual implementation          →      PyTorch API
(PyTorchTrainingSteps)                (PyTorchTrainingStructural)
         ↓
Classification task with real dataset
(LinearandNonlinearDatas)
```

---

## Setup

```bash
git clone https://github.com/IbrahimEmreYildiz/Deep-Learning-Training.git
cd Deep-Learning-Training

python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # macOS/Linux

pip install torch torchvision numpy pandas matplotlib jupyter
jupyter notebook
```

> CUDA kullanıyorsan PyTorch'u [resmi siteden](https://pytorch.org/get-started/locally/) CUDA versiyonuna göre kur.

---

## Tech Stack

| Tool | Version |
|---|---|
| Python | 3.10+ |
| PyTorch | 2.x |
| NumPy | latest |
| Pandas | latest |
| Matplotlib | latest |
| Jupyter Notebook | latest |

---

## Author

**İbrahim Emre Yıldız**  
Computer Engineering Student — Çukurova University  
[GitHub](https://github.com/IbrahimEmreYildiz) · [LinkedIn](https://linkedin.com/in/ibrahimemreyildiz)