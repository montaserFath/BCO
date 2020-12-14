# Behavior Cloning (BC) and Behavior Cloning from Observation (BCO)

- Implementation for Behavior Cloning (BC) and behavior cloning from observation (BCO) ([pdf](https://arxiv.org/abs/1805.01954v2)) in Pytorch for [OpenAI Gym Environment](https://gym.openai.com/)

- Behavior Cloning (BC) and behavior cloning from observation (BCO) are **Imitation Learning** algorithms 

- Behavior Cloning (BC) assume that you have access to **expert's states and actions** but behavior cloning  from observation assume that you have access to **expert's States only**

## How it works?

**1- Collecting data**:

- **Learner**: exploration policy, save states and actions

- **Expert**: train expert (if you don’t have one), save states only.

- **all data available** [here](https://bit.ly/37AoBlR)

**2- Train Inverse dynamic model (T)**:

- **Input**: Learner current state and Learner next state.

- **Output**: predicted Learner current action.

- **Loss function**: MSE, L1loss or NLL (predicted Learner current action, Learner current action).

**3- Test: Inverse dynamic model (T):**

- **Input**: Expert current state and Expert next state

- **Output**: predicted Expert current action.

**4- Train Behaviour model (policy):**

- **Input**: Expert current state.

- **Output**: prediction of predicted Expert current action.

- **Loss**: MSE, L1loss or NLL (prediction of predicted Expert current action, predicted Expert current action).

**5- Learner interacts with environment BCO(alpha):** 

- Learner use Behaviour model (policy) to get action given current state.

- Collect new data (states and actions)

- Use collected data to update Inverse dynamic model (T) and Behaviour model (policy) (repeat 2, 3, and 4)



## OpenAI Gym Enviroment
- Open AI Gym has several environments, We Use classical control environments [Pendulum](https://github.com/openai/gym/wiki/Pendulum-v0) and [Bipedal Walker2D](https://github.com/openai/gym/wiki/BipedalWalker-v2) environmens.

# Installing

```
pip install gym
pip install numpy
pip install box2d-py
pip install torchvision
```
# Data

- [Pendulum](https://github.com/openai/gym/wiki/Pendulum-v0) and [Bipedal Walker2D] (https://github.com/openai/gym/wiki/BipedalWalker-v2) Exploration States and actions, also expert states you can download it from [here](https://bit.ly/37AoBlR)

## Results
![BCO VS BC Pendelum_result](https://github.com/montaserFath/BCO/blob/master/results/Scaled%20Performance%20BC%20VS%20BCO%20in%20Walker%20v2.png)

![alpha](https://github.com/montaserFath/BCO/blob/master/results/alpha%20v2.png)

## Demo

![**BC**](https://github.com/montaserFath/BCO/blob/master/demo/bc.gif)


![**BCO**](https://github.com/montaserFath/BCO/blob/master/demo/bco.gif)
