# What is Human in the loop

Human in the loop mean of is enble human intervention(involve) at any point in a workflow.

This especially usefull in large language model(LLM) - deriven applications where model output may require validation , correction ,or additional context..


exmpele of tool:

    @tool
    def human_assistance(query: str) -> str:
        """Request assistance from a human."""
        human_response = interrupt({"query": query})
        return human_response["data"]


# what is persistent layer

persistent execution state :

    interrupts use langgraph presistence layer(Save the data via cheackpointer) , which saves the graph state , to idefinitely pause graph execution until you resume.

