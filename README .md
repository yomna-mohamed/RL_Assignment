
# Project Title

 Using the Q-learning approach with Open AI Gym and selecting an environment like ("Taxi-v3"),to Teach a Taxi to pick up and drop off passengers at the right locations with Reinforcement Learning ,and Getting the hyper parameter tunning (alpha, gamma,epsilon) that affects on environment as we want to choose parameters which enable us to get the maximum reward as fast as possible. 


## Installation

    !pip install cmake 'gym[atari]' scipy
## Features

1- Generlization : 
  -Brute_force_approach(env,s): fuction that takes an environment and state this solving the environment without Reinforcement Learning
     - Results (Time steps taken ,Penalties incurred)
  - Training the Agent by Q_learning_approach, training(env,s): fuction that takes an environment and state this solving the environment by Reinforcement Learning the function takes an environment and the three parameters (alpha and gamma and epsilon)like this : training (env,a,g,e) , where alpha is the learning rate ,gamma is the discount factor
     - Results : The Q-table is a matrix where we have a row for every state (500) and a column for every actions in 6 action that we have  (south,north ,east,west ,pickup,dropoff ) 
  -Evaluating the agent ,evaluation (q_table,env) : this function that takes a q_table and the environment , this fuction evaluates the performance of our agent. We don't need to explore actions any further, so now the next action is always selected using the best Q-value
     -Results :this fuction return Average timesteps per episode and Average penalties per episode and Average rewards.
2- Tunning :The values of `alpha`, `gamma`, and `epsilon` , all three should decrease over time because as the agent continues to learn, give to parameters (alpha , gamma, epsilon)different values from (0.1 :0.9) and try which parameters will affect in the environment 
3- Hyper Parameter Tunning: making a grid search and try which parameters will give us highest evaluation by using this formula (rewords/(avr_penalties+avr_time_stampe)) 
     using the grid search list in training and evaluation to choose parameters which enable us to get the maximum reward as fast as possible. 
     -Results:which Parameter we can choose parameters which enable us to get the maximum reward as fast as possible. 
Note the hyper Parameter Tunning takes more than 3 hours to train the Agent with 3 values for every parameter