# AI Genetic-TSP
A Solution to the Travelling Salesman Problem using Genetic Algorithms

The Travelling Salesman Problem (TSP) is finding the minimal path that traverses though all cities so that a salesman can travel with the minimal cost. The solution to this - classic in algorithms - problem can be achieved with many different approaches (Greedy and Brute Force to name a few) but all these have one common drawback: The Search Space of the Problem itself!

In other words these types of algorithms can't be used to solve the TSP because they find the solution in exponential time, unfeasible in real-life tasks.

That's where the Genetic Algorithms are used, to provide approximately optimal solutions in feasible time.

### DATA:
For this project Qatar and Djibouti cites loaction have been used. Qater data is in `DATA/qa194.tsp` directory. Djibouti data is in `DATA/dj38.tsp` directory.

### The Genetic Algorithm:
The Genetic Algorithm is a Possibilistic Algorithm inspired by the Darwinean Theory of Evolution. It searches through the space of possible solutions so as to find acceptable - according to some criteria - solutions.

To use a Genetic Algorithm to a Problem, one must define:

### Population:
In this problem the population is a list of strings (genomes) that each letter (allele) is a vertex of the given graph.

Example: For a Graph with vertices V = {a,b,c,d,e}, an allele is any of the elements in V, a genome is any permutation of the elements in V and a population is a list of N genomes.

### Fitness Function:
It's the measure used to compare genomes to each other. For this problem a fitness function (and the one we use in this implementation) is the sum of the edge's weights through the graph for a certain path - encoded in the genome

### Mutation:
After making the offsprings of the next generation, to finalize the creation of the new population we must mutate the genomes.

To mutate a genome we just select two random alleles and swap them in a genome

*Note: the mutation does not occur always. It occurs with a user-defined probability.*

### Elitism:
In Genetic Algorithms sometimes the fittest genomes from the current generation are passed directly to the next, contesting with the offsprings and crossover to - potentially - fitter solutions.

This step occurs during the calculation of the Fitness function value for each genome. When all values are computed the genome with the minimum value is appended directly to the next generation's population.

### Algorithm Convergence
The Algorithm stops if:

All genomes in the population are the same or
Reached the max. Generation limit
These cases indicate that the algorithm has converged to a minima (global or local).

Note: To make the algorithm more consistent it is recommended to have a sufficient large population and mutation rate.

***Warning**: Setting the mutation rate too high increases the probability of searching more areas in search space, however, prevents population to converge to any optimum solution. [[Source](https://www.researchgate.net/post/Why-is-the-mutation-rate-in-genetic-algorithms-very-small)] Likewise setting the elititsm rate too high decreases the probability of searching more areas in search space, leading the population to converge faster to a solution but - potentially - preventing it from reaching any optimum.*
    
# Properties of the task environment
- Fully observable
- Single agent
- Stochastic
- Episodic
- Static
- Discrete
- Known


# How to use
 
1. **Google Colab**:
    1. Copy **Genetic.ipynb** file in your google drive
    2. Copy data in data folder in your google drive 
    3. Open **Genetic.ipynb** in your google drive
    4. change data path in the code
2. **.py file**:
    1. Open **Genetic.py** in your pyhton code editor
    2. Change data path in python code
    3. Run the code

# Descriptions of the files of this project:
1. **Project.pdf**
    - In this file, all details about the project have been explained.
2. **Report.pdf**
    - Report file for the project. All results of implemented python codes with plots are visible here.
3. **Genetic.ipynb**
    - Genetic google colab code
4. **Genetic.py**
    - Genetic python code
    
#### Unfortunately **"Project.pdf"** and **"Report.docx"** are only available in **"Persian"**. If you seriously need a translation, contact me.
