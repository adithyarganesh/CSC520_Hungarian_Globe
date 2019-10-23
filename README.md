#Important Information
All the code was run from a personal linux computer using the python version 3.6.
While trying to run on a similar VCL image, it was found that "python Search.py <ALG> <FILE>" had problems in execution and "python3 Search.py <ALG> <FILE>" ran correctly (specifying the python version explicitly while running)

#Description
The code to develop a search algorithm for solving the Globe Puzzle is written and compiled in Python3. It is available in the file Search.py. Three search techniques have been used to determine the path from the scrambled state. Namely bfs, astar and rbfs.

#Implementation
The code is implemented in a single package called Search.py. This code will be
called as follows:
python3 Search.py <ALG> <FILE>
Where ALG is one of: "BFS", "AStar", "RBFS". And FILE is the puzzle file name.
For simplicity, the entire coordinate system is converted to a list of integers from [0 to 29] and a mapping function to map the initial configuration to the final configuration is written.

#Results
It was determined that, for a tree of height 6, the Breadth First search technique took 5 seconds to determine the path while heuristic techniques such as AStar search could determine the path in less than 1 second.

The comparison of BFS with heuristic techniques are tabulated for the files below:

PathN-1.mb : BFS- 0.0 seconds, Astar = 0.0 seconds
PathN-2.mb : BFS- 0.0 seconds, Astar = 0.0 seconds
PathN-3.mb : BFS- 0.0 seconds, Astar = 0.0156 seconds
PathN-4.mb : BFS- 0.0624 seconds, AStar- 0.0312 seconds
PathN-5.mb : BFS- 0.1406 seconds, Astar = 0.0312 seconds
PathN-6.mb : BFS- 1.8750 seconds, Astar = 0.0937 seconds
PathN-7.mb : BFS- 26.0940 seconds, Astar = 0.1718 seconds
PathN-8.mb : BFS- 207.7097 seconds, Astar = 1.9688 seconds
PathN-9.mb : BFS- Few minutes, Astar = 2.7501 seconds
PathN-10.mb : BFS- Few hours, Astar = 1.5626 seconds

From the above tabulation, we can see that with a good heuristic, we can easily determine the path to the final configeration in seconds.

#Issues
While solving the puzzles named Puzzle2-X.mb where X is the puzzle number, there was a problem in determining the path for the following puzzles.
Puzzle2-X.md where X is 6,7,10,13,17
The recursive-best first search approach reaches recursion depth when the path is greater or equal to 4

