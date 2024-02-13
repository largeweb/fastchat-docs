---
sidebar_position: 3
---

# FSDP Optimization Solutions

FastChat relies on the Fully Sharded Data Parallelism (FSDP) technique to distribute model training across multiple GPUs. However, some users may experience out-of-memory issues due to FSDP's memory management during training.

The following tips can help you optimize FSDP and resolve such issues:

1. Consider reducing the global batch size or using a smaller context length which will reduce memory consumption.
2. Use a reduced precision (e.g. mixed precision training or lower bit precision) to decrease memory requirements.
3. Use [Megatron](https://github.com/NVIDIA/Megatron-LM) or model parallelism to distribute model components across multiple GPUs and aggregate memory.
4. Make sure all the GPUs involved have compatible or equal memory capacities. Uneven memory capacity can lead to an inefficient memory distribution strategy.

For more insights on memory management and best practices with FastChat, see [Managing Memory](/docs/inference/memory_management.md) and [Troubleshooting Memory Issues](/docs/troubleshooting/memory_issues.md).
