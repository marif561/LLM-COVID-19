# A Large Language Model (LLM) Approach to COVID-19 Fake News Detection

Muhammad Arif, Samah Fodeh-Jarad, Elyas Irankhah, Uroosa Fatima, Lama Ayash, Sreeraj Ramachandran

📄 Paper: [`LLM_COVID19_Fake_News_Detection.pdf`](LLM_COVID19_Fake_News_Detection.pdf)

## Overview

We classify COVID-19 tweets as **real** or **fake**. The study compares pretrained transformer models with LLMs and applies six fusion/optimization methods to improve their predictions.

## Dataset

- **COVID-19 English Tweets** dataset (public): 6,420 tweets, of which 3,360 are real and 3,060 are fake
- Two columns: `Tweets` (text) and `Labels` (real/fake)
- Preprocessing: URLs, special tags and numbers removed, whitespace normalised, text lowercased
- Split: 70% train / 10% validation / 20% test (no class balancing needed)

## Models

| Type | Models |
|---|---|
| Transfer-learning transformers | BERT-base, ALBERT-base, XLM-RoBERTa-base, DistilBERT |
| Large language models | GPT-2, XLNet, T5 |

**Fusion / optimization methods:** weighted fusion, particle swarm optimization (PSO) fusion, Nelder–Mead, Powell's method, BFGS, and trust-region constrained optimization.

## Results

GPT-2 was the best single model on the test set:

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| GPT-2 | 0.9631 | 0.9612 | 0.9610 | 0.9600 |

Full results for every model and fusion method (Tables II–V) and the confusion-matrix heatmaps are in the paper.

## Evaluation

Accuracy, precision, recall, F1-score and confusion matrices.

## Citation

```bibtex
@misc{arif2026llmcovid,
  title  = {A Large Language Model (LLM) Approach to COVID-19 Fake News Detection},
  author = {Arif, Muhammad and Fodeh-Jarad, Samah and Irankhah, Elyas and Fatima, Uroosa and Ayash, Lama and Ramachandran, Sreeraj},
  note   = {Yale School of Medicine}
}
```
