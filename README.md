# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 25/09/25
# Register no. 212222060143
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

# AI Tools Required:
OpenAI GPT API (ChatGPT / GPT-5)

Cohere API (for NLP tasks)

Hugging Face Transformers (optional, for text or code generation)

Python Libraries: requests, json, pandas

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

Persona Pattern Experiment:

Use the persona of a programmer to interact with AI tools for a specific application (e.g., generating Python code, summarizing data, or creating AI-driven recommendations).

Create prompts for each AI tool using both naïve and refined structures to analyze how responses differ.

Python Code Development:

Automate sending prompts to multiple AI tools via their APIs.

Retrieve responses and compare outputs.

Generate insights such as code correctness, efficiency, or quality of explanations.

Analysis & Discussion:

Compare outputs from different AI tools based on clarity, correctness, and depth.

Highlight differences in approach, strengths, and limitations of each AI tool.

# Sample Python Code:

#Import libraries
import requests
import json

#Example: OpenAI API interaction
def get_openai_response(prompt):
    url = "https://api.openai.com/v1/chat/completions"
    headers = {
        "Authorization": "Bearer YOUR_OPENAI_API_KEY",
        "Content-Type": "application/json"
    }
    data = {
        "model": "gpt-5-mini",
        "messages": [{"role": "user", "content": prompt}],
        "max_tokens": 150
    }
    response = requests.post(url, headers=headers, json=data)
    return response.json()["choices"][0]["message"]["content"]

#Example: Cohere API interaction
def get_cohere_response(prompt):
    url = "https://api.cohere.ai/generate"
    headers = {
        "Authorization": "Bearer YOUR_COHERE_API_KEY",
        "Content-Type": "application/json"
    }
    data = {
        "model": "command-xlarge",
        "prompt": prompt,
        "max_tokens": 150
    }
    response = requests.post(url, headers=headers, json=data)
    return response.json()["generations"][0]["text"]

#Example prompts
prompt = "Generate a Python function to calculate factorial of a number."

#Get responses from both AI tools
openai_output = get_openai_response(prompt)
cohere_output = get_cohere_response(prompt)

print("OpenAI Output:\n", openai_output)
print("\nCohere Output:\n", cohere_output)


# Conclusion:

Multiple AI tools can be integrated via Python APIs to automate tasks efficiently.

Comparing outputs provides insights into tool strengths, response clarity, and code quality.

Using the persona pattern helps tailor the prompts to the desired domain or role, resulting in higher-quality responses.

# Result: 
The corresponding Prompt is executed successfully.
