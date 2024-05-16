# Elevator Problem (1 hour)

It's lunch time in your building and the elevator's broken. You are an engineer with elevator maintainance department and 
you're trying fix the elevator and program it to pick up and drop off the people in the building in the most efficient way.  

Your goal:
- Get all the people in the building to their destinations in less than 1 minute.

You will additionally be assessed on:
- The quality of your code
- The time it takes to for your simulation to finish

A few things to note about the simulation:
- The elevator will start on a random floor
- The elevator has a max capacity of 3 people
- The building has 5 floors
- It takes 1 second for the elevator to move to an adjacent floor (i.e. moving from floor 1 to floor 2 takes 1 second)
- It takes 3 seconds for the elevator to stop at a floor (i.e. opening the doors, letting people on/off, and closing the 
  doors takes 3 seconds)
- If the elevator stops at a floor, everyone who can get off will, and everyone who can get on will. If not everyone who 
  wants to get on will fit, the person first in line will get preference.
- The destinations of people waiting on a floor or in the elevator are represented by an array. A value of -1 in those 
  arrays means there is no one in that spot. (Note: This should only be true for instances of the 'passengers' and 
  'departures' arrays)
- People who get off the elevator and arrive on their destination floor should be visually denoted by an 'x' on the 
  arrivals side of the simulation. Within the code, the number of people who've arrived on a floor is represented as 
  an integer variable within the floor_s structure. 

To build the project, type the following in your bash terminal:
gcc elevator_problem.c -o elevator_problem

To run the project, type the following in your bash terminal:
./elevator_problem.exe

Candidate Action Items:
- Fill in the unfinshed function at the beginning of the file: 
  - int8_t setNextElevatorStop(struct building_s building) 
  If you need to add additional variables, structures, functions, etc, that's fine. However, with the exception of the 
  above function, please do not edit the code that's already in the files, unless you are extremely certain that 
  there's a bug in the code.
- Briefly describe your implementation (1-3 sentences).
  - Use SCAN method to find eligible floor to stop
  - Skips floors when the elevator is full or when a floor is empty/not requested
  - Uses conditional statements to achieve solution. Simulates in each direction then decides to avoid getting stuck at the top and bottom floor

Don't forget; we are interested in both your solution and your thought process.

Good Luck!