# Reinforcement Learning (Richard S. Sutton; Andrew G. Barto)

## Introduction

1. Important points:
    - Direct sensorimotor connection: direct pathway from the sensory to motor cortex: allows sensory input to influence motor output
      - Looked at as the way we learn information about environment and self

     
### 1.1 Reinforcement Learning
1. Machine learning paradigms
   ```
   Supervised
   unsupervised 
   reinforcement
   ```


3. Reinforcement Learning: learning what to do (map situations to actions) to maximize a numerical reward signal
	 - Learner has to discover what action yields the most value by trying them out
      - Two most important features for this type of learning
        - Trial and error search
        - Delayed reward
          - Idea that an immediate action can affect the next situation…etc.


4. Unsupervised vs supervised learning
    - **Supervised**:
      - learn from training set of guiding examples given by a supervisor
        - Not good in interactive environment
          -  Got to learn from experience 
    - **Unsupervised** can be about fading structures hidden a lot of unlabeled data

5. Challenge for reinforcement learning:
    - Will have to make mistakes or fail 
      - Have to balance exploration and exploitation
        - **Exploration**
          - Has to choose to do things it hasn't before to find better option
        - **Exploitation**
          - Choosing to do things that worked out in the past


6. Key feature of reinforcement learning
    - Considers the whole problem 
      - Other paradigms consider goals ...`Which is a limitation`

      - Agents have 
        ```
        Specific goals
        Senses aspects of the env
        Can choose action that affect env
        Starts out with no info about env
        Has to make decisions about now and future
        ```
        
### 1.3 Elements of Reinforcement Learning

1. Main sub-elements of a reinforcement learning system
   - **Policy:**
      `Agents way of behaving a given time`
       - May be stochastic
         
    - **Reward signal:** `What's good immediately `
      - Each time step, env sends a reward (single number) to agent
      - Agents wants to maximize that reward
        - May be stochastic
          
    - **Value function:** `What's good in the long run`
      - Will be estimated and re-estimated based on observations from their lifetime
        
    - **Model**
      - Allows for inferences about how an env behaves
      - Used for planning
     
        
### 1.4 Limitations and Scope
1. Relies heavily on state
  - State is whatever info is available to agent about env
    - Book is looking deciding what action to take as a function of whatever state signal is available 

## Part 1: Tabular Solutions Methods
1. State and actions spaces are small
  - Can be represented as arrays or tables
  - Methods can then find the optimal value function and policy


### Chapter 2: Multi-armed bandits

1. Important difference about reinforcement
  - Evaluates the action rather than by instruction
  - Evaluative feedback cs instructive
  - Evaluate indicates how good the action taken was
2. Action taken
  - Instructive indicates best or worst action taken
  - Independent of action

### 2.1 A k-armed Bandit Problem

1. Idea
  - Faced with a choice with k different options/action
    - Each choice gives you a numerical reward
      - Which is chosen from a stationary probability distribution that depends on action selected 
    - Goal is to maximize expected total reward
          - E.g. slot machine

2. K action has a expected or mean reward when an action is selected \n
```
    q⇤(a) . = E[Rt |At=a].
```
_At_ = value of action selected on timestamp t

_Rt_ = corresponding reward

_A_ = arbitrary action

_q⇤(a)_ = expected reward given taht a is slected
     - if you know the values, always select action with hightest value
  - we want :

    ` Qt(a) to be close to q⇤(a).`
  - mainting estimates of action values at any time stamp, allows for you to select the action wiht highest value
    - this is called a **greedy action**
      - doing so means you are **exploiting** your current knowledge
        - right thing to do to maxmize the expected reward
      - nongreedy items mean you are **exploring**
        - right thing to do to produce greater total reward in long run

### 2.2 Action-value methods
1. **action value methods** : method for estimating values of action and for using the estimates to make action selection decisions

true value of an action = mean reward that action is selected

`Qt(a) . = sum of rewards when a taken prior to t / number of times a taken prior to t`



       
           
     
      - 
    
     
