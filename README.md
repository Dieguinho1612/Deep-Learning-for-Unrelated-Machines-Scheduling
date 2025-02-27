# Theory

The entire theoretical background as well as the obtained results will be explained in a paper, being hold for submission right now.

<ins>Probem:</ins><br>
We treat Job Scheduling Problems on Unrelated Machines with an initial occupation and deterministic processing times. Both, Jobs and Machines, have deadlines and weights. We want to minimize the makespan added to the weigthed sum of the Job and Machine tardinesses.<br>

<ins>Approach:</ins><br>
Our approach is to apply Deep Reinforcement Learning. We will embed these problems into a markovian environment with every decision situation being a state. Policies are identified with scheduling rules. We compute the true Q-values with brute force for Job Scheduling Problems with 8 Jobs and 4 Machines. We exctract the data from these simulated states and use them to supervisedly train a Neural Network. This Neural Network contains architectures of Natural Language Processing models to handle the variability of the dimension in the data due to changing numbers of Jobs and Machines. By using it as a Target Network, we can then apply Deep Reinforcement Learning techniques. Therefore, we iteratively estimate data of Job Scheduling Problems with higher Job numbers and uptrain the Network.<br>

<ins>Results:</ins><br>
We compare the scheduling costs obtained by our Neural Network to the optimal costs. We will find that they do not differ much. We then compare them to a heuristic scheduling algorithm and conclude that our Neural Network vastly outperforms it.<br>

# Code

All the code is written in Python 3 and uploaded as Jupyter [Notebooks](https://github.com/Dieguinho1612/Job-Scheduling-Deep-Reinforcement-Learning/tree/main/Notebooks). The principal Notebook is [Main.ipynb](https://github.com/Dieguinho1612/Job-Scheduling-Deep-Reinforcement-Learning/blob/main/Notebooks/Action_Pointer.ipynb).

# Files

Besides the directory of Notebooks, there are two more directories containing files:

- [Neural Networks](https://github.com/Dieguinho1612/Job-Scheduling-Deep-Reinforcement-Learning/tree/main/Neural_Networks): Contains the <i>h5</i>-file of the principal [Neural Network](https://github.com/Dieguinho1612/Job-Scheduling-Deep-Reinforcement-Learning/blob/main/Neural_Networks/Neural_Network.h5) after it has been trained supervisedly. It also contains its <i>h5</i>-files after having been uptrained to higher numbers of Jobs by using the corresponding estimated data sets.
- [Data](https://github.com/Dieguinho1612/Job-Scheduling-Deep-Reinforcement-Learning/tree/main/Data): Contains all the data we computed to train, validate and test the Neural Network. It also contains all the data that we have estimated to uptrain it to higher numbers of Jobs.

