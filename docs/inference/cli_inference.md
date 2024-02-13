---
sidebar_position: 1
---

# Inference with Command Line Interface

This guide will teach you how to perform inference using FastChat's command line interface (CLI) to chat with your models.

## Supported Models

FastChat supports a wide range of models, including LLama 2, Vicuna, Alpaca, Baize, ChatGLM, Dolly, Falcon, FastChat-T5, GPT4ALL, Guanaco, MTP, OpenAssistant, OpenChat, RedPajama, StableLM, WizardLM, xDAN-AI, and more. See the complete list of supported models and instructions to add a new model in the [supported models documentation](/docs/inference/cli_inference.md).

### Single GPU

This command requires around 14 GB of GPU memory for Vicuna-7B and 28 GB of GPU memory for Vicuna-13B. If you do not have enough memory, refer to the "Not Enough Memory" section. `--model-path` can be a local folder or a Hugging Face repository name.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5
```

### Multiple GPUs

You can use model parallelism to aggregate GPU memory from multiple GPUs on the same machine.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --num-gpus 2
```

### CPU Only

This runs on the CPU only and does not require GPU. It requires around 30 GB of CPU memory for Vicuna-7B and around 60 GB of CPU memory for Vicuna-13B.

```bash
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-7b-v1.5 --device cpu
```

For more information on GPU optimization, memory management, and other platforms, refer to the [Advanced Features](/docs/advanced-features/gpu_optimizations.md) section.
