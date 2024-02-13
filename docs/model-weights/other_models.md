---
sidebar_position: 2
---

# Other Models

Besides Vicuna, FastChat also supports two additional models: LongChat and FastChat-T5. You can use the commands below to chat with them. The weights will be downloaded automatically from Hugging Face repositories.

## Available Models

| Model          | Chat Command                                                            | Hugging Face Repo         |
| -------------- | ----------------------------------------------------------------------- | ------------------------- |
| LongChat-7B    | `python3 -m fastchat.serve.cli --model-path lmsys/longchat-7b-32k-v1.5` | lmsys/longchat-7b-32k     |
| FastChat-T5-3B | `python3 -m fastchat.serve.cli --model-path lmsys/fastchat-t5-3b-v1.0`  | lmsys/fastchat-t5-3b-v1.0 |
