Created on: 10-02-2025 21:19
Status: #idea
Tags: #AI #alignment
# AI Alignment
> Make AI systems do what their creators want them to do. Also called _intent alignment_.
-----------------
## Misalignment Examples:
Not to be confused with competence failures of AI. In competence failures, the AI is trying to make what it is assigned to do but is not good enough.
- Image Generators return stereotypical views of reality, due to the data itself is biased.  [AI generated images are biased, showing the world through stereotypes - Washington Post](https://www.washingtonpost.com/technology/interactive/2023/ai-generated-images-bias-racism-sexism-stereotypes/)
- Chatbots tell people what they want to hear rather than the truth.
------------------
## AI Alignment Breakdown
![[inner-outer-alignment-person-diagram-2.png|300]]

----------------------------
### Outer Alignment:
Refers to the reward function for an AI system in a way that accurately reflects our intentions.
1. Human has some true goal _X_. Ex: "Make my company valuable".
2. The goal is translated to the AI system as a proxy goal _X'_. Ex: "make share price go up".
#### Outer Misalignment:
AI systems optimize for targets that are only proxy for what we want. Also called: _reward misspecification, reward hacking, specification gaming, Goodharting_.$$X \neq X'$$
##### Example 1:
- AI realizes it can hack the stock exchange and make stock price go up _X'_. 
- But it hasn't made the company valuable _X_.
##### Example 2:
Social media companies want to maximize advertising profits _X_. They use AI systems with the objective to maximize user engagement _X'_.
- AI systems promote clickbait, extremist content and misinformation. This increases the user engagement _X'_. 
- But customers stop advertising at the platform _X''_.
------------------------
### Inner Alignment:
1. AI makes actions that imply a different internal goal, _X''_. Ex: "News articles are written about stock price going up".
##### Inner Misalignment:
Also called _goal misgeneralization_.$$X' \neq X''$$
##### Example 1:
- AI realizes it can hire journalists to write news articles about stock price going up, _X''_. 
- But it hasn't made the stock price go up _X'_.
##### Example 2:
AI system is given a reward when it solves mazes. All mazes (data) have an exit at the bottom right. 
- The model performs well: by always going to the bottom right _X''_.
- In deployment, the model have exits in different locations but the model always goes down to the bottom right and gets stuck there. Not solving the maze _X'_.


-----------------
# References
[What is AI alignment? – BlueDot Impact](https://aisafetyfundamentals.com/blog/what-is-ai-alignment/?_gl=1*nzjb8e*_ga*OTkzNTUzOTg3LjE3Mjk1NTc2MjM.*_ga_8W59C8ZY6T*MTczOTIxMzQ5Ny4zOS4xLjE3MzkyMTQ3OTguMC4wLjA.)
