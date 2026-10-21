<div align="center">

# A Large Language Model (LLM) Approach to COVID-19 Fake News Detection

**Muhammad Arif · Samah Fodeh-Jarad · Elyas Irankhah · Uroosa Fatima · Lama Ayash · Sreeraj Ramachandran**

Yale School of Medicine

[![Paper](https://img.shields.io/badge/Paper-PDF-4f46e5)](A%20Large%20Language%20Model%20LLM%20Approach%20to%20COVID-19%20Fake%20News%20Detection.pdf)
[![Project page](https://img.shields.io/badge/Project-Page-0ea5e9)](https://marif561.github.io/LLM-COVID-19/)
![Task](https://img.shields.io/badge/Task-Fake%20news%20detection-10b981)
![Best accuracy](https://img.shields.io/badge/GPT--2%20accuracy-96.31%25-f43f5e)

</div>

---

## Overview

We classify COVID-19 tweets as **real** or **fake**. The study compares fine-tuned transformer models with large language models (LLMs), then applies six fusion and optimization methods to combine their predictions.

**Pipeline:** collect tweets → clean text → fine-tune 4 transformers + 3 LLMs → fuse predictions (6 methods) → evaluate.

## Dataset

| | |
|---|---|
| **Source** | COVID-19 English Tweets (public) |
| **Size** | 6,420 tweets — 3,360 real, 3,060 fake |
| **Columns** | `Tweets` (text), `Labels` (real / fake) |
| **Split** | 70% train · 10% validation · 20% test |
| **Balancing** | Not needed — classes are near-balanced |

**Preprocessing:** removed URLs, special tags and numbers; normalised whitespace; lowercased text.

## Models

| Family | Models |
|---|---|
| Transfer-learning transformers | BERT-base, ALBERT-base, XLM-RoBERTa-base, DistilBERT |
| Large language models | GPT-2, XLNet, T5 |

**Fusion / optimization methods:** weighted fusion, particle swarm optimization (PSO) fusion, Nelder–Mead, Powell's method, BFGS, and trust-region constrained optimization.

## Results

GPT-2 was the best single model on the test set.

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| **GPT-2** | **0.9631** | **0.9612** | **0.9610** | **0.9600** |

Full results for every model and fusion method (Tables II–V) and the confusion-matrix heatmaps are in the [paper](A%20Large%20Language%20Model%20LLM%20Approach%20to%20COVID-19%20Fake%20News%20Detection.pdf).

**Evaluation metrics:** accuracy, precision, recall, F1-score and confusion matrices.

## Repository contents

| File | Description |
|---|---|
| `A Large Language Model LLM Approach to COVID-19 Fake News Detection.pdf` | Full paper |
| `index.html` | Project page (served via GitHub Pages) |
| `CITATION.cff` | Citation metadata — enables GitHub's "Cite this repository" button |
| `README.md` | This file |

Training scripts and analysis notebooks will be added to this repository.

## Citation

If you use this work, please cite:

```bibtex
@misc{arif2026llmcovid,
  title  = {A Large Language Model (LLM) Approach to COVID-19 Fake News Detection},
  author = {Arif, Muhammad and Fodeh-Jarad, Samah and Irankhah, Elyas and
            Fatima, Uroosa and Ayash, Lama and Ramachandran, Sreeraj},
  note   = {Yale School of Medicine}
}
```

## Contact

Muhammad Arif — [GitHub @marif561](https://github.com/marif561) · [LinkedIn](https://www.linkedin.com/in/muhammadarif1906/)
