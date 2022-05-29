# JobsGraphSystem
Here's my try at implementing a parallel jobs system based on a graph of dependencies.

The plan is to be able to define a list of tasks with some dependencies between them. After that, we define a group of worker thread to execute the tasks in the right order based on the dependencies. As much as possible, tasks that don't depend on each other should be able to be ran in parallel.

Here is a quick list of initial tasks that I can think of that needs to be implemented for this to work:

* Define what is a task
    * Some function pointer
    * Some way to keep track of progress?
    * Return some unique ID to build dependencies w/ other tasks
* Create a worker threads group structure
* Build a graph of the list of tasks to complete
* Keep track of tasks and run in order
* When no more tasks are in the list, join the worker threads.
