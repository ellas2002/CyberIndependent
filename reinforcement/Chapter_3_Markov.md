# Chapter 3 Finite Markov Decision Processes

## 3.2 Goals and Rewards

1. purpose (goal) of agent is formalized in terms of a special signal (_reward_)
   - _reward hypothesis_
     - agent's goal is to maximize the cumlative reward in the long run
       - at each time step: R<sub>t</sub> ∈ R .
      
    - the _reward signal_ is there to show the agent how to achieve what we want it to do
       - avoids telling the agent what you want it to achieve
         - this can lead the agent to find another way of achieving without actually achieving the goal
        
## 3.3 Returns and Episodes

1. reinforcement learning seeks to maximize the _expected return_

   ```return sum of all rewards: G<sub>t</sub>.= R<sub>t+1</sub>  + R<sub>t+2</sub>  + R<sub>t+3</sub> + · · · + R<sub>t</sub>```

   T is final time step

   - this works if the agent-env interaction breaks into subsequces (_episodes_)
     - each episode ends on a special state (_terminal state_)
       - this is followed by a reset to a standard starting state or a sample from a standard distribution starting states
         - next episode starts independently of the previous episode
            - will have its own rewards or outcomes (this type of task is call _episodic tasks_)
          

  2. agent-env interaction is without episodes and goes on continually without limit (_continuing tasks_)
     - the final time step would be T = inf and the return could be infinite
     - additional concept is _discounting_
       - this approach: agent tries t select actions so that the sum of the discounted rewards it recieves over the future is maximized
      
        ``` see math on page 55 ```
          - discount rate determins the present value of guture rewards


  ## 3.4 Unified Notation for Episodic and Continuing Tasks
      
         

        
