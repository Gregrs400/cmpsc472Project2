## Project Theme: 
Wild Fire

## Aspects of wild fire to explore:
- detection and monitoring
- resource allocation
- evacuation planning
- data logging/real-time analysis
- simulation and forecasting
- emergency communication systems

## What needs to be included:
- user-friendly interface
- comments to explain design/implementation
- project report (must be .md file in GitHub repo)
	- goals
	- info on why the project is meaningful and novel
	- installation and usage instructions
	- systematic flowchart of code structure with explanations
	- list of functionalities and verification results
	- project results that demonstrate you've achieved your project goals
	- discuss project issues, limitations, and how course concepts were applied

## Course Concepts to apply:
- child processes using fork()
- threads using pthread_create()
- interprocess communication via pipes or shared memory
- mutex/semaphores for critical sections

# Potential Idea:
- Have a global pool of resources used to fight wildfires
- Have a 2D array of 0's to represent land, and randomly choose positions within this array to have the value of 1. A value of 1 represents a wildfire.
- For each wildfire that breaks out, somehow associate two values with it: one value to represent the number of resources needed from the global resource pool to extinguish the fire, and a priority. Lower priorities go first.
- Either use multiple processes or threads to deal with these wildfires, where each process or thread uses some of the global resources to extinguish the fires.
- Use interprocess communication to communicate to other processes or threads that a wildfire is being dealt with.
- Use semaphore/mutex locks to lock any critical sections. An example of a critical section could be taking incrementing or decrementing the global resource variable.
- Once a wildfire is extinguished, add the resources back to the pool of resources. A wildfire is extinguished when a 1 is set back to 0. 