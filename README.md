# Life on TensorFlow

[Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) is a delightfully playable [zero-player game](zero-player game) with some 
intriguing mathematical properties.
 - [Self Replicating](https://en.wikipedia.org/wiki/Von_Neumann_universal_constructor), which is how it gets its name.
 - [Turing Complete](https://en.wikipedia.org/wiki/Turing_completeness), it can be used as a computer.
 - [Complex Dynamical System](https://math.stackexchange.com/questions/2267175/how-can-i-prove-that-game-of-lifes-evolution-function-is-continuous), 
 Complexity emerges from its simple rules.

But we are more interested in the why TensorFlow is a great tool for exploring the Game of Life.

## Life is Local
Life is an example of a problem that is ["Embarrassingly Parallel"](https://en.wikipedia.org/wiki/Embarrassingly_parallel),
 each step in it's calculation requires only a proximal subset of the data and results can be aggregated via
  concatenation. Tensorflow facilitates computing the solution in a distributed fashion.

## Life is convoluted
One approach to algorithm of life is a [kernel method](https://en.wikipedia.org/wiki/Kernel_method#Mathematics).


## Life can be tricky.
The kernal trick?
https://en.wikipedia.org/wiki/Kernel_method#Mathematics:_the_kernel_trick

## Lots to Learn

Credits
 - https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life
 - https://nostarch.com/download/samples/PythonPlayground_sampleCh3.pdf
 - https://databricks.com/tensorflow/custom-functions
 - http://drsfenner.org/blog/2015/07/game-of-life-in-numpy-preliminaries-2/
