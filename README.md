# Life on TensorFlow

Notebooks (2019–2020) exploring [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) with
TensorFlow. First as a plain computation that a GPU speeds up, then as a learning problem: can a small network learn
Life's rules from examples?

Life is a cellular automaton with some intriguing properties. It is
[Turing complete](https://en.wikipedia.org/wiki/Turing_completeness), it supports
[self-replicating patterns](https://en.wikipedia.org/wiki/Von_Neumann_universal_constructor), and some of its outcomes
are [undecidable](https://en.wikipedia.org/wiki/Undecidable_problem). It is also
[embarrassingly parallel](https://en.wikipedia.org/wiki/Embarrassingly_parallel): each cell's next state depends only
on its eight neighbours. So one generation is a single 3×3 convolution, which is exactly what TensorFlow is built to run
fast.

Every notebook opens in Google Colab with its outputs saved, so you can read the results without running anything.

## Notebooks

| Notebook | What it shows |
|---|---|
| [A heuristic approach](LTF_heuristic_performance.ipynb) · [Colab](https://colab.research.google.com/github/eireford/ConwayLifeTensorFlow/blob/main/LTF_heuristic_performance.ipynb) | Life as a fixed convolution kernel, with no learning. TensorFlow makes good use of a GPU even for work that isn't ML. |
| [Heuristic on TPU](LTF_heuristic_on_TPU.ipynb) · [Colab](https://colab.research.google.com/github/eireford/ConwayLifeTensorFlow/blob/main/LTF_heuristic_on_TPU.ipynb) | The same algorithm on a TPU. It didn't speed up, which is a finding in itself. |
| [Linear regression](LTF_linear_regression_comparison.ipynb) · [Colab](https://colab.research.google.com/github/eireford/ConwayLifeTensorFlow/blob/main/LTF_linear_regression_comparison.ipynb) | A first step toward learning the rules: predict one cell's next state from its 3×3 neighbourhood. |
| [Logistic regression](LTF_logistic_regression.ipynb) · [Colab](https://colab.research.google.com/github/eireford/ConwayLifeTensorFlow/blob/main/LTF_logistic_regression.ipynb) | A convolutional model learns Life's rules from just 40 examples. Convolutions are good at extracting repeating local patterns. |
| [Logistic regression, two steps](LTF_logistic_regression_two_step.ipynb) · [Colab](https://colab.research.google.com/github/eireford/ConwayLifeTensorFlow/blob/main/LTF_logistic_regression_two_step.ipynb) | Predicting two generations ahead needs a larger kernel and more data. |
| [Emoji Life](emoji_life.ipynb) · [Colab](https://colab.research.google.com/github/eireford/ConwayLifeTensorFlow/blob/main/emoji_life.ipynb) | An early scratchpad for mapping cell states to emoji (see also [Emojioji](https://github.com/eireford/emojioji)). |

A third step was the natural next experiment. Simply scaling up the two-step model didn't work, which is where this
exploration stopped.

## See also

- [gol-deep](https://github.com/sitomani/gol-deep), another take on learning Life with neural networks
- [Game of Life in NumPy](http://drsfenner.org/blog/2015/07/game-of-life-in-numpy-preliminaries-2/)
- [Python Playground, chapter 3](https://nostarch.com/download/samples/PythonPlayground_sampleCh3.pdf)
