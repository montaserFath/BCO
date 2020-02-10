# Behavior Cloning (BC) and Behavior Cloning from Observation (BCO)

- Implementation for Behavior Cloning (BC) and behavior cloning from observation (BCO) ([paper](https://arxiv.org/abs/1805.01954v2)) in Pytorch for [OpenAI Gym Environment](https://gym.openai.com/)

- Behavior Cloning (BC) and behavior cloning from observation (BCO) are **Imitation Learning** algorithms 

- Behavior Cloning (BC) assume that you have access to **expert's states and actions** but behavior cloning  from observation assume that you have access to **expert's States only**


## OpenAI Gym Enviroment
- Open AI Gym has several environments, We Use classical control environments [Pendulum](https://github.com/openai/gym/wiki/Pendulum-v0) and [Bipedal Walker2D](https://github.com/openai/gym/wiki/BipedalWalker-v2) environmens.

# Installing

```
pip install gym
pip install numpy
pip install box2d-py
pip install torchvision
```

## Results
![BCO VS BC Pendelum_result](https://github.com/montaserFath/BCO/blob/master/results/Scaled%20Performance%20BC%20VS%20BCO%20in%20Walker%20v2.png)

![alpha](https://github.com/montaserFath/BCO/blob/master/results/alpha%20v2.png)

## Demo

![**BC**](https://github.com/montaserFath/BCO/blob/master/demo/bc.gif)


![**BCO**](https://github.com/montaserFath/BCO/blob/master/demo/bco.gif)
