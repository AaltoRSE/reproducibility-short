.. _index:

Reproducible research - Preparing code to be usable by you and others in the future
===================================================================================


.. admonition:: Notes for the instructor:

   This course is for new researchers, bachelors and masters students, summer
   workers and so on. The do not have a lot of experience with programming and 
   will not write long programs to start with. Emphasize reproducability of
   workflows and saving your work (instead of just running commands and getting
   results).

   Reproducability:
     - record computational steps and dependencies
     - keep data as raw as possible (in case of FIONA, raw data cannot be exported)
     - keep data and code in the same place.
     - write a workflow to reproduce the entrie paper

   Quick timings:
    - intro and motivation: 10 minutes
    - organizing-projects + git demo: 15 minutes
    - workflow-management: 15 minutes
    - dependencies and publishing: 10 minutes
    - exercises and discussion: 10 minutes
   
   10 + 15 + 15 + 10 + 10 = 60 minutes   

Have you ever **lost hours of work** when your computer decided to update itself?
Or a program crashed when you clicked save? Did you maybe delete a file by mistake?

In this section we will look at ways of saving your work for yourself and saving 
effort by making computational steps easy to repeat, share and modify. Making you
research project reproducible increase the quality of your work, but the main
motivation should be to make your life easier in the long run.

In this lesson we will explore different methods and tools for better
reproducibility in research software and data. We will demonstrate how version
control, workflows, and package managers can be used to **record
reproducible environments and computational steps** for our future selves
and share those with other researchers.


.. admonition:: Learning outcomes

  By the end of this lesson, learners should:
    - be able to apply well organized directory structure for their project
    - be able to document and reproduce computational steps
    - understand that code can have dependencies, and know how to document them
    - if a computational study contains several steps, be able to document them


.. prereq::

   In examples and demonstrations, we use
   `Git, Python, and Snakemake <https://coderefinery.github.io/installation/>`__.
   These are not required to follow the lesson, but trying them yourself is very
   useful


.. toctree::
   :maxdepth: 1
   :caption: Core episodes

   intro.md
   motivation.md
   organizing-projects.md
   workflow-management.md
   dependencies.md
   where-to-go.md


.. toctree::
   :maxdepth: 1
   :caption: For Reference

   exercises
   guide


.. toctree::
   :maxdepth: 1
   :caption: See Also

   Codefinery Lessons <https://coderefinery.org/lessons/core/>
   This lesson is based on the `Reproducibility lesson <https://coderefinery.org/lessons/core/>`__
   CodeRefinery Organization <https://coderefinery.org/>
