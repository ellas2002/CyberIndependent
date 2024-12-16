## Chapter 4 Dynamic Programming
1. **Dynamic Programming** (DP): a collection of algos taht can be used to comute optimal policies given a eprfect model of the enviornment as a MDP
   - Classical DP algos
      - limited utility in reinforcement learning because of
        -  assumption of a perfect model
        -  great computational expense
        -  
2. approximate solitons for continuous tasks
   - quantize the state and action spaces and then apply finite-state DP methods
   
3. key idea of DP
   - use of value functions to organize and structure the search for good policies



### 4.5 Asynchronous Dynamic Programming
1. drawback to DP methods
   - involve operations over the entire state of the MDP (require sweeps of the state)
