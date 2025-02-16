# ObfusQAte

This repository provides the **ObfusQAte** framework for generating obfuscated question-answer pairs. It is intended for **research purposes** to study how well Large Language Models (LLMs) handle increasingly complex or obfuscated queries.

---

## Repository Structure


1. **ObfusQAte-Prompts/**  
   Contains three `.txt` files, each describing a different style of prompt:
   - `ObfusQAte-Prompts/Named Entity Indirection Prompt.txt` – The prompt template for Named-Entity Indirection (NEI).  
   - `ObfusQAte-Prompts/Distractor Indirection Prompt.txt` – The prompt template for Distractor Indirection (DI).  
   - `ObfusQAte-Prompts/Contextual Overload Prompt.txt` – The prompt template for Contextual Overload (CO).

2. **ObfusQAte-Dataset/**  
   Contains the **ObfusQA** dataset in CSV format, including the **base questions** and their **three obfuscated variants** (NEI, DI, CO).

---

## Usage

1. **Review the Prompt Files**  
   - Each `.txt` file provides instructions that can be used to generate obfuscated versions of a question.  
   - You can load these prompts into an LLM to replicate or extend the obfuscation process.

2. **Explore the Dataset**  
   - The `ObfusQAte-Dataset/ObfusQA.csv` file contains 1024 examples (base question + three obfuscated (NEI, DI and CO) variants.  
   - Each row represents a single question and its obfuscations, verified by human annotators.

3. **Research & Development**  
   - Use the dataset to evaluate how different LLMs handle obfuscated queries.  
   - Compare accuracy, robustness, and potential hallucinations across question types.

---

## License

This repository is **anonymized** for double-blind review. Usage is permitted for **non-commercial, research-oriented** purposes only.  
For inquiries about extended usage or collaboration, please contact the authors once anonymity is lifted.

---

## Citation

If you find **ObfusQAte** helpful in your research, please cite our paper (citation details will be provided after anonymity is lifted).

