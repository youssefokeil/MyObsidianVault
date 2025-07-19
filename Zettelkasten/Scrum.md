Created on: 22-04-2025 18:27, Note by Youssef Okeil
Status: #idea
Tags: #software #agile
# Scrum
> Isn't confined to software projects. The creation of books can also benefit from Scrum concepts. 

- **Roles**: Product Owner, Scrum Master, Developer.
- **Artifacts**: Product Backlog, Sprint Backlog, Scrum Board, Burndown Chart.
- **Events**: Sprint Planning, Sprint, Daily Meetings, Sprint Review, Retrospective.
### Roles:
1. **Product Owner (PO)**
	- requires clear vision of the product developed.
	- writes user stories
	- should consistently be available to address team's questions
2. **Scrum Master**
	- Responsible for ensuring the adherence of the team to the Scrum framework
	- They do not lead the team, as Scrum teams are self-organizing
3. **Developers**
	- Scrum teams should be multidisciplinary and cross-functional
	- Reduce dependency on external members
	- Should have specialists such as front-end developers, back-end developers, database specialists, and UI designers. They are responsible for technical decisions during the project
### Artifacts and Events
1. **Product Backlog** (Artifact)
	prioritized list of user stories. 
	- not static, requires constant updates to capture changes to requirements
	- product owner should updates the product backlog, to remove old features that no longer hold relevance and emerging new ideas
2. **Sprint** (Event)
	every sprint should yield a product increment with clear customer values.
3. **Sprint Planning** (Event)
	is a preparatory meeting that serves as the launchpad for every sprint. The meeting consists of two parts:
	1. Product Owner, suggests stories for the upcoming sprint. Remaining team members evaluate if they have enough capacity and velocity to implement them
	2. Then developers decompose tasks and their execution times are estimated.
4. **Sprint Backlog** (Artifact)
	- generated at the end of the Sprint Planning
	- a list of tasks for the sprint
	- is also a dynamic entity like the product backlog
		- Unchanged: the sprint goal, the selected stories should remain unchanged. If stories are to be changed, they are changed between sprints
		- Changed: tasks and the estimated effort for each task.
**Additional Scrum Artifacts**
5. **Scrum Board** (Artifact, compliments the sprint backlog)

	![[Screenshot 2025-04-22 192912.png]]
	provides visual aid for tracking the daily progress of the sprint. 
	The criteria for marking stories as done is very important:
	- maybe that all its unit tests pass.
	- maybe a code review by another team member is required.
6. **Burndown Chart** (Artifact)
	- displays the number of work hours remaining to complete the unfinished tasks on each day of the sprint.
	 ![[Screenshot 2025-04-22 195747.png]]
	 
**Additional Scrum Events**
7. **Daily Stand-Up meetings** (Event)
	lasting 15 minutes and involving all team members, to facilitate communication and information sharing among team members. 
	1. What tasks were completed the previous day? 
	2. What tasks are planned for the current day? 
	3. Are there any significant obstacles hindering their progress?
8. **Sprint Review**
	show case the results of a sprint
	- involves all team members and stakeholders relevant to the sprint's goals
	- **Product Owner** approves all user stories in a sprint. If any issues are identified, the story is returned to **Product Backlog** to be reworked in a future spring.
9. **Retrospective**
	conclusion of a sprint. 
	- address critical issues; tardiness, absence from daily meetings, etc.
	- after the retrospective the project progresses to next sprint with actionable insights.

| **Event**       | **Time-box**       |
| --------------- | ------------------ |
| Sprint Planning | maximum of 8 hours |
| Sprint          | less than 1 month  |
| Daily Stand-Up  | 15 minutes         |
| Sprint Review   | maximum of 4 hours |
| Retrospective   | maximum of 3 hours |


-----------------
# References
[[Software Engineering:  A Modern Approach]]