# what is langraph 

langgraph is paradigm shift(change mindeset in AI world)

Langgraph is scalable AI agent workflow using graph-based architectures.

It enables the development of AI agents that can reason, plan, and act through interconnected steps, allowing for cyclical and branching workflows.

## Use case
1. Langgraph use a Graph Structure

2. Build ing multi-agant systems that requred memory,error handling and realtime decision making

exmple:
N8N,Chat bot , coding agents etc


## what is meaning of scalable AI

scalable ai it's mean they use 

- State(for stred data like user query,search result etc)
- node(node mean they as a function )
- adge (adges are conneact a node and work stap by stap)

## about Graph

### 1.State:

state is hold agent data ,they carry information bettween nodes.

like query,booline value,serech information , user name ,id etc

this information are use and access any tools

### 2.Node

Node mean is they react as a function (as step)

like test answer,query send,llm,agent

exmples : user enter query and node are work step by step cheak query type user ask hi,hello rout node are go gemini and user ask coding query so rout are going with claud api.

    graph_builder.add_node("chat_bot",chat_bot)
    --> this node

    graph_builder.add_edge(START,"chat_bot")
    graph_builder.add_edge("chat_bot",END)
    --> this is edges work with node 

    node acte as conditnal statment

### Edge 

Edge is coneact into defreent node in geaph structur way and go to one logic(node) to next(node) logic

or 

an edge connects one node to another.

    graph_builder.add_node("classify_messages",classify_messages)
    graph_builder.add_node("rout_query",rout_query)
    graph_builder.add_node("general_query",general_query)
    graph_builder.add_node("coding_query",coding_query)
    graph_builder.add_node("codin_validate_query",codin_validate_query)


    graph_builder.add_edge(START,"classify_messages")
    graph_builder.add_conditional_edges("classify_messages",rout_query)
    graph_builder.add_edge('general_query',END)
    graph_builder.add_edge('coding_query',"codin_validate_query")
    graph_builder.add_edge('codin_validate_query',END)

- here available two type of edge 
    1. add_edge
    2. add_conditional_edges (act as if,else)



# langchain VS langgraph

langchain provides a standerd interface for interacting with models and components

While Lnaggraph

langgraph is more low lavel and provides more control over the agents  behavior, especially when dealing with complex ,statfull and cyclical workflow