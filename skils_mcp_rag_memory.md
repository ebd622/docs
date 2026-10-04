# Skills vs MCP vs RAG vs Memory: What AI Agents Need to Know
Modern AI agents need multiple capabilities working together such as Skills, MCP, RAG and Memory that solve different problems


## Skils
Skills define how the agent performs a task (i.e. a kind of set of instructions). 

Examples:
* Analyze a log file
* Troubleshoot Kubernetes deployments

A skill usually contains:
* Instructions
* Workflows
* Best practices
* Tool usage patterns

## MCP
MCP is a standard way for agents to connect to external systems.

Examples:
* Splunk (to get logs)
* GitHub
* Jira
* Azure

## RAG (Retrieval-Augmented Generation)
RAG helps the agent access information it wasn't trained on. RAG reads docs fom a Vector DBs and thouse docs were put into that DB by a person.

Examples:
* Internal documentation
* Runbooks
* Wiki pages
* Architecture documents

## Memory
Memory is the stuff that agent (not a person) has picked up itself and kind of stored for later from things that happened preciously. So, the agent can look back at some kind of memory to get knoledge from previous ex[erience/iteration.

For example, when the agent managed to find/fix an issues it can save back details on the issue into the memory and use it next time.

## Summary
* Skill is a procedure to follow something repeatable
* MCP is a way the agent can look something up in the world
* RAG is knowledge that somebody has written down
* Memory is knowledge that the agent picked up from experience

# Resources
* https://youtu.be/X4FVEEegCbk?si=n_WfuJjQFHDodRMI
