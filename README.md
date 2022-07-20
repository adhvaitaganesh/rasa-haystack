# Rasa Haystack Integration for a specific use case

AI assistants have been around for quite a while, however they become useless when a specific knowledge based question is asked.
Here we leverage RASA a conversational chat bot platform, and Haystack a NLP transformer framework to create intelligent chatbots that can answer specific 'long-tail' questions.

# How this works
Generally, all the conversational aspects are taken care by RASA using its intent handling techniques, which can also be trained to custom use cases.
Whenever a specific knowledge based question is asked, the RASA framework calls haystack's question-answering model to get the relevant answer from a curated knowledge base!

## Below are the steps to use this project
### Make changes to the following files on the RASA location
- domain.yml
- config.yml 
- data/nlu.yml
- data/rules.yml
- actions/actions.py

### Start the Haystack REST API and a demo DocumentStore via Docker: 
```
git clone https://github.com/deepset-ai/haystack.git
cd haystack
docker-compose pull
docker-compose up
```
  
### Train a model in this repository with `rasa train`  
### Call `rasa shell` to start interacting with the chatbot.

# Voila!, enjoy chatting :)
