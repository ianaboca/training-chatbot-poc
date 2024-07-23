# Customer Support Agent Training Chatbot POC

This is a proof of concept of a customer support agent training tool.
The goal of the tool is to improve customer satisfaction through realistic case studies and training for the support agents.
It is powered by generative AI, namely [OpenAI chat completion API](https://platform.openai.com/docs/api-reference/chat/create).

A typical training conversation with the chatbot:

https://github.com/user-attachments/assets/63324d81-a12e-4c3d-9c4b-882a0a80daeb

## Usage

> [!WARNING]  
> The proof of concept leaks the API key through the `apiKey` query parameter.

Open the following URL with your OpenAI API key:

https://ianaboca.github.io/training-chatbot-poc?apiKey=YOUR_API_KEY

The page will issue a warning if the `apiKey` query parameter is missing from the URL.

## Known issues

### Persona swap

Sometimes the chatbot swaps the personas in the chat.
The initial prompt instructs the model to act as a customer, but in the course of the conversation it may generate a response as if it was the agent and continue to do so.
The only reliable solution is to restart the conversation.
