# QLoRA Fine-Tuning for Persian Multiple-Choice Answering

This project fine-tunes an instruction-tuned LLM using QLoRA to answer Persian multiple-choice questions (4 options).  
The model is prompted to output **only a single digit**: 0, 1, 2, or 3.

## Project Structure
- `notebooks/` Training + evaluation notebook
- `data/questions.json` Evaluation dataset (Persian MCQs)
- `adapters/` QLoRA adapter weights 

## Method
- Base model: Qwen2.5 Instruct
- Training: Supervised fine-tuning (SFT) with PEFT
- Output constraint: strict single-digit answer (0–3)

## Results (Example)
- Base accuracy: 0.45 (9/20)
- Fine-tuned accuracy: 0.80 (16/20)

## Reproducibility
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
