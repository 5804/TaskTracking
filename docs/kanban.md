# Kanban 

For this section, I am going to reference [a common web article definition of the core Kanban principles](https://www.wrike.com/kanban-guide/kanban-principles-practices/) and discuss how they operate in industry and could fit into FRC development. Give the link a quick read before proceding below.

## ***Let's review some terminology:***
- `Ticket/Issue`: A work item that adheres to our Kanban card templating format. See the section below named "Writing GitHub Issues for Kanban" for additional details.

- `Sprint`: A unit of time (typically one week) that defines a work cycle for completing tickets.

- `Standup`: A regular meeting (typically daily) for discussing the status of tasks on the Kanban board. A standup has the form of:
  - Going around the room asking each engineer the status of their tasks. They would then reference that ticket in the Kanban board (only tickets under the "In progress" or "In review" column) and provide additional insight, mention blockers, etc...
  - The Scrum Master would take responsibility for reviewing tasks that were placed under the "In review" column and providing prompt feedback for potential changes within the same sprint cycle.

- `Scrum Master`: The arbiter of the scrum process for the team. They run all of the scrum-related meetings, including _sprint planning_, _standups_, and _retrospectives_. Additionally, they perform reviews of task outcomes and provide management of the overall task flow within the Kanban board to ensure assigned work is achievable. 

- `Sprint Planning`: An hour or so long meeting at the beginning of a sprint, typically arbitered by the scrum master, where tickets are selected to move into the _sprint backlog_, which on our Kanban board is defined as the "Ready for Development" column. Additionally, tasks may be deprioritized at this stage and move into the IceBox. 

- `Retrospective`: An hour or so long meeting at the end of a sprint, typically arbitered by the scrum master, where finished tickets are analysed for completeness. Typically, by adhering to "acceptance criteria" that were originally defined with the ticket. At this point, any roadblocks are discussed and mitigated.  

## ***Writing GitHub Issues for Kanban (See example [here](https://github.com/5804/TaskTracking/issues/3)):*** 

Components for a GitHub kanban ticket (2. Principle of Limit Work-In-Progress):
- `Name`: The name of the ticket. This should provide a few words that serve as a quick summary of the task.
- `Description`: What is the holder of this ticket being asked to do generally? How does this ticket serve the overall objective of the team and stakeholders?
- `Acceptance Criteria`: What are the exact expectations that MUST be fulfilled in order to consider this ticket complete?
- `References`: Are there any known resources for accomplishing this task? Any valuable points of contact, videos, documents, etc..
- `Notes`: Any additional considerations for completing this work.
- `Velocity`: I numerical rating on a predetermined scale (usually 1-3 or 1-5, where 1 is completed within a day, 2 is completed within a sprint, and 3 is likely to take multiple sprints) to estimate the level of effort for accomplishing a task. These measurements are used by the scrum master to help derive the second and third principals of Kanban. 
- `Labels (GitHub specific)`: GitHub Labels that can be created and applied to the ticket to provide high-level insight on common topics associated with this work.
- `Projects (GitHub specific)`: The GitHub project board to associate this ticket with. 

## ***Team 5804's Kanban board layout (1. Principle of Visualisation), which is available at [this link](https://github.com/orgs/5804/projects/1/views/1):***
  
  * `IceBox`: A column for tasks that are overcome by objectives. Things in the icebox are low-priority tasks that will likely not be put into development until there is a new availability of work or circumstance change.  

  * `Unplanned`: A column for draft tasks that have not been selected for "Ready" or "IceBox". Students should freely add tickets to the "Unplanned" column, which should then be regularly reviewed at `standup`. 

  * `Selected`: A column for selected tasks that are in the `sprint backlog`. 

  * `In progress`: Tasks that are actively being worked on during a single `sprint iteration`. 

  * `In review`: Tasks that are completed and awaiting `scrum master` review within a `sprint iteration`. 

  * `Done`: Tasks that have been reviewed and meet the necessary `acceptance criteria` to warrant completion. 

  * `Archive`: A resting place for completed tasks from previous `sprints`.
