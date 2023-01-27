# GA-feature-selection
An application of a genetic algorithm for the determination of the best features for data classification, using Python's scikit-learn API and Pandas. The dataset provided consists of 5-second audio frames of the steps of two people. The original dataset has elements with 34 features of audio belonging to two classes.

The genetic algorithm for feature selection consists of:
- Cromosome objects that contain the dataset with a unique number of the original features, which have:
  - A fitness method which calcuates fitness using the accuracy of the _Random Forest Classifier_ algorithm.
  - A breeding method which reproduces two cromosomes using a random crossover point with a mutation rate.
- A function for the parent selection criteria, which uses _Roulette Wheel Selection_ to chose two cromosomes to generate a child cromosome. (used to create 90% of the next generation)
- Elitism to generate 10% of the next generation.

The accuracy with the original dataset using all **34 features was of 86.77%**. The accuracy of the best individual after running the genetic algorithm for 100 generations was **91.73% with 15 features** (for the run in the jupyter notebook). However, the algorithm might have to be run multiple times for better results in case a fast convergence occurs.
