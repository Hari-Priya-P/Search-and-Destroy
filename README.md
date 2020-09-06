# Search-and-Destroy

Consider a map of cells which can be of various terrain types (‘flat’, ‘hilly’, ‘forested’, ‘a complex maze of caves and tunnels’) representing how difficult they are to search. Hidden somewhere in this landscape is a Target, which we need to find. We have the ability to search a given cell, to determine whether or not the target is there. However, the more difficult the terrain, the harder is can be to search - the more likely it is that even if the target is there, you may not find it (a false negative). The value of false negatives are different for different terrains. The false positive rate for any cell is taken to be 0. If you find the target, you are done. The goal is to locate the target in as few searches as possible by utilizing the results of the observations collected. Implemented this by modelling the knowledge/belief about the system probabilistically using Bayesian Networks, and used this belief state to efficiently direct future action according to the following rules:
- At any time, search the cell with the highest probability of containing the target.<br/>
- At any time, search the cell with the highest probability of finding the target.<br/>
