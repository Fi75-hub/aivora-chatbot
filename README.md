# Aivora — Shopping Support Chatbot

A Python chatbot that handles simulated online-shopping support conversations using regular expressions, keyword scoring and NLTK text preprocessing. Its responses and support rules are stored in a separate JSON knowledge base.

## Features

- 55 intents covering orders, returns, delivery, payments, accounts and related support topics.
- Tokenisation, stemming, synonym normalisation and simple spelling correction.
- Session memory for a name, preference and order reference.
- Context and follow-up handling, clarification prompts and rule-based priority detection.
- A summary of the conversation when the user exits.

The conversation runs locally using the rules and responses in `intents.json`. Order numbers are used for session context; they are not looked up in a shop database.

## Run the notebook

Use Python 3.10 or later and a Jupyter environment. From this folder:

```sh
python -m pip install -r requirements.txt
python -m pip install jupyterlab
python -m jupyterlab
```

Open `aivora.ipynb` and run the cells in order. The final cell starts the interactive conversation. Type `exit` or `quit` to finish. Keep `intents.json` beside the notebook, and use this folder as the notebook working directory.

The NLTK utilities used here do not require downloading a separate corpus or language model.

## Try it

```text
hello
my name is Alex
where is my order
order number 12345
exit
```

Responses are demonstration text selected from `intents.json`; some response templates are selected randomly.

## Structure

| File | Purpose |
| --- | --- |
| `aivora.ipynb` | Conversation loop, preprocessing, intent detection and response generation |
| `intents.json` | Intent patterns, response templates, language rules and follow-up data |
| `requirements.txt` | Python runtime dependency |

## Project context

Developed for the Programming with Data midterm in the University of London Computer Science programme. The notebook follows the supplied starter-template stages and adds the support domain, JSON knowledge base and extensions described above.
