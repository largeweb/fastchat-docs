---
sidebar_position: 3
---

# Advanced Features for Model Serving

FastChat provides advanced serving features to better serve models with various system configurations and requirements.

1. Use model parallelism to improve serving performance. This guide explains how to use model parallelism to aggregate GPU memory from multiple GPUs on the same machine.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --num-gpus 2
```

For additional details on model serving, including instructions on setting up distributed systems and using third-party user interfaces (UIs), this is the section for you.
