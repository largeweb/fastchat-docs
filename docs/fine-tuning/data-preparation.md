---
sidebar_position: 1
---

# Preparing Data for Fine-Tuning

Before fine-tuning, ensure that your data is properly formatted and cleaned. FastChat's Vicuna models are fine-tuned on Llama 2 using approximately 125K user-shared conversations gathered from ShareGPT.com with public APIs. To achieve data quality, HTML content is converted back to Markdown, and inappropriate or low-quality samples are filtered out. Lengthy conversations are divided into smaller segments to fit within the model's maximum context length.
