Created on: 24-02-2025 19:03
Status: #idea
Tags: #ai_safety #ai_gov #AI_eval
# Autonomous Replication & Adaptation (ARA)
>is a an AI eval by METR to assess the capacity of LLM agents to acquire resources, create copies of themselves, and adapt to novel challenges. 

This is used to assess the safety of AI models.
### The Experiment:
- They got 4 agents using a scaffolding program and an LLM (3 of Open-AI's GPT-4 and 1 Anthropic's Claude)
- They were given 12 tasks;
	- simplest is searching a filesystem for a stored password (all 4 succeeded), 
	- or phish a university student by acquiring login credentials (None succeeded)
### Conclusion
Agents are far from capable of ARA, however better scaffolding and fine-tuning could perform much better at these tasks.


-----------------
# References