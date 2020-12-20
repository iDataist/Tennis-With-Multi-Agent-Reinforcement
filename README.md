# Tennis With Multi Agent Reinforcement

In this project, I trained two agents to play tennis.

## Reinforcement Learning Environment

Unity Machine Learning Agents (ML-Agents) is an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents. The image below shows the [tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment for this project.

![](tennis.png)

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents).

## Getting Started

1. Create the Conda Environment

    a. Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer, by selecting the latest Python version for your operating system. If you already have `conda` or `miniconda` installed, you should be able to skip this step and move on to step b.

    **Download** the latest version of `miniconda` that matches your system.

    |        | Linux | Mac | Windows |
    |--------|-------|-----|---------|
    | 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
    | 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

    [win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
    [win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
    [mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
    [lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
    [lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

    **Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

    - **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
    - **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
    - **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install

    b. Install git and clone the repository.

    For working with Github from a terminal window, you can download git with the command:
    ```
    conda install git
    ```
    To clone the repository, run the following command:
    ```
    cd PATH_OF_DIRECTORY
    git clone hhttps://github.com/iDataist/Tennis-With-Multi-Agent-Reinforcement
    ```
    c. Create local environment

    - Create (and activate) a new environment, named `maddpg-env` with Python 3.7. If prompted to proceed with the install `(Proceed [y]/n)` type y.

        - __Linux__ or __Mac__:
        ```
        conda create -n maddpg-env python=3.7
        conda activate maddpg-env
        ```
        - __Windows__:
        ```
        conda create --name maddpg-env python=3.7
        conda activate maddpg-env
        ```

        At this point your command line should look something like: `(maddpg-env) <User>:USER_DIR <user>$`. The `(maddpg-env)` indicates that your environment has been activated, and you can proceed with further package installations.

    - Install a few required pip packages, which are specified in the requirements text file. Be sure to run the command from the project root directory since the requirements.txt file is there.
        ```
        pip install -r requirements.txt
        ipython3 kernel install --name maddpg-env --user
        ```
    - Open Jupyter Notebook, and open the Continuous_Control.ipynb file. Run all the cells in the jupyter notebook to train the agents.
        ```
        jupyter notebook
        ```
2. Download the Unity Environment

   a. Download the environment from one of the links below.  You need only select the environment that matches your operating system:

    - Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

    (For Windows users) Check out this [link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use this [link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual screen, and then download the environment for the Linux operating system above.)

    b. Place the file in the folder with the jupyter notebook, and unzip (or decompress) the file.

## File Descriptions

1. [requirements.txt]() - Includes all the required libraries for the Conda Environment.
2. [model.py](https://github.com/iDataist/Tennis-With-Multi-Agent-Reinforcement/blob/main/model.py) - Defines the actor and critic networks.
3. [agent.py](https://github.com/iDataist/Tennis-With-Multi-Agent-Reinforcement/blob/main/agent.py) - Defines the Agent that uses MADDPG to determine the best action to take and maximizes the overall or total reward.
4. [Tennis.ipynb](https://github.com/iDataist/Tennis-With-Multi-Agent-Reinforcement/blob/main/Tennis.ipynb) - The main file that trains the agents. This file can be run in the Conda environment.

