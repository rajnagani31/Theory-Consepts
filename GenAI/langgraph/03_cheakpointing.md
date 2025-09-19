# What is cheakpointing

Cheakpointing is process of saving the state of graph (agent exicution) at specific point 

so you that can:

    Pause and resum leater (even srever restart)
    recover from the error without reruning everything



Benefits in Real Use Cases

Chatbots with memory → conversation doesn’t reset if server restarts.

Human-in-the-loop → pause execution until user approves, then resume.

Data pipelines → if API rate limit hits, wait and resume later.

Long tasks → LLM agents that take hours/days to finish.

# NOTE : this cheakpointing consepts stord all user data (like : user name is this ) this consept are not use vector embedings stord data

