# Tennis_bots
Implementing Multi-robot collaborative reinforcement algorithm DDPG to solve reacher problem. Goal of the project was to gain 0.5 points over 100 episodes.
Where agent gets 0.1 point for clearing the ball to other side.

### Output of the algorithm with collabrative multi-agent system.

<img src="https://github.com/harshkakashaniya/Tennis_bots/blob/main/images/Tennis.gif" width="800"/>


If you want to train your own model you will refer the file.

[Training program](https://github.com/harshkakashaniya/Tennis_bots/blob/main/scripts/Tennis.ipynb)

## Details of environment :
```
Number of agents: 2
Size of each action: 2
There are 2 agents. Each observes a state with length: 24
```
In this environment, two agents control rackets to bounce a ball over a net.

### State Space :

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.

### Action Space :

Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

### Reward :

If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

### Solving criterias of the problem. 

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Setup environment:

1. First we have to install conda once the conda is installed we need to update the bash script.  [Install anaconda](https://docs.anaconda.com/anaconda/install/linux/)

2. Run the following commands in the terminal.
```
conda create --name drlnd python=3.6
source activate drlnd
```

3. Clone the environment repo:
```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Clone this repo :
```
git clone https://github.com/harshkakashaniya/Tennis_bots
cd Tennis_bots
```

5. Setup drlnd environment :
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```
6. Finally open the Jupyter noetbook :

```
jupyter notebook
```

And select the appropiate file to train or test the model.
(Eg. scripts >> Tennis.ipynb)

**Note : Do not forget to select Kernal >> Change kernal >> drlnd**

7. Edit the location of Tennis linux in code cell 2 and run the notebook( Hit  **Shift + Enter**) 


## Project Report :

[Architecture and project report](https://github.com/harshkakashaniya/Tennis_bots/blob/main/Report.md)

## Results :

### Our Average score vs Episodes.

![](https://github.com/harshkakashaniya/Tennis_bots/blob/main/images/graph.png)
