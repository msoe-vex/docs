.. Document describing the high level process we take when developing software

Process Overview
================

Our team has adapted a custom process to aid us in the software development process. Our process is heavily influenced from both the :term:`Kanban` and :term:`Scrum` project management methodologies, with resources on each being available in the Glossary and Appendix. This section will describe how our process works, as well as the features we use from different project management processes. The steps to the process will be outlined sequentially.

**Platform Strategy**

Developing the platform stragey is how ideas are first introduced into our platform, which is guided by the Executive Board. 

Town Hall meetings are held by the Exective Board to outline the current plans for the upcoming 2-3 quarters. The entire team is open to share ideas and contribute to the plan, but the Exective Board is responsible for facilitating the meetings and collecting feedback.

The plan that is created should encompass high level features early on, and become more granular as it moves closer to the quarter start. The Executive Board should work with project manager(s) to determine the specifics of the plan, and develop the detail necessary to act on the plan.


**Work Intake**

Work Intake refers to the process of how we plan and prioritize work that needs to be done. When we move onto the next project or set of work, it gets pulled into the :term:`Software Backlog`, hosted on GitHub. 

(TODO image here)

The :term:`Software Backlog` consists of :term:`Issues` (also known as tasks) that outline all of the major features that need to be completed. Each new issue contains key information, including:

- :term:`Issue Description`

    - A high level description of what the current problem is, and what is being solved with this feature

- :term:`User Story`

    - A brief story description of the problem being solved
    - Following the user story form: *As a <user>, I want <feature> so that I can <use case>*
    - Used to quickly understand the objective and value of the issue

- :term:`Issue Completion Steps`

    - A checkmark list of steps required to complete the software component of the issue
    - If the issue hasn't undergone :term:`Grooming`, then this section can be empty

- :term:`Definition of Done`

    - A checkmark list of requirements for the card to be completed
    
- :term:`Card Labels`

    - Issue type (bug, enhancement, documentation, etc)
    - Assigned team (Web, Embedded, AI, etc)
    - Point estimate
        
        - This value is determined during the :term:`Grooming` process, where the team talks through the issue. This will be discussed in the **Grooming** section


The following can be used as a template when creating new issues:

```
TODO
TODO
TODO
```

