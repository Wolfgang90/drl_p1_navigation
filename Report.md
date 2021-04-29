# Report on description of implementation

## Learning Algorithm
Deep Q-Learning is employed to train the agent.

#### Chosen hyperparameters
* minibatch size: 64
* discount factor (gamma): 0.99
* tau for soft update of target parameters: 1e-3
* learning rate: 5e-4
* update frequenzy of the network: 4
* replay buffer size: 1e5
* maximum number of timesteps per episode: 300
* starting value of epsilon, for epsilon-greedy action selection: 1.0
* minimum value of epsilon: 0.01
* multiplicative factor (per episode) for decreasing epsilon: 0.995

#### Selected neural network architecture
* Network input: state-size -> 37 x 1 vector
* Number of nodes in first hidden fully-connected layer with ReLU applied: 64
* Number of nodes in second hidden fully-connected layer with ReLU applied: 64
* Number of nodes in output layer representing the potential actions: 4

## Plot of Rewards
The environment was solved within **438 episodes**.
As described in `README.md` the environment was considered to be solved, when the agent got
* an average score of +13
* over 100 consecutive episodes

#### The following plot of rewards was obtained during training:
![Alt text](plots/plot_of_rewards.png?raw=true "Title")

## Ideas for future work
Potential future work to be done:
Evaluate... 
* alternative Neural Network architectures
* double DQN
* prioritized experience replay
* dueling DQN
