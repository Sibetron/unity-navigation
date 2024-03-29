[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

### Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the DRLND GitHub repository, in the `unity-navigation/` folder(which we will clone below), and unzip (or decompress) the file. 


### Install Dependencies
To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

- Linux or Mac:
```
conda create --name drlnd python=3.6 
source activate drlnd
```
- Windows:
```
conda create --name drlnd python=3.6 
activate drlnd
```
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.

    - Next, install the classic control environment group by following the instructions [here.](https://github.com/openai/gym#classic-control)
    - Then, install the box2d environment group by following the instructions [here.](https://github.com/openai/gym#box2d)

3. Clone the repository (if you haven't already!), and navigate to the python/ folder. Then, install several dependencies.
```
git clone https://github.com/Sibetron/unity-navigation.git
cd unity-navigation/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the drl environment.
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the```drlnd``` environment by using the drop-down ```Kernel``` menu.
Kernel

![alt text](https://github.com/Sibetron/unity-navigation/blob/master/kernel.png?raw=true)

### Instructions

Execute the cells in `Navigation.ipynb`. The File has the following 5 sections,

#### 1. Start the Environment

Here we import the needed packages for our project and start the environment by running the banana.exe for windows and banana.app for Mac OS

#### 2. Examine the state and action spaces

We get the state and action spaces values from the environment.
#### 3. Take random actions in the environment
Here we see the agent in action when it takes random actions before training.

#### 4. Train the Agent to Collect Yellow Bananas
In this training process we pass the parameters to the dqn_agent.py and get the state, actions, reward, etc. We loop through the training process and print the average score. The model is set to save in checkpoint.pth when the average score is >=15. 

#### 5. Observe the Agent in Action
We load the best model from checkpoint.pth and test the agent.





