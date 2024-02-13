---
sidebar_position: 2
---

# Memory Management for Inference

This guide will provide you with tips and techniques for managing memory usage during inference with FastChat.

## Not Enough Memory

If you do not have enough memory, you can enable 8-bit compression by adding `--load-8bit` to the commands. This can reduce memory usage by around half, with slightly degraded model quality. It is compatible with the CPU, GPU, and Metal backend.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --load-8bit
```

### CPU Offloading

In addition to 8-bit compression, you can add `--cpu-offloading` to offload weights that don't fit on your GPU onto the CPU memory. This requires 8-bit compression to be enabled and the `bitsandbytes` package to be installed, which is only available on Linux operating systems.

For more information on memory management during inference, refer to the [Troubleshooting](/docs/troubleshooting/memory_issues.md) section.
