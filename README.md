# Install

## Setup conda env and use Python version 3.9

```
  conda create --name jupyter python=3.9
```

```
  conda activate jupyter
```

```
  conda install -c conda-forge ipywidgets
```

## Install 

You can use Visual Studio Code or use Jupyter notebook server instead.

### Visual Studio Code

Open the project folder using Visual Studio Code and run the Jupyter notebooks in the IDE.

### Jupyter 

See also https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html

```
  conda install -c conda-forge jupyterlab
```

#### Start the jupyter notebook server

```
  jupyter-lab
```

On Mac M1 processors you need to have the arm64 lib versions
This is how you can install them.

```
  pip uninstall hnswlib

  ARCHFLAGS="-arch arm64" pip install hnswlib --compile --no-cache-dir
```

# Examples

## 1. OpenAI

This is a Python notebook example that demonstrates how to use the OpenAI API to generate text completions. The notebook installs the OpenAI package using pip, sets the API key, and defines a function that generates text completions based on a given prompt. The notebook provides examples of generating text completion for different prompts, including creating a tweet and adding emojis. The notebook uses the text-davinci-003 engine for generating text completions and sets the max_tokens to 100.

## 2. LLM 

This Python notebook provides two different examples of using OpenAI and LangChain libraries.

The first example demonstrates how to use OpenAI's GPT-3 language model to generate text completions. It defines a function call_gpt to generate text completion given a prompt. Then, it provides three different prompts and calls the call_gpt function to generate text completion for each prompt.

The second example shows how to use the LangChain library's LLM to generate answers to questions using OpenAI's GPT-3 language model. It uses the LangChain LLM to generate answers to two different questions, "What is the meaning of life?" and "When is the next Devoxx Belgium?".

## 3. LLM & YouTube

This notebook contains code for using OpenAI's GPT model to generate text, specifically for answering questions and summarizing text. 

It also includes code for loading data from YouTube videos using the YouTube Transcript API and PyTube. The code uses LangChain, a Python library for building language models. 

The notebook demonstrates two methods for summarizing text: "STUFF-ing" and "Map Reduce". The former involves stuffing all relevant data into a prompt as context to pass to the language model, while the latter involves an initial prompt on each chunk of data.

## 4a. LLM & YouTube & QnA

The code loads a YouTube video, splits it into chunks, converts those chunks into embeddings, and performs a similarity search to find the most relevant chunks to a given query. The code then uses those chunks to answer a question using a question-answering model. 

There are several variations of the question-answering model used, including one that involves intermediate steps and a map-rerank method.

## 4b. LLM & Groovy & QnA

The code loads the Groovy documentation in HTML, strips the HTML tags and removed the new lines.
Langchain splits the text into chunks, created embeddings and stores it into a FAISS in memory vector database.
Now we can ask questions using the related Langchain lib.

## 5. LLM & QnA & Google Search

The notebook performs a question-answering task using various tools and APIs, including OpenAI's GPT, YouTube Transcript API, PyTube, transformers, ChromaDB, and langchain. It creates a document database and performs a similarity search on a given query before using a question-answering model to answer the query. 

Finally, the script initializes a Google search agent and runs two queries using it.

## 6. ChatGPT FAQ

This example uses OpenAI's CHATGPT to answer questions about Devoxx Belgium 2023. 

It's designed to answer questions based on a pre-defined context and specific role. It allows to ask questions about the event's schedule, location, registration, ticket types, code of conduct, cancellation policy, transportation, and other relevant details. 

## 7. LLM & QnA & Web

This example runs several questions through the LLM agent. The agent uses various tools such as search engines, calculators, and Wolfram Alpha to answer the questions posed to it.

## 8. LLM Tools & QnA

This example uses Python REPL and BashProcess to visit a website and get details from a webpage.

## 9a. LLM & Python REPL - Game 1

The example initializes an agent to execute a zero-shot-react-description task. 

The agent is run with a task to create a Python function that prints the word DEVOXX using ASCII-art. 
The output shows the code for the function and verifies that it produces the desired output.

## 9b. LLM & Python REPL - Game 2
