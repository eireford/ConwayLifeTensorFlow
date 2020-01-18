# Conway's Life for TensorFlow
An implementation of Conway's Game Of Life for TensorFlow



## Life is Local
[Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) is an example of 
a problem that is ["Embarassingly Parralel"](https://en.wikipedia.org/wiki/Embarrassingly_parallel),
 each step in it's calculation requires only a proximal subset of the data and results can be aggregated via
  concatenation. Tensorflow facilitates computing the solution in a distributed fashion.

## Life is convoluted
One approach to algorithm of life is a kernal method. where each element in the result set is determined by the cross
product of 


## Life can be tricky.
The kernal trick?
https://en.wikipedia.org/wiki/Kernel_method#Mathematics:_the_kernel_trick

