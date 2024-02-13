---
sidebar_position: 1
---

# GPU Optimizations for FastChat

This guide provides tips and best practices for optimizing GPU performance with FastChat.

1. Use model parallelism to aggregate GPU memory from multiple GPUs on the same machine. This allows you to run models on systems with limited GPU memory. For example:

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --num-gpus 2
```

2. Balance memory allocation across multiple GPUs using the `--max-gpu-memory` flag. This helps in allocating more memory for activations, leading to better performance in longer context lengths or larger batch sizes. For example:

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --num-gpus 2 --max-gpu-memory 8GiB
```

For more GPU optimization tips, check out the [Advanced Features](/docs/advanced-features/gpu_optimizations.md) section.
