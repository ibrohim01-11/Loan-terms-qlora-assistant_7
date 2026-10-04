# Loan Terms QLoRA Assistant

A parameter-efficient (QLoRA) fine-tuned Qwen2.5-1.5B-Instruct model for grounded question answering over bank loan Terms & Conditions documents. The model is trained to cite its source document, refuse off-topic questions, and explicitly state when information is not present in the provided terms — behaviours the base instruction-tuned model does not reliably exhibit.

Companion code and data for the paper submitted to *Journal of Mathematical Models and Methods in Engineering (JMMME)*.

## Repository contents

- `loan_assistant_qlora_finetune.ipynb` — full training notebook (QLoRA fine-tuning, before/after evaluation, Gradio demo)
- `train.jsonl` / `eval.jsonl` — 45 training examples / 8 held-out evaluation examples
- `*.pdf` — five source bank loan Terms & Conditions documents (CIBC, CIMB, National Bank of Uzbekistan, South Indian Bank, Standard Chartered)

## Setup

Trained on a single NVIDIA Tesla T4 (Google Colab free tier), 4-bit NF4 quantization, LoRA rank 16, 4 epochs, ~140 seconds wall-clock training time.
