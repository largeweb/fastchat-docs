---
sidebar_position: 2
---

# Gradient Checkpointing for Out-of-Memory During Model Saving

Gradient checkpointing is an efficient technique to reduce memory usage during model training and saving. It trades computation for memory by recomputing some values instead of storing them.

## How to Use Gradient Checkpointing

To use gradient checkpointing with FastChat, add the `--gradient_checkpointing` flag to the training command:

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --gradient_checkpointing
```

Using gradient checkpointing can significantly reduce memory usage during model saving, making it easier to handle large models on systems with limited memory.

For more details on memory management and related techniques in FastChat, see [Memory Management](/docs/inference/memory_management.md) and [Troubleshooting Memory Issues](/docs/troubleshooting/memory_issues.md).
