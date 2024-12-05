# Table of Contents
- [Project Goals](#project-goals)
-  [Significance and Novelty of Project](#significance-and-novelty-of-project)
-  [Installation and Usage Instructions](#installation-and-usage-instructions)
-  [Code Structure](#code-structure)
-  [List of Functionalities and Verification Results](#list-of-functionalities-and-verification-results)
-  [Showcasing the Achievement of Project Goals](#showcasing-the-achievement-of-project-goals)
-  [Discussion and Conclusion](#discussion-and-conclusion)

# Project Goals
## Idea
Our overall project idea aims to represent a landscape that is monitored for wildfires. If a wildfire breaks out, it will be detected and available resources will be dispatched to extinguish the fire. 

## Goals
- Generate a 2D array of 0's to represent a landscape with no wildfires.
- Include a global pool of limited resources to fight wildfires.
- Randomly generate a wildfire within the landscape every 1 to 10 seconds. Wildfires will be represented by 1's within the landscape.
- For each wildfire that breaks out, associate the number of required resources to extinguish the fire.
- Use a thread to monitor the landscape for any wildfires.
- If a wildfire is detected, notify the parent process through inter-process communication.
- Use semaphores or mutexes to lock any critical sections
- Have parent process dispatch resources to wildfire location to extinguish the fire.
- Once a fire is extinguished, the value at that position will be set back to 0.

# Significance and Novelty of Project
This project is significant because it meets the requirements of having a theme of wildfires and including important concepts learned throughout the course including child processes, threads, inter-process communication, and locking mechanisms to lock critical sections. Critical and creative thinking were utilized to come up with the idea that a 2D array can be used to represent a landscape where a 0 represents a section of the landscape not burning and a 1 represents a section of the landscape actively burning. The concept of creating a child process was utilized to create threads to monitor the landscape for any fires that break out. The concept of inter-process communication via pipes is being used to send information about wildfires discovered throughout the landscape from the child process to the parent process. With this communicated information the parent process will then send out firefighting resources to the wildfires. The concept of applying a locking mechanism to the firefighting resources is being used to prevent synchronization issues when accessing the global firefighting resources. Overall, the project is significant and novel due to the way that all project requirements are met and implemented in a unique and meaningful way.

# Installation and Usage Instructions
The code for this project is located within a Google Colab, so there is no need to install anything to run this code.  

To use this program, all the user has to do is click the 'Run cell' button on the cell block containing all the C source code. Once this step is complete, navigate to the smaller code cell block and click that cell's 'Run cell' button. After selecting the 'Run cell' button, the program will run automatically, and the user won't have to perform any further actions. The program will automatically generate a landscape, have fires spawn throughout that landscape, detect those fires, have resources delivered to those fires to extinguish them, and display the results.  

# Code Structure
The structure of the code is intended to follow good programming practices such as readability, reusability, comments, and modularity. To accomplish this, the code contains a main function, several additional functions, two structs, and comments to explain different lines of code. 

The main function begins by creating an array of file descriptors for inter-process communication, creating the landscape using the Landscape struct, and setting random spots throughout the landscape on fire. A Fire struct is used to store the row and column of a fire and how many resources needed to extinguish the fire. Once all fires are set, a child process is created. The code is structured so the child process can create threads to search the landscape for fires and communicate the fire location and the number of resources for the fire to the parent process via a pipe. At the same time, the parent process runs in a loop to listen for all fires reported from the child process. Once the child process finishes its search of the landscape, it will send a message to the parent process, and upon receiving this message, the parent process will break out of the loop. To ensure the child process finishes first, the parent process then immediately calls a wait command. Once the child process has finished executing, the parent process will use the information passed to it to dispatch resources to the wildfires throughout the landscape to extinguish them. 

# List of Functionalities and Verification Results

# Showcasing the Achievement of Project Goals

# Discussion and Conclusion
