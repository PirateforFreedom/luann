


# Luann

<p align="center">
  <img src="./assets/luann_github.png" alt="luann logo"></a>
</p>

<div align="center">

 <strong>Luann (fka TypeAgent) allows you to create many LLM based agent(Various types of agent,scale up),which has complete memory module (long-term memory, short-term memory),Tool Use module,RAG module etc.</strong>
</div>

<div align="center">

 <strong>[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.pt-br.md)</strong>
</div>







Luann makes user easy to build and deploy  LLM agents with support for: 
* Long term memory/state managemet,short term memory
* Basic RAG workflow for knowledge base which created by external data sources (e.g. PDF files)
* Defining and calling custom tools，then help you do something(take action)
* Changing personas settings and role-playing
* Create various types of agent(memgpt,swe,langchain agent,etc..)

You can also use Luann to deploy agents as a *service*. You can use a Luann server to run a multi-user, multi-agent application on top of supported LLM providers.





## Quickstart


### From pypi
1. Run `pip install luann`
2. Run `luann server`
3. Go to `localhost:8283` in the browser to view the developer portal
4. then you can use restful api and client to develop your app


### From source
0. Clone the repo
1. Run `python main.py configure`
2. Run `python main.py server`
3. Go to `localhost:8283` in the browser to view the developer portal
4. then you can use restful api and client to develop your app 

The pip install of Luann defaults to using SQLite. If you have a PostgreSQL instance running on your own computer, you can still connect Luann (installed via pip) to PostgreSQL by setting the environment variable LUANN_PG_URI.

## Supported Type of Agents 
Luann is designed to Create various types of agent. The following type of agent are supported: 

| Type            | supported    |
|---------------------|-----------------|
| Memgpt              | ✅               |
| openhands        |    ❌           |



## Supported Endpoints & Backends
Luann is designed to be model and provider agnostic. The following LLM and embedding endpoints are supported: 

| Provider            | LLM Endpoint    | Embedding Endpoint |
|---------------------|-----------------|--------------------|
| OpenAI              | ✅               | ✅                  |
| Azure OpenAI        | ✅               | ✅                  |
| Google AI (Gemini)  | ✅               | ❌                  |
| Anthropic (Claude)  | ✅               | ❌                  |
| vLLM                | ✅               | ❌                  |
| Ollama              | ✅               | ✅                  |

When using Luann with open LLMs (such as ollma and vllm ), the performance of Luann will be highly dependent on the LLM's function calling ability ,Language understanding and reasoning skills.

## Docs
 Coming
## TODO LIST

- add other type agent( more complex agent  like  openhand, or simple functional agent)
- add other vectordb and other llms
- add baichuan/qianwen etc LLM
- add voice clone （tortoise-tts）
- add Agent Evaluation
- add Production RAG Evaluation（Ragas https://github.com/explodinggradients/ragas and part from crewai）
- add openai swarm
- add LLM reranker subsystem（GPT4o reranker）
- add automation workflow（not only chat but also do something）
- add session timeline （from phidata）
- add  Other modulus models, such as OCR models, BLIP etc.
- add trained SLM or SMM or fine-tune SLM by using Self-developed deep learning training framework PyFlame ,which aimed to use specific usecase,because Special small models act as lubricants for modules in the agent framework
- add usage recording


## Comments

- This project is a Leisure time hobby.
- Our codebase for the Luann builds heavily on [MemGPT codebase](https://github.com/cpacker/MemGPT?tab=readme-ov-file),Thanks for open-sourcing! 
- The difference of between MemGPT(letta) and Luann is that Luann optimizes the entire original memgpt code structure and propose new ,Small, lightweight, Agent Development Framework,which is  Easy to scale up of creating agents.Each has its own advantages
- New ideas and new features will be added continuously,make everyone use very well
- new version is coding ,please wait..
  
## Roadmap
goal:EQ and IQ AGENT ,TOOL agent ,Scale up to create agent more easier
