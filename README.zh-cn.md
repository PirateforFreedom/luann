


# Luann

<p align="center">
  <img src="./assets/luann_github.png" alt="luann logo"></a>
</p>

<div align="center">

 <strong>Luann（fka TypeAgent）可以创建许多基于 LLM 的Agent（各种类型的Agent，可大量化创建），它具有完整的记忆模块（长期记忆、短期记忆）、工具使用模块、RAG 模块等。</strong>
</div>

<div align="center">

 <strong>[English](README.md), [简体中文](README.zh-cn.md)</strong>

</div>







Luann 让用户能够轻松构建和部署 LLM Agent，并支持: 
* 长期记忆/状态管理、短期记忆
* 由外部数据源（例如 PDF 文件）创建的知识库的基本 RAG 工作流程
* 定义并调用自定义工具，然后帮你做一些事情（采取行动）
* 改变角色设定和角色扮演
* 创建各种类型的Agent（memgpt、swe、langchain 代理等）

用户还可以使用 Luann 将Agent部署为*服务*。可以在Luann 服务上运行多用户、多Agent应用程序。




## 快速入门


### pypi 包 安装
1. 运行 `pip install luann`。
2. 运行 `luann server`。
3.在浏览器中访问 `localhost:8283` 查看开发者 Restful API。
4. 然后你可以使用 restful api 和python Client来开发你的应用程序。


### 开源源代码安装
0. GIT CLONG repo
1. 运行 `python main.py configure`
2. 运行 `python main.py server`
3. 在浏览器中访问 `localhost:8283` 查看开发者 Restful API
4. 然后你可以使用 restful api 和python Client来开发你的应用程序 

Luann 的 pip 安装默认使用 SQLite。如果您自己的计算机上运行着 PostgreSQL 实例，仍然可以通过设置环境变量 LUANN_PG_URI 将 Luann（通过 pip 安装）连接到 PostgreSQL。

## 支持的Agent类型
Luann 旨在创建各种类型的Agent。支持以下类型的Agent：

| 类型            | 支持状态    |
|---------------------|-----------------|
| Memgpt              | ✅               |
| openhands        |    ❌           |



## 支持的 LLM 和 Embedding 后端
支持以下 LLM 和Embedding端点： 

| 供应商            | LLM Endpoint    | Embedding Endpoint |
|---------------------|-----------------|--------------------|
| OpenAI              | ✅               | ✅                  |
| Azure OpenAI        | ✅               | ✅                  |
| Google AI (Gemini)  | ✅               | ❌                  |
| Anthropic (Claude)  | ✅               | ❌                  |
| vLLM                | ✅               | ❌                  |
| Ollama              | ✅               | ✅                  |

当将 Luann 与开源的 LLM（例如 ollma 和 vllm）一起使用时，Luann 的性能将高度依赖于 LLM 的函数调用能力、语言理解和推理能力。
## 文档
 正在制作中。。
## 即将要做的

- 添加其他类型的代理（更复杂的代理，如 openhand，或简单的功能代理）
- 添加其他vectordb和其他llms
- add baichuan/qianwen etc LLM
- 添加语音克隆（tortoise-tts）
- 添加代理评估
- 添加生产 RAG 评估（Ragas https://github.com/explodinggradients/ragas 和部分来自 crewai）
- 添加 OpenAI Swarm
- 添加 LLM 重排序子系统（GPT4o 重排序子系统
- 添加自动化工作流程（不仅聊天，还可以做其他事情）
- 添加会话时间线（来自phidata）
- 添加其他模态模型，如OCR模型、BLIP等。
- 使用自主研发的深度学习训练框架PyFlame添加已训练好的SLM或SMM，或对SLM进行微调，旨在使用特定的用例，因为特殊的小模型作为代理框架中模块的润滑剂
- 添加使用记录


## 补充说明

- 我们的 Luann 代码库主要基于 [MemGPT 代码库](https://github.com/cpacker/MemGPT?tab=readme-ov-file)，感谢开源
- MemGPT(letta)与Luann的区别在于，Luann对原有的memgpt整个代码结构进行了优化，提出了新的小型、轻量级的代理开发框架，易于扩展创建代理，各有优势。
- 新的想法和新功能将不断添加，让每个人都能很好地使用
- 新版本正在编码，请等待..
  
## 路线图
目标：情商和智商代理，工具代理，规模化创建代理更容易
