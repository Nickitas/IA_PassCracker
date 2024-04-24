# Password Cracking using Immune Algorithm

## 1. Environment Setup

### 1.1. Installing External Dependencies
To install the DEAP (Distributed Evolutionary Algorithms in Python) package for working with genetic algorithms in the working environment. It provides facilities for defining algorithm operators and registering functions used in the genetic algorithm.

```bash
pip install deap
```

№№ 2. Solving the Problem
### 2.1. Setting Variables and Input Data

TARGET_PASSWORD: The password to be cracked.
ALPHABET: The set of characters used to generate random passwords.
Constants for the immune algorithm:
- POPULATION_SIZE: Number of individuals in the population.
- P_CROSSOVER: Probability of crossover.
- P_MUTATION: Probability of individual mutation.
- MAX_GENERATIONS: Maximum number of generations.
  
### 2.2. Description of the Problem's Classes
FitnessMax. Sets up a single fitness value with a weight of 1.0, indicating maximization of the value when solving the problem.
Individual. Represents the creation of an individual.

### 2.3. Description of Necessary Genetic Functions
1. generate_symbol. Generates a random character from the alphabet.
2. individualCreator. Generates a random individual (password).
3. populationCreator. Generates a population of individuals.

### 2.4. Defining the Problem's Objective Function
The passwordFitness function compares an individual with the target password and returns the number of matching characters.

### 2.5. Registering Genetic Operators
1. evaluate. Computes the fitness value for each individual in the population using the passwordFitness function.
2. select. Selects individuals from the population using tournament selection.
3. mate. Performs two-point crossover.
4. mutate. Performs mutation using shuffle indexes.

### 2.6. Immune Algorithm Implementation
Initializes the population.
Collects statistical data about the population's fitness values.
Executes the algorithm's main loop.
Selects the best individual in each generation.
Logs the evolution results.
Displays the evolution of the password cracking process graphically.

## Results
The best-found password is displayed after running the algorithm.

