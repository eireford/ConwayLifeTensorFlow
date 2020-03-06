# Life on TensorFlow

[Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) is a delightfully playable [zero-player game](https://en.wikipedia.org/wiki/Zero-player_game) with some intriguing mathematical properties.
 - [Self Replicating](https://en.wikipedia.org/wiki/Von_Neumann_universal_constructor), which is how it earns its name.
 - [Turing Complete](https://en.wikipedia.org/wiki/Turing_completeness), it can be used to do arbitray computations.
 - [Complex Dynamical System](https://math.stackexchange.com/questions/2267175/how-can-i-prove-that-game-of-lifes-evolution-function-is-continuous), complexity emerges from its simple rules.
  - [Undecidable](https://en.wikipedia.org/wiki/Undecidable_problem) It can be proven that there are outcomes that cannot be predicated.

TensorFlow is a great tool for exploring the Game of Life. Life is an example of a problem that is ["Embarrassingly Parallel"](https://en.wikipedia.org/wiki/Embarrassingly_parallel), each step in it's calculation requires only a proximal subset of the data and results can be aggregated via concatenation. One approach to algorithm of life is a [kernel method](https://en.wikipedia.org/wiki/Kernel_method#Mathematics).

See Also
 - https://github.com/sitomani/gol-deep
 - https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life
 - https://nostarch.com/download/samples/PythonPlayground_sampleCh3.pdf
 - https://databricks.com/tensorflow/custom-functions
 - http://drsfenner.org/blog/2015/07/game-of-life-in-numpy-preliminaries-2/
