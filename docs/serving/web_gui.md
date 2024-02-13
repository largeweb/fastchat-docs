---
sidebar_position: 1
---

# Serving with Web GUI

To serve your models using FastChat's web user interface (UI), be sure to have a working controller, model worker(s), and web server.

Here are the commands to follow in your terminal:

## Launch the Controller

This controller manages distributed workers.

```bash
python3 -m fastchat.serve.controller
```

## Launch the Model Worker(s)

```bash
python3 -m fastchat.serve.model_worker --model-path lmsys/vicuna-7b-v1.5
```

Wait until the process finishes loading the model, and you see "Uvicorn running on ...". The model worker will register itself with the controller.

Ensure your model worker is connected to the controller correctly by sending a test message:

```bash
python3 -m fastchat.serve.test_message --model-name vicuna-7b-v1.5
```

## Launch Gradio Web Server

This server displays the user interface that your users will interact with.

```bash
python3 -m fastchat.serve.gradio_web_server
```

By following these steps, you'll be able to serve your models with FastChat's web UI. Open your browser and start chatting with the models. If the models fail to appear, try rebooting the Gradio web server.
