## Arabic OCR Fine-Tuning with Qwen 3.5-2B

This project fine-tunes **Qwen 3.5-2B** with **LoRA** for **Arabic OCR** using a **20k-sample subset** of `mssqpi/Arabic-OCR-Dataset`, while the full Hugging Face dataset contains about **2.16M labeled image-text pairs**.

### Dataset
- Each sample provides an **image** and its ground-truth **text**, making it suitable for supervised OCR training and evaluation.
- Dataset mainly contains **short Arabic text snippets**, with viewer statistics showing image widths around **29–222 px** and text lengths around **7–10 characters**.
  
### Finetuning with Low-Rank Adaptation (LoRA) technique
LoRA fine-tuning adapts Qwen 3.5-2B to Arabic OCR by learning small low-rank updates to the pretrained model weights, enabling efficient training with much lower compute and memory cost.

### Evaluation
- Evaluation was performed on a **held-out split** using OCR-focused metrics, mainly **Character Error Rate (CER)**.
- The model achieved about **0.32 CER**.
