Following methods have been used for training agent:

* Replay buffer contains 100,000 number of set of (state, action, reward, next state, done)

* Epsilon greedy policy has been used to explore and exploit actions from given state. start epsilon value is 1.0 and end epsilon value is 0.01 with 0.995 epsilon decay.

* create Multilayer Artificial neural network using pytorch

* Architecture: 
[ Input(37) -> dense(64) -> dense(64) -> output(4) ]
with relu activation

* Training the model using double DQN method to get proper Q value with 2000 episodes,1000 maximum number of step per episode, 64 batch size, 0.0005 learning rate and 0.99 discount factor.

* In the end of the code, if average reward of last 100 episode is greater than 13, training would be stopped and save current weights with plotting average reward graph over the training. 

You can see output graph in [Navigation.ipynb](https://github.com/TapanBhavsar/Navigation_DRLND/blob/master/Navigation.ipynb)

For Future scope, Dueling network can be used because the training time in double DQN method is time consuming compare to Dueling network. there are more nagetive reward samples in replay buffer so that problem can be reduced using priortize experience replay method.   
