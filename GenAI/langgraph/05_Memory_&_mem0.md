# Introduction

<h3>mem0 is a memory layer designed for modern AI agents. it acts as a persistent memory layer that agent can useto:

1. recall relevant past interactions
2. store important user preference and factual context
3. learn from success and faliures

It gives AI agents memory so they can remember, learn, and evolve across interactions. Mem0 integrates easily into your agent stack and scales from prototypes to production systems

</h3>

# Stateless and Statful Agents

<h3> Statless meaning is </h3> they process a query , generate a response and forget everythings 

<br>
even with huge context windows , everything reset the next session 

User --> Agant ---> response

then  new seesion is non context preserved

agent starts from zero and all context from previous runs lost

<h3> Statful Agents</h3>

Statfill agents are different. they retain context , recall what matter and behave more intelligently over the time.

User(query) --> Agent --> Memory --> responser

New session context preserved(it usually means that previous information is kept and carried forward into the current step and intreaction.) 

in short statless lost past information and statful agent are not lost past information

# What is memory

<h2> Types of memory </h2>
<h3> 1.short term memory
<h3> 2.long term memory
</h3>

## 1. short term memory 

this memory working for short time session awareness(info kept only for a short time)

If you close the app or restart, this memory is gone unless saved.


## 2. Long term memory

<h3> 1. Factual memory: They remmeber person facts like name ,profassion,frirnd ,familly and other ...

<br>

<h3> 2. Episodic memory :

