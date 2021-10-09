.. This document creates a term glossary

Glossary
========

.. glossary::
    Backlog
        The backlog is a list of tasks, or :term:`Issues` that we are looking to solve. The backlog stores anything that we plan on working on in the future, from several days out to years out. The primary use of this is to capture what we *need* to work on, before it is forgotten or lost. Backlogs are often very large, and because of that, a :term:`Project Manager (PM)` is responsible for prioritizing the importance of issues. If a PM believes a certain issue needs to be accomplished before the others, it will move to the **top** of the backlog. Likewise, if something isn't very important, it will move to the **bottom** of the backlog. To fully utilize this prioritization, members should always take tasks from **near the top** of the backlog, as these will always be features that are more urgently needing to be completed.

    Card Labels
        Card labels are specific "tags" that we assign issues in our backlog, to help us classify them. Tags fall into several main categories, including:
        
        - Point values (rough difficulty assessment - see :term:`Scrum` for more information)
        - Team that the issue falls under (embedded, web, data science, etc.)
        - Type of work (documentation, enhancements, bug fixes, etc.)
        - Other information we want developers to know

        This allows us to quickly prioritize and select issues to work on when they are present in our :term:`Backlog`, making it generally easier to use.

    Compute Co-processor
        The compute co-processor is a generic term regarding a secondary processor on the robot, which works in parallel to the :term:`V5 Brain` that is required. The compute co-processor is generally delegated to more computationally heavy tasks, such as image processing and algorithm processing, allowing us to free up CPU bandwidth for core processes on the V5 Brain. This device is usually either a Raspberry Pi or an NVIDIA Jetson depending on compute load of the robot.

    Definition of Done
        The Definition of Done is a term to reflect the basic standards that need to be met in order for something to be considered "done". While each specific task may have unique conditions in it's own Definition of Done, there are often shared conditions between different tasks. For instance, many tasks on our team require the :term:`Engineering Notebook` to be updated before something can be declared as "done". This helps us enforce some basic management that we need done from the team, and provides a strong outline of what we need done in order to progress on an idea. Once all of the criteria in a task's Definition of Done are complete, the task can formally be declared as completed.

    Docker
        Docker is a virtualization platform used to host containers, which are small, isolated application environments that run similarly to running a separate computer. A machine can interact with it's containers over various HTTP ports, similar to how different computers communicate.

    Engineering Notebook
        The Engineering Notebook is a formal deliverable that our team curates during the entire year. As is done in a typical Engineering Notebook, we are required to document all decisions, testing, and results obtained from the season. The purpose of this document is to show how we got to where we are currently; in an ideal world, anyone should be able to *retrace our steps to achieve the same results and outcomes*. Our team uses :term:`Overleaf` to manage our notebook, which allows us to write it in :term:`LaTeX`. 

    Grooming
        (TODO)

    Issue Completion Steps
        (TODO)

    Issue Description
        (TODO)

    Issues
        Issues are how we document what needs to get done on our various projects. If we have a bug that needs to be fixed, a new feature for a product, documentation to add, or any other changes, we first create an issue to capture *what needs to get done*. This issue gets entered into it's respective :term:`Backlog`, where the team will determine how urgently it should be completed, and how it should be completed.

        Issues are synonymous with *tasks* or *Product Backlog Items (PBIs)*.

    Kanban
        (TODO)

    KiCAD
        (TODO)

    LaTeX
        LaTeX is a flavor of :term:`TeX`. LaTeX is a compiled documentation language commonly used for technical papers and reports, including our Engineering Notebook.

    MSOE Robotics
        MSOE Robotics is the professional organization used to provide STEM Opportunities to students at MSOE, through connections to student orgs, volunteering opportunities in the community, and professional development opportunities with companies and other students.

    Overleaf
        (TODO)

    PCB
        PCBs, or *printed circuit boards*, are custom boards designed with etched copper, in order to produce compact and intracate circuits. 

    Project Manager (PM)
        (TODO)

    Restructured Text (RST)
        Restructured Text (RST) is the markdown language used by our documentation website. More information on the language can be found here: (TODO)

    Robot Path File
        (TODO)

    Scrum
        (TODO)

    Sphinx
        Sphinx is the document creation tool used by our documentation site. Sphinx is responsible for creating the webpage wrapper around the :term:`Restructured Text (RST)`

    TeX
        TeX is a markdown language made to automate document formatting and styling within a text document.

    User Story
        (TODO)

    V5 Brain
        The primary processing device for our robot. Provided by VEX Robotics, we are required to use this device as the primary interface with the motors on the robot, and can use it to handle many types of input sensors. This brain include 21 smart ports with built in RS-232 communication for V5 devices, as well as 8 3-wire legacy ports on the side for sensors and extra peripherals. More information about the V5 Robot Brain `can be found here`__.

        __ https://www.vexrobotics.com/276-4810.html
