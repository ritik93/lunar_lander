## The Lunar Lander Environment

In this project we will be using [OpenAI's Gym Library](https://www.gymlibrary.ml/).  
The Gym library provides a wide variety of environments for reinforcement learning.  
To put it simply, an environment represents a problem or task to be solved. In this project, we will try to solve the Lunar Lander environment using reinforcement learning.  

The goal of the Lunar Lander environment is to land the lunar lander safely on the landing pad on the surface of the moon.   
The landing pad is designated by two flag poles and it is always at coordinates `(0,0)` but the lander is also allowed to land outside of the landing pad. The lander starts at the top center of the environment with a random initial force applied to its center of mass and has infinite fuel.  
  
The environment is considered solved if you get `200` points.  
  
### 3.1 Action Space

The agent has four discrete actions available:

* Do nothing.
* Fire right engine.
* Fire main engine.
* Fire left engine.

Each action has a corresponding numerical value:

```python
Do nothing = 0
Fire right engine = 1
Fire main engine = 2
Fire left engine = 3
