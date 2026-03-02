# ObfusQAte: A Proposed Framework to Evaluate LLM Robustness on Obfuscated Factual Question Answering
![](./obfusfinalfinalfinal.png)
## 📌 Overview
**ObfusQAte** is a novel obfuscation technique and benchmark framework designed to stress-test LLMs on *semantically equivalent but linguistically obfuscated* variants of factual questions. While LLMs excel at direct factual recall, our study reveals a drastic degradation in performance when questions are rephrased to require genuine reasoning rather than surface-level pattern matching.

> A simple question like *"Who invented the telephone?"* becomes *"Name the ingenious person who gifted us with the ability to converse audibly across long distances?"* — the LLM struggles despite the answer being the same.

**Dataset (ObfusQA) Link:** [https://huggingface.co/datasets/Adignite/ObfusQA](https://huggingface.co/datasets/Adignite/ObfusQA)


---

## 📊 Dataset: ObfusQA

| Property | Value |
|---|---|
| Total Questions | **1,024** |
| Base Questions | 256 |
| Obfuscated Variants per Question | 3 (NEI, DI, CO) |
| Source | TriviaQA + GKToday |
| Generation Model | Gemini 2.0 Flash (temp=0.75) |
| Annotation | Human-in-the-loop (7 annotators, κ=0.862) |
| Language | English |

## 🤖 Benchmark Results

We evaluated **7 state-of-the-art LLMs** under Zero-Shot, Few-Shot, and Chain-of-Thought (CoT) prompting using Exact Match (EM) accuracy.

### Main Results (EM Accuracy %)

| Model | Base | NEI | DI | CO |
|---|---|---|---|---|
| **GPT-4o** | 84.38 | 55.86 | 32.42 | 38.67 |
| **Claude 3.5 Sonnet** | 78.91 | 54.30 | 38.28 | 39.45 |
| **LLaMA 3.3 70B** | 75.69 | 41.41 | 30.08 | 35.55 |
| **GPT-4o mini** | 61.72 | 36.72 | 26.17 | 30.08 |
| **Gemini Flash 2.0** | 78.91 | 50.78 | 33.59 | 35.55 |
| **DeepSeek R1** | 82.15 | 58.92 | 40.78 | 42.33 |
| **o3-mini** | 72.45 | 45.20 | 36.90 | 36.70 |

> CoT prompting improves performance by **8–12%** on average. Few-shot provides only marginal gains (~2–4%).

### Average Performance Degradation from Base Question

| Model | Avg. Drop |
|---|---|
| GPT-4o mini | ~57% |
| GPT-4o | ~56% |
| Gemini Flash 2.0 | ~55% |
| DeepSeek R1 | ~50% |
| Claude 3.5 Sonnet | ~49% |
| LLaMA 3.3 70B | ~44% |

### Citations

If you use ObfusQAte pls cite ~

```
@inproceedings{obfusqate2026,
  title={ObfusQAte: A Benchmark for Evaluating Robustness to Question Obfuscation},
  author={Ghosh, Shubhra and Borah, Abhilekh and Guru, Aditya Kumar and Ghosh, Kripabandhu},
  booktitle={Proceedings of the Language Resources and Evaluation Conference (LREC)},
  year={2026}
}
```

<p align="center">
  <i>ObfusQAte — because real intelligence shouldn't need the answer spelled out.</i>
</p>
