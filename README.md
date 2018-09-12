# Navigation_DRLND
  Navigation project of UDACITY's Deep Reinforcement learning NanoDegree

## Requirement

1. Python version: **python3**.
2. Install **Jupyter notebook**.
> 1. Numpy (pip3 install numpy)
> 2. matplotlib (pip3 install matplotlib)
> 3. pytorch (pip3 install torch torchvision)

## Description:

[Environment](https://github.com/TapanBhavsar/Navigation_DRLND/tree/master/python) has been provided in project 1 by Udacity. 37 states and 4 actions havew been fetched from given environment and fed to agent explain in [Navigation.ipynb](https://github.com/TapanBhavsar/Navigation_DRLND/blob/master/Navigation.ipynb) 

Run first three cell in [notebook](https://github.com/TapanBhavsar/Navigation_DRLND/blob/master/Navigation.ipynb) to load Environment. 
> **DO NOT RUN CELL NO 6**
```
env.close()
```

Following methods have been used for training agent:
* Replay buffer contains 100,000 number of set of (state, action, reward, next state, done)
* Epsilon greedy policy has been used to explore and exploit actions from given state. start epsilon value is 1.0 and end epsilon value is 0.01 with 0.995 epsilon decay.
* create Multilayer Artificial neural network using pytorch
* Architecture: 
[ Input(37) -> dense(64) -> dense(64) -> output(4) ]
with relu activation
* Training the model using double DQN method to get proper Q value with 2000 episodes,1000 maximum number of step per episode, 64 batch size, 0.0005 learning rate and 0.99 discount factor.
* In the end of the code, if average reward of last 100 episode is greater than 13, training would be stopped and save current weights with plotting average reward graph over the training. 
