---
sidebar_position: 2
---

# Memory Issues and Their Solutions

If you encounter memory-related issues with FastChat, you can use the following techniques to resolve them:

1. Enable 8-bit compression: Add the `--load-8bit` flag during inference to enable 8-bit compression, which can reduce memory usage by around half with slightly degraded model quality.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --load-8bit
```

2. Use CPU offloading: Combine CPU offloading with 8-bit compression by adding the `--cpu-offloading` flag to the commands. This requires the `bitsandbytes` package, which is available only on Linux operating systems.

For additional guidance on troubleshooting memory issues, refer to the [Memory Management Guide](/docs/inference/memory_management.md).
