# Building-a-knowledge-grounded-chatbot-using-LLM

In today's data-driven world, the ability to process and generate natural language text at scale has become a transformative force across industries. Large Language Models (LLMs) represent a cutting-edge advancement in natural language processing, enabling businesses to extract valuable insights, automate tasks, and enhance user experiences. By harnessing the power of LLMs, organizations can improve customer service, automate content creation, and gain a competitive edge in the digital landscape.
 
This project builds the foundation for Large Language Models by diving deep into the details of their inner workings. Moreover, It shows how to optimize their use through prompt engineering and fine-tuning techniques such as LoRA. 
 
Prompt engineering techniques involve crafting specific instructions or queries given to the language model to influence its output will be introduced to guide LLMs in generating desired responses through zero-shot, one-shot, and few-shot inferences.
 
Fine-tuning entails training a pre-trained language model on a specific task or dataset to adapt it for a particular application. It explores full fine-tuning and Parameter Efficient Fine Tuning (PEFT), a technique that optimizes the fine-tuning process by focusing on a subset of the model's parameters, making it more resource-efficient.
 
The project also involves the application of Retrieval Augmented Generation (RAG) using OpenAI's GPT-3.5 Turbo, resulting in the development of a chatbot for online shopping for knowledge grounding. Knowledge grounding with Retrieval Augmented Generation (RAG) is implemented to mitigate hallucinations and provide trustworthy and reliable responses. This is achieved by incorporating information from external sources to validate and support the generated text.
 
For example, in the context of an e-commerce chatbot using RAG, knowledge grounding ensures that product information, availability, and prices are sourced from a trusted database or e-commerce platform. This prevents the chatbot from generating inaccurate or fictional details and instead provides responses based on real-world data. 

****Data Description ****
•	The dialogue summarization exercises in this project utilize the knkarthick/dialogsum dataset from the Hugging Face library. 
•	For the purpose of demonstrating the development of a chatbot, data about apparel and paper products is provided. This dataset includes textual information about various apparel items and paper products. 


**Tech Stack**
•	Language: Python 3.8
•	Libraries:  transformers, datasets, torchdata, torch, streamlit, openai, langchain, unstructured, sentence-transformers, chromadb, evaluate, rouge_score, loralib, peft

**Folders in repository:**

Folder name: 'full' contains fully trained model files except files : pytorch_model.bin and optimizer.pt could not be attached as they have huge size and cannot be compressed to 25MB size as required by GitHub.
Folder name: 'peft' contains model trained by using : PEFT ( Parameter Efficient Fine Tuning) , files: adapter_model.bin and optimizer.pt
File: llm_labs.ipynb explains all the concepts mentioned above in detail with outputs
Folder name: 'kb' contains data on apparels and paper products in form of text files: apparel_products and paper_products that we have used for uploading in stream-lit application for the chatbot.
We can run llm_app.py file in jupyter notebook as well by using command : !streamlit run llm_app.py file for executing chatbot app in browser as local url or in network url.
Please note that the use of the OpenAI API may require the utilization of allocated free credits or additional purchases (depending on the account status) for implementing the project. Kindly take note of the free credits limit provided in the account.

File: requirements.txt contains all the packages that need to be installed.

# Execution Instructions
​
# Python version 3.8.10
​
To create a virtual environment and install requirements in Python 3.8.10 on different operating systems, follow the instructions below:
​
### For Windows:
​
Open the Command Prompt by pressing Win + R, typing "cmd", and pressing Enter.
​

Change the directory to the desired location for your project:
​

`cd C:\path\to\project`

​
Create a new virtual environment using the venv module:

​
`python -m venv myenv`

​
Activate the virtual environment:

​
`myenv\Scripts\activate`

​
Install the project requirements using pip:

​
`pip install -r requirements.txt`


​
​
### For Linux/Mac:
​
Open a terminal.

​
Change the directory to the desired location for your project:
​

`cd /path/to/project`
​

Create a new virtual environment using the venv module:
​

`python3 -m venv myenv`
​

Activate the virtual environment:
​

`source myenv/bin/activate`
​

Install the project requirements using pip:
​

`pip install -r requirements.txt`
​

These instructions assume you have Python 3.8.10 installed and added to your system's PATH variable.
​
​

## Execution Instructions if Multiple Python Versions Installed
​
​
If you have multiple Python versions installed on your system , you can use the Python Launcher to create a virtual environment with Python 3.8.10, you can specify the version using the -p or --python flag. Follow the instructions below:
​

### For Windows:
​

Open the Command Prompt by pressing Win + R, typing "cmd", and pressing Enter.
​

Change the directory to the desired location for your project:
​

`cd C:\path\to\project`
​

Create a new virtual environment using the Python Launcher:
​

`py -3.8 -m venv myenv`
​

Note: Replace myenv with your desired virtual environment name.
​

Activate the virtual environment:
​

`myenv\Scripts\activate`
​

Install the project requirements using pip:
​

`pip install -r requirements.txt`
​

​
For Linux/Mac:

​

Open a terminal.
​

Change the directory to the desired location for your project:

​

`cd /path/to/project`


Create a new virtual environment using the Python Launcher:
​

`python3.8 -m venv myenv`


Note: Replace myenv with your desired virtual environment name.
​

Activate the virtual environment:
​

`source myenv/bin/activate`


Install the project requirements using pip:
​

`pip install -r requirements.txt`
​


​

By specifying the version using py -3.8 or python3.8, you can ensure that the virtual environment is created using Python 3.8.10 specifically, even if you have other Python versions installed.
​
​

Then you can run the notebook or use the command to run the app:

`streamlit run llm_app.py`



```
code
├─ full
├─ images
├─ kb
│  ├─ apparel_products.txt
│  └─ paper_products.txt
├─ llm_app.py
├─ llm_labs.ipynb
├─ peft
├─ readme.md
└─ requirements.txt

```
