---
sidebar_position: 4
---

# LangChain Integration

LangChain is an AI-powered translation service, and it can be integrated with FastChat to provide multilingual support for your chatbot. This section will guide you through the process of integrating LangChain with FastChat.

## Prerequisites

Ensure you have a LangChain API key. If you don't, sign up on the LangChain platform to obtain one.

## Integration Steps

1. Add support for handling multiple languages in FastChat by following the instructions given in the [Translate your Site](/docs/advanced-features/translate_your_site.md) tutorial.

2. In the code where you perform inference with the FastChat model, make HTTP requests to LangChain's API to translate input and output text. You will need to translate user input into the model's working language and then translate the model's responses back to the user's preferred language.

Here's a simple Python function to call LangChain API for translation:

```python
import requests

def langchain_translate(text, source_lang, target_lang, api_key):
    url = "https://api.langchain.io/translate/v1"
    headers = {
        "Content-Type": "application/json",
        "x-api-key": api_key,
    }
    data = {
        "source": source_lang,
        "target": target_lang,
        "text": text,
    }
    response = requests.post(url, json=data, headers=headers)
    result = response.json()

    if response.status_code != 200 or "errorMessage" in result:
        raise Exception(f"LangChain API request failed: {result.get('errorMessage', 'unknown error')}")

    translated_text = result["translation"]
    return translated_text
```

3. Use the `langchain_translate` function to translate the input and output with the FastChat model in your application logic.

For more information on FastChat API usage, visit the [API](/docs/api/restful_api.md) section.
