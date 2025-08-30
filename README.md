

# Fine-Tune Gemma 3-1B For Text-to-SQL Tasks

Supervised fine-tuning of the open-source Google model **Gemma 3-1B** for the Text-to-SQL task, executed locally on a T4 GPU using PEFT with **LoRA** to fit resource constraints. The notebook includes a before/after performance comparison of the model on Text-to-SQL prompts.

## Overview

- Goal: adapt Gemma 3-1B to convert natural-language questions into SQL queries via supervised fine-tuning.[1][2][3]
- Hardware: single NVIDIA T4 GPU; PEFT (LoRA) applied to enable training within limited memory.[2][3]
- Outcome: side-by-side evaluation in the notebook comparing base vs. fine-tuned model behavior.[4][1]

## Method

- Base model: Gemma 3-1B.[5]
- Training approach: Supervised fine-tuning with Parameter-Efficient Fine-Tuning (PEFT) using LoRA adapters.[3][2]
- Rationale: LoRA reduces trainable parameters by injecting low-rank adapters, enabling efficient tuning on small GPUs like T4.[2][3]
