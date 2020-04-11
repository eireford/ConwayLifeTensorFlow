# Life on TensorFlow

[Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) is a delightfully playable cellular automaton [zero-player game](https://en.wikipedia.org/wiki/Zero-player_game) with some intriguing mathematical properties.
 - [Self Replicating](https://en.wikipedia.org/wiki/Von_Neumann_universal_constructor), which is how it earns its name.
 - [Turing Complete](https://en.wikipedia.org/wiki/Turing_completeness), it can be used to do arbitrary computations.
 - [Complex Dynamical System](https://math.stackexchange.com/questions/2267175/how-can-i-prove-that-game-of-lifes-evolution-function-is-continuous), complexity emerges from its simple rules.
  - [Undecidable](https://en.wikipedia.org/wiki/Undecidable_problem) It can be proven that there are outcomes that cannot be predicated.

TensorFlow is a great tool for exploring the Game of Life. Life is an example of a problem that is ["Embarrassingly Parallel"](https://en.wikipedia.org/wiki/Embarrassingly_parallel), each step in it's calculation requires only a proximal subset of the data and results can be aggregated via concatenation. One approach to algorithm of life is a [kernel method](https://en.wikipedia.org/wiki/Kernel_method#Mathematics)

## [A heuristic approach](https://github.com/eireford/ConwayLifeTensorFlow/blob/master/LTF_heuristic_performance.ipynb)
  While convolution layers are common in Machine Learning Models, no learning is required to implement the game of life algorithm using a convolution.  In this notebook,LTF heuristic performance, you can see how tensorflow makes good use of a GPU for tasks that don’t include ML.

## [Linear Regression](https://github.com/eireford/ConwayLifeTensorFlow/blob/master/LTF_linear_regression_comparison.ipynb)
  One step towards implementing the full Game Of Life algorithm using ML is to consider the outcome of a single step for a single cell.  This notebook trains a model that updates a single cell based on its immediate neighborhood.

## [Logistic regression](https://github.com/eireford/ConwayLifeTensorFlow/blob/master/LTF_logistic_regression.ipynb)
  This notebook shows how convolutional networks are particularly efficient at extracting the repeating patterns. This model learns the rules for the game of life after just 40 examples.

## [Logistic regression two steps](https://github.com/eireford/ConwayLifeTensorFlow/blob/master/LTF_logistic_regression_two_step.ipynb)
  Training for two steps in the life algorithm requires a larger kernel and more data.

## Logistic regression three steps
  You can’t just scale up the two step model and train for three steps.

See Also
 - https://github.com/sitomani/gol-deep
 - https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life
 - https://nostarch.com/download/samples/PythonPlayground_sampleCh3.pdf
 - https://databricks.com/tensorflow/custom-functions
 - http://drsfenner.org/blog/2015/07/game-of-life-in-numpy-preliminaries-2/


