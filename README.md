# Monitoring Core Web Vitals

This is an example project for showing how to implement a basic performance
monitoring script to capture Core Web Vitals. This is for educational purposes
and is not production ready.

If you need production website monitoring, check out [Request Metrics](https://requestmetrics.com/)

## Setup

- Node 14.15.0
- npm install
- npm start
- import os
from azure.ai.inference import ChatCompletionsClient
from azure.ai.inference.models import SystemMessage, UserMessage
from azure.core.credentials import AzureKeyCredential

endpoint = "https://models.github.ai/inference"
model = "openai/gpt-4.1"
token = os.environ["GITHUB_TOKEN"]

client = ChatCompletionsClient(
    endpoint=endpoint,
    credential=AzureKeyCredential(token),
)

response = client.complete(
    messages=[
        SystemMessage("You are a helpful assistant."),
        UserMessage("What is the capital of France?"),
    ],
    temperature=1.0,
    top_p=1.0,
    model=model
)

print(response.choices[0].message.content)

#🚡
#:[0-9]



