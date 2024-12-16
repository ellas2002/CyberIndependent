## Chapter 4 Dynamic Programming
1. **Dynamic Programming** (DP): a collection of algos that can be used to compute optimal policies given a perfect model of the enviornment as a MDP
   - Classical DP algos
      - limited utility in reinforcement learning because of
        -  assumption of a perfect model
        -  great computational expense
        -  
2. approximate solutions for continuous tasks
   - quantize the state and action spaces and then apply finite-state DP methods
   
3. key idea of DP
   - use of value functions to organize and structure the search for good policies



### 4.5 Asynchronous Dynamic Programming
1. drawback to DP methods
   - involve operations over the entire state of the MDP (require sweeps of the state set)
     - large state set = single sweep expensive

2. **Asynchronous** DP algoritms are in place iterative DP algorithms
   - update values of states in any order, using whatever value is available
      - cannot ignore an state opdate after some point in the computation
      - allows for flexibility in selecting states to update
    
3. Asynchronous allows us not to get stuck in a long sweep before it can improve a policy
    - to take advantage of this:
       - select states to which we apply updates to improve the algo's rate of progress
       - order the updates to let calue info propagaate from state to state
       - try skipping updates for states if they are not relevant to optimal behavior

4. Asynchronous makes it easier to intermix computation with real time interaction
   - run an iterative DP algo at the same tima of an agent experiencing the MDP
      - agents expereinces can determine the states the DP applies its updates
      - latest balue and policy info from DP algo can guide agent's decision making
    

### 4.6 Generalized Policy Iteration
