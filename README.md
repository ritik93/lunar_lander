## The Lunar Lander Environment

In this project we will be using [OpenAI's Gym Library](https://www.gymlibrary.ml/).  
The Gym library provides a wide variety of environments for reinforcement learning.  
To put it simply, an environment represents a problem or task to be solved. In this project, we will try to solve the Lunar Lander environment using reinforcement learning.  

The goal of the Lunar Lander environment is to land the lunar lander safely on the landing pad on the surface of the moon.   
The landing pad is designated by two flag poles and it is always at coordinates `(0,0)` but the lander is also allowed to land outside of the landing pad. The lander starts at the top center of the environment with a random initial force applied to its center of mass and has infinite fuel.  
  
The environment is considered solved if you get `200` points.  
  
### Action Space

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
```  
  
### Observation Space

The agent's observation space consists of a state vector with 8 variables:

* Its $(x,y)$ coordinates. The landing pad is always at coordinates $(0,0)$.
* Its linear velocities $(\dot x,\dot y)$.
* Its angle $\theta$.
* Its angular velocity $\dot \theta$.
* Two booleans, $l$ and $r$, that represent whether each leg is in contact with the ground or not.
  
  
### Rewards

The Lunar Lander environment has the following reward system:

* Landing on the landing pad and coming to rest is about 100-140 points.
* If the lander moves away from the landing pad, it loses reward. 
* If the lander crashes, it receives -100 points.
* If the lander comes to rest, it receives +100 points.
* Each leg with ground contact is +10 points.
* Firing the main engine is -0.3 points each frame.
* Firing the side engine is -0.03 points each frame.
  
  
### Episode Termination

An episode ends (i.e the environment enters a terminal state) if:

* The lunar lander crashes (i.e if the body of the lunar lander comes in contact with the surface of the moon).

* The lander's $x$-coordinate is greater than 1.  
  
  
  
For a complete description of the environment, check out the [Open AI Gym documentation](https://www.gymlibrary.ml/environments/box2d/lunar_lander/)

