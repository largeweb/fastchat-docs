---
sidebar_position: 2
---

# Model Compression and Acceleration Techniques

FastChat supports various model compression and acceleration techniques to enhance performance on limited hardware resources. Some of these techniques include:

1. 8-bit compression: Reduce memory usage by approximately half with slightly degraded model quality. Compatible with CPU, GPU, and Metal backend. Activate with the `--load-8bit` flag during inference.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --load-8bit
```

2. ExLlama V2: Optimized inference for LLMs. Read more in the [ExLlama V2 documentation](/docs/advanced-features/exllama_v2.md)
3. GPTQ 4-bit inference: See the [GPTQ for LLaMa Guide](/docs/advanced-features/gptq.md).
4. AWQ 4-bit inference: Works with `mit-han-lab/llm-awq`. Read more in the [AWQ documentation](/docs/advanced-features/awq.md).
5. MLC LLM: Deploy Vicuna natively on phones, consumer GPUs, and web browsers using the TVM Unity compiler, which supports Vulkan, Metal, CUDA, and WebGPU.

For additional information on model compression, acceleration, and supported platforms, refer to the [Supported Platforms](/docs/advanced-features/supported_platforms.md) section.
