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
- For each wildfire that breaks out, associate a priority value (lower value means higher priority) and the number of required resources to extinguish the fire.
- Use a thread to monitor the landscape for any wildfires.
- If a wildfire is detected, notify the parent process through inter-process communication.
- Use semaphores or mutexes to lock any critical sections
- Have parent process dispatch resources to wildfire location to extinguish the fire.
- Once a fire is extinguished, the value at that position will be set back to 0.

# Significance and Novelty of Project
This project is significant because it meets the requirements of the of the project in a novel way based on the theme of wildfires. Critical and creative thinking were utilized to come up with a project idea that covers all the major topics learned throughout the semester including creating child processes, creating threads, using inter-process communication, and using locking mechanisms to lock critical sections.
# Installation and Usage Instructions

# Code Structure

# List of Functionalities and Verification Results

# Showcasing the Achievement of Project Goals

# Discussion and Conclusion
