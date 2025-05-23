# Building-Agentic-AI-Chatbot-using-LangGraph
Developing an Agentic AI Chatbot using LangGraph tools. A Qwen LLM is utilized here leveraging tools which include ArXiv, Wikipedia and Tavily for Internet search

To build the State Graph i.e structure of entire graph, the workflow consists of the following:
1. Nodes: Python functions corresponding to tasks
2. Edges: Connects the nodes (can also contain a conditional edge)
3. State: State schema serves as the input for all nodes.

For the chatbot workflow which is created using LangGraph,


![image](https://github.com/user-attachments/assets/568f5568-0d22-4462-8dc4-a656b31b1828)

When the LLM/AI Assistant (which is considered as the brain) receives any input from the user, there will be two responses based on the state of the message:
- Either the user input must be very generic which can be answered directly by the LLM itself
- Or a tool call will be initialized (Groq) if the LLM is unable to answer the question on it's own since the LLM doesn't have access to latest records/current affairs.

Ultimately, integrating the LLM with tools lets it decide or think whether to make a tool call based on input and then act accordingly which is known as the ReAct architecture (Reasoning + Thinking)

This tool call can be initialized using the ToolNode - A node which is integrated with some tools. Here these tools include ArXiv, Wikipedia and Tavily.

#### Note: Details for code logic are written within the notebooks as comments and markdowns as inference

