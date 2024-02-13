---
sidebar_position: 2
---

# Setting up a Distributed Multi-Model Serving System

FastChat enables you to serve multiple models simultaneously or establish a distributed model serving system to increase throughput for a single model. Use these instructions to set up a distributed multi-model serving system.

1. Register multiple model workers to a single controller. This method can be used for serving a single model with higher throughput or serving multiple models at the same time. Allocate different GPUs and ports for different model workers.

Example:

```bash
# worker 0
CUDA_VISIBLE_DEVICES=0 python3 -m fastchat.serve.model_worker --model-path lmsys/vicuna-7b-v1.5 --controller http://localhost:21001 --port 31000 --worker http://localhost:31000
# worker 1
CUDA_VISIBLE_DEVICES=1 python3 -m fastchat.serve.model_worker --model-path lmsys/fastchat-t5-3b-v1.0 --controller http://localhost:21001 --port 31001 --worker http://localhost:31001
```

2. Launch a multi-tab Gradio server, which includes Chatbot Arena tabs.

```bash
python3 -m fastchat.serve.gradio_web_server_multi
```

By following these instructions, you'll create a distributed multi-model serving system with FastChat.
