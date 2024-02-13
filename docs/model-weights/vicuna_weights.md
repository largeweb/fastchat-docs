---
sidebar_position: 1
---

# Vicuna Model Weights

Vicuna is based on Llama 2 and should be used under Llama's model license. You can use the commands below to start chatting. The weights will be automatically downloaded from Hugging Face repositories.

> **NOTE**: transformers>=4.31 is required for 16K versions.

## Available Model Sizes and Weights

| Size    | Chat Command                                                           | Hugging Face Repo         |
| ------- | ---------------------------------------------------------------------- | ------------------------- |
| 7B      | `python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5`      | lmsys/vicuna-7b-v1.5      |
| 7B-16k  | `python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5-16k`  | lmsys/vicuna-7b-v1.5-16k  |
| 13B     | `python3 -m fastchat.serve.cli --model-path lmsys/vicuna-13b-v1.5`     | lmsys/vicuna-13b-v1.5     |
| 13B-16k | `python3 -m fastchat.serve.cli --model-path lmsys/vicuna-13b-v1.5-16k` | lmsys/vicuna-13b-v1.5-16k |
| 33B     | `python3 -m fastchat.serve.cli --model-path lmsys/vicuna-33b-v1.3`     | lmsys/vicuna-33b-v1.3     |

See more command options and how to handle out-of-memory issues in the "Inference with Command Line Interface" section.
