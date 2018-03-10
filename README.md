# Gambling-Game

**1. Source** <br>
https://hannekedenouden.ruhosting.nl/RLtutorial/Instructions.html is a small machine learning tutorial in which two machine learning algorithms are used to simulate and fit an individual player's behavior in a game called the Gambling Game. 

The Matlab code, datasets and theory about the simulation and fitting can all be found in the site of the tutorial. I have read through the tutorial and reproduced parts of it in Python in a Jupyter Notebook. The dataset that I've used is downloaded from site. 

**2. Brief Description** <br>
In the Gambling Game, there are two slot machines. Each dispenses a coin with an unknown probability. The player tries to choose the machine that will most likely dispense a coin. Each such choice constitutes 1 trial. There are 135 trials in total. In each trial, exactly 1 machine dispenses a coin. 

We use a Reinforcement Learning model and a Bayesian Learning model to simulate and fit the behavioral data provided in the dataset. 

**3. The Dataset** <br>
The dataset is the file 'tutorialRevLearn_low_s014_data.mat'. It contains data of an individual player of this game. It is a nested structure array. One of the fields is called **'data'**. 

<br>
Two of the fields that **'data'** contains are: 

1. **'choice'** 

  'choice' contains a 135x2 array. Each column corresponds to a machine, and if at row i the entry in a column is 1, then the player has chosen the corresponding machine at trial i. Else, they haven't. 

2. **'prep'**

  'prep' is a structure array. Two of the fields it contains are: 
  
   - **'feedback'**. 'feedback' is a 135x2 array. Each column corresponds to a machine, and if at row i the entry in a column is 1, then the corresponding machine dispenses a coin at trial i. Else, they don't.

   - **'feedbackprob'**. 'feedbackprob' is a 135x1 array. If the entry in row i is p, then the machine corresponding to column 0 in 'feedback' has probability p of dispensing a coin. 
