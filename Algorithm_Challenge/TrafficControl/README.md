# Traffic Light Problem (1 hour)

There's a busy traffic intersection outside your building. The roads at the intersection are horizantal street and vertical street. 
You are an engineer with the department of transportation and you're trying to come up with a new traffic light pattern that 
prevents cars from crashing in the intersection but also minimizes traffic jams. 

Your goal:
- Get all the cars safely through the intersection in less than 2 minutes.
- Minimize the cumulative time that each car waits at the intersection

You will additionally be assessed on:
- The quality of your code

A few things to note about the simulation:
- Cars waiting to go into the intersection can only move into the intersection if the light is green.
- Cars already in the intersection can move out of the intersection even when the light is red or yellow.
- A crash will occur if a car on horizantal street and a car on vertical street are in the intersection at the same time.
- Cars IN the intersection are denoted with an 'X'. Cars on either side of the intersection are denoted with a '+'. 
  This will make more sense once you try running the program.
- Only one car from each lane can be IN the intersection at once. For example, if two cars are waiting in the eastbound 
  lane to cross the intersection, they cannot both move into the intersection at the same time. The first car in the 
  lane will move into the intersection. Then, the second car will move into the intersection as the first car leaves. 

To build the project, type the following in your bash terminal:
gcc traffic_light_problem.c -o traffic_light_problem

To run the project, type the following in your bash terminal:
./traffic_light_problem.exe

Candidate Action Items:
- Fill in the two unfinshed functions at the beginning of the file: 
  - char * setHorizantalTrafficLight(struct intersection_s intersection) and 
  - char * setVerticalTrafficLight(struct intersection_s intersection)
  If you need to add additional variables, structures, functions, etc, that's fine. However, with the exception of the 
  above two functions, please do not edit the code that's already in the files, unless you are extremely certain that 
  there's a bug in the code.
- Briefly describe your implementation (1-3 sentences).
  - High level: Code adjusts the light durations based on "real-time" traffic data in a data-driven adaptive control kind of way; this is done in the calculateGreenDuration function
  - Mid level: Finite state machine controls light change between vertical and horizontal; done in setHorizantalTrafficLight/setVerticalTrafficLight functions using a global variable
  - Low level: The timer makes sure that there are no collisions. And other aspects run by different parts of code; also done in setHorizantalTrafficLight/setVerticalTrafficLight functions

Don't forget; we are interested in both your solution and your thought process.

Good Luck!