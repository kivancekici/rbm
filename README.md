Restricted Boltzmann Machine
===========
This is a simple implementation modeled from http://blog.echen.me/2011/07/18/introduction-to-restricted-boltzmann-machines/
Currently has no bias

Results RBM(visual=6,hidden=4)
```
Training Data:
[[1.0, 1.0, 1.0, 0.0, 0.0, 0.0]
 [1.0, 0.0, 1.0, 0.0, 0.0, 0.0]
 [1.0, 1.0, 1.0, 0.0, 0.0, 0.0]
 [0.0, 0.0, 1.0, 1.0, 1.0, 0.0]
 [0.0, 0.0, 1.0, 1.0, 0.0, 0.0]
 [0.0, 0.0, 1.0, 1.0, 1.0, 0.0]]

Input:  [[0.0, 0.0, 0.0, 1.0, 1.0, 0.0]]
Output: [[0.0, 0.0, 1.0, 1.0, 1.0, 0.0]]

Inputs: [[0.0, 0.0, 0.0, 1.0, 1.0, 0.0] [0.0, 0.0, 1.0, 1.0, 0.0, 0.0]]
Outputs: [0.0, 0.0, 1.0, 1.0, 1.0, 0.0] [0.0, 0.0, 1.0, 1.0, 0.0, 0.0]]
```

Image Recognition

Input a 100x63 pixel image of a fighter jet at 24bit color resolution. Each RGB value is encoded as a 24 bit vector making a total input size of 100 x 24 x 63 bits.
<table>
   <tr>
      <td>Input<br/><img src="https://raw.githubusercontent.com/kennycason/rbm/master/src/main/resources/data/fighter_jet_small.jpg" width="200"/></td>
      <td>RBM Generated<br/><img src="https://raw.githubusercontent.com/kennycason/rbm/master/src/main/resources/data/output/fighter_rendered_small_rendered_24bit.jpg" width="200"/></td>
   </tr>
</table>


Number Recognition
```
// INPUT
INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□■■■□□□□□
□□□□□□□□□□□■■■■■■■■■■■■□□□□□
□□□□□□□□■■■■■■■■■■□□□□□□□□□□
□□□□□□□□■■■■■■■■■■□□□□□□□□□□
□□□□□□□□□■□■■■□□□■□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■■□□□□□□□□□□□□□□
□□□□□□□□□□□□■■□□□□□□□□□□□□□□
□□□□□□□□□□□□□■■■□□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□□■■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■■□□□□□□□□
□□□□□□□□□□□□□□□□□■■■□□□□□□□□
□□□□□□□□□□□□□□□■■■■■□□□□□□□□
□□□□□□□□□□□□□■■■■■■■□□□□□□□□
□□□□□□□□□□□□■■■■■■□□□□□□□□□□
□□□□□□□□□□■■■■■■□□□□□□□□□□□□
□□□□□□□■■■■■■■□□□□□□□□□□□□□□
□□□□□■■■■■■■■□□□□□□□□□□□□□□□
□□□□■■■■■■■□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■■■□□□□□□□
□□□□□□□□□□□□□■■■■■■■■□□□□□□□
□□□□□□□□□□□■■■■■■■□□□□□□□□□□
□□□□□□□□□□■■■■□□□□□□□□□□□□□□
□□□□□□□□□□■■■■□□□□□□□□□□□□□□
□□□□□□□□□□■■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■■■■□□□□□□□□□□□□
□□□□□□□□□□□■■■■■■■□□□□□□□□□□
□□□□□□□□□□□□□□□■■■■□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□■■□□□□□□□□□□□□□□
□□□□□□□□□□□□■■□□□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□■■■■■□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□□■□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□■■■■■□□□□□□□□
□□□□□□□□□□□□□□□■■■■■□□□□□□□□
□□□□□□□□□□□□□■■■■■■■□□□□□□□□
□□□□□□□□□□□□■■■■■■■□□□□□□□□□
□□□□□□□□□□□□■■□□■■■□□□□□□□□□
□□□□□□□□□□□■■□□■■■□□□□□□□□□□
□□□□□□□□□□□■■□□■■□□□□□□□□□□□
□□□□□□□□□□□■■□■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■□■■□□□□□□□□□□□
□□□□□□□□□□□■■□□■■□□□□□□□□□□□
□□□□□□□□□□□■■□□■■□□□□□□□□□□□
□□□□□□□□□□■■□□□■■□□□□□□□□□□□
□□□□□□□□□□■■□□□■■□□□□□□□□□□□
□□□□□□□□□□■■□□■■□□□□□□□□□□□□
□□□□□□□□□□■■■■■■□□□□□□□□□□□□
□□□□□□□□□□□■■■■□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□■■■■■□□□□□□□□□□□□□□□
□□□□□□■■■■■■■■■□□□□□□□□□□□□□
□□□□□■■■■□■■■■■□□□□□□□□□□□□□
□□□□□□■□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□□■■■■□□□□□□□□□□
□□□□□□□□□□□□□□□■■■□□□□□□□□□□
□□□□□□□□□□□□□□□■■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■□□□□□□□□□□
□□□□□□□□□■■■□□□□■■■□□□□□□□□□
□□□□□□□□■■■■□□□□□■■□□□□□□□□□
□□□□□□□□■■■■□□□□□■■□□□□□□□□□
□□□□□□□□□■■■■□□□■■■□□□□□□□□□
□□□□□□□□□■■■■■□□■■■□□□□□□□□□
□□□□□□□□□■■■■■■■■■□□□□□□□□□□
□□□□□□□□□□■■■■■■■■□□□□□□□□□□
□□□□□□□□□□■■■■■■■■■■■■■■■□□□
□□□□□□□□□□□■■■■■■■■■■■■■□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□■■□□□■□□□□□□□□□□□□□□□□
□□□□□□■■■■■■■■□□□□□□□□□□□□□□
□□□□□□■■■■■■■■■■■□□□□□□□□□□□
□□□□□□□□■■□□□□■■■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■□□□□□□□□□□
□□□□□□□□□□□□□□□■■□□□□□□□□□□□
□□□□□□□□□□□□□■■■□□□□□□□□□□□□
□□□□□□□□□□□■■■□□□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□□■■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□□■■□□□□□□□□
□□□□□□□□□□□□□□□□□□■■□□□□□□□□
□□□□□□□□□□□□□□□□□□■■□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□■■■■■■□□□□□□□□□□
□□□□□□□□□□□■■■□□■■□□□□□□□□□□
□□□□□□□□□□■■■□□□■■□□□□□□□□□□
□□□□□□□□□□■■□□□□■■□□□□□□□□□□
□□□□□□□□□□■■□□□■■■□□□□□□□□□□
□□□□□□□□□□■□□■■■■□□□□□□□□□□□
□□□□□□□□□□■■■■■■■□□□□□□□□□□□
□□□□□□□□□□□■■■□■■□□□□□□□□□□□
□□□□□□□□□□□□□□□■□□□□□□□□□□□□
□□□□□□□□□□□□□□□■□□□□□□□□□□□□
□□□□□□□□□□□□□□■■□□□□□□□□□□□□
□□□□□□□□□□□□□□■■□□□□□□□□□□□□
□□□□□□□□□□□□□□■□□□□□□□□□□□□□
□□□□□□□□□□□□□□■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■□□□□□□□□□□□□□□
□□□□□□□□□□□□□■□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.learn.ContrastiveDivergence - Start Learning (7 samples)
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 0/15000, error: 1305.5197925558577, time: 0.059s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 100/15000, error: 57.300594478427854, time: 0.004s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 200/15000, error: 15.952329441261893, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 300/15000, error: 5.4044291068371155, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 400/15000, error: 2.602268788842556, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 500/15000, error: 1.4970038901297982, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 600/15000, error: 1.1067551950980756, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 700/15000, error: 0.8295110168889177, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 800/15000, error: 0.5378197659583355, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 900/15000, error: 0.3994753611475093, time: 0.003s
...
...
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 14400/15000, error: 0.002183322948934887, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 14500/15000, error: 0.0018464431984471126, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 14600/15000, error: 0.002316604784920346, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 14700/15000, error: 0.015824371649477142, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 14800/15000, error: 0.0033692543108419077, time: 0.003s
INFO  nn.rbm.learn.ContrastiveDivergence - Epoch: 14900/15000, error: 0.006265503532066407, time: 0.003s
INFO  nn.rbm.TestRBM - Data Index: 0
INFO  nn.rbm.TestRBM -

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□■■■■□■■■■□□□□
□□□□□□□□□□□■■■■■■■■■■■■□□□□□
□□□□□□□□■■■■■■■■■■□□■□■□□□□□
□□□□□□□■■■■■■■■■■■□□□□□□□□□□
□□□□□□□□□□□■■■□□■■□□□□□□□□□□
□□□□□□□□□□□□■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■■□□□□□□□□□□□□□□
□□□□□□□□□□□□■■□□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□□■■■■□□□□□□□□□□
□□□□□□□□□□■□□□□■■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■■□□□□□□□□
□□□□□□□□□□□□□□□■■■■■□□□□□□□□
□□□□□□□□□□□□□■■■■■■□□□□□□□□□
□□□□□□□□□□■■■■■■■■□□□□□□□□□□
□□□□□□□□□□■■■■■□□□□□□□□□□□□□
□□□□□□□■■■■■■■□□□□□□□□□□□□□□
□□□□■■□■■■■■□□□□□□□□□□□□□□□□
□□□□□■■■■□■□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■■■■□□□□□□
□□□□□□□□□□□□□■□■■■■■■□□□□□□□
□□□□□□□□□□□■■■■■■□□□□□□□□□□□
□□□□□□□□□□■■■■□□□□□□□□□□□□□□
□□□□□□□□□□■■■■□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□■■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□■■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□■■□□□□□□□□□□□□□□□
□□□□□□□□□□□□■■■■■□□□□□□□□□□□
□□□□□□□□□□□■■■■■■■□□□□□□□□□□
□□□□□□□□□□□□□□□■■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□■■□□□□□□□□□□□□□□
□□□□□□□□□□□■■■□□□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□■■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□■□■■■□□□□□□□□□□
□□□□□□□□□□□□□■■■■■□□□□□□□□□□
□□□□□□□□□□□□□■■■■□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□□■■□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□■■■■□□□□□□□□□
□□□□□□□□□□□□□□□■■■■■□□□□□□□□
□□□□□□□□□□□□□■■■■■■□□□□□□□□□
□□□□□□□□□□□□■■■■■■■■□□□□□□□□
□□□□□□□□□□□■■■■□■■■□□□□□□□□□
□□□□□□□□□□□■■□□□■□□□□□□□□□□□
□□□□□□□□□□□■■□□■■□□□□□□□□□□□
□□□□□□□□□□□■■□■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■□■■□□□□□□□□□□□
□□□□□□□□□□□□■□□■■□□□□□□□□□□□
□□□□□□□□□□□■■□□■■■□□□□□□□□□□
□□□□□□□□□□□■■□□■■□□□□□□□□□□□
□□□□□□□□□□■■□□□■■■□□□□□□□□□□
□□□□□□□□□□■□□□□■■□□□□□□□□□□□
□□□□□□□□□□■■□□■■■□□□□□□□□□□□
□□□□□□□□□□■■■■■■□□□□□□□□□□□□
□□□□□□□□□□□□■■□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□■■■■□□□□□□□□□□□□□□□□
□□□□□□■■■■■■■■■□□□□□□□□□□□□□
□□□□□□■■■■■■■■■■□□□□□□□□□□□□
□□□□□■□□□□□□■■■■□□□□□□□□□□□□
□□□□□□□□□□■□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□□■■■□□□□□□□□□□
□□□□□□□□□□□□□□□■□■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□■■□□□□■■■□□□□□□□□□
□□□□□□□□□□■■□□□□□■■□□□□□□□□□
□□□□□□□□■■■■□□□□□■■□□□□□□□□□
□□□□□□□□□■■■■□□□□■■□□□□□□□□□
□□□□□□□□□□■■■■■□■■■□□□□□□□□□
□□□□□□□□□□■■■■■□■■□□□□□□□□□□
□□□□□□□□□□■■■■■■■■□□□■□■□□□□
□□□□□□□□□□■■■■■■■■■■□■■■■□□□
□□□□□□□□□□□■■■■■■■■■■■■■□□□□
□□□□□□□□□□□■□□□□□□□■□□■□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□■■□□□■■□□□□□□□□□□□□□□□□
□□□□□□■■■■■■■■■■□□□□□□□□□□□□
□□□□□■■■■■□■■■■■■□□□□□□□□□□□
□□□□□□□□■□□□■□■■■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■■□□□□□□□□□
□□□□□□□□□□□□□□□□□■□□□□□□□□□□
□□□□□□□□□□□□□□□■■■□□□□□□□□□□
□□□□□□□□□□□□□□■■□□□□□□□□□□□□
□□□□□□□□□□□■■■■□□□□□□□□□□□□□
□□□□□□□□□□□■■■■□□□□□□□□□□□□□
□□□□□□□□□□□□■■■□□□□□□□□□□□□□
□□□□□□□□□□□□□□■■■■□□□□□□□□□□
□□□□□□□□□□□□□□□■■■□□□□□□□□□□
□□□□□□□□□□□□□□□□■■■■□□□□□□□□
□□□□□□□□□□□□□□□□□□■■□□□□□□□□
□□□□□□□□□□□□□□□□□□■■□□□□□□□□
□□□□□□□□□□□□□□□□□□■■□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□

INFO  nn.rbm.TestRBM -
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
□□□□□□□□□□□□□□■■□□□□□□□□□□□□
□□□□□□□□□□□□■■■■■□□□□□□□□□□□
□□□□□□□□□□■■■□■□■■□□□□□□□□□□
□□□□□□□□□□□■■□□□■□□□□□□□□□□□
□□□□□□□□□□■■□□□□■■□□□□□□□□□□
□□□□□□□□□□■□□□□■■■□□□□□□□□□□
□□□□□□□□□□■■■■■■■□□□□□□□□□□□
□□□□□□□□□■□■■■■■■□□□□□□□□□□□
□□□□□□□□□□□■■□■■■□□□□□□□□□□□
□□□□□□□□□□□□□□■■□□□□□□□□□□□□
□□□□□□□□□□□□□□□■□□□□□□□□□□□□
□□□□□□□□□□□□□□■■■□□□□□□□□□□□
□□□□□□□□□□□□□■□□□□□□□□□□□□□□
□□□□□□□□□□□□□□■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□■□□□□□□□□□□□□□□
□□□□□□□□□□□□□■■□□□□□□□□□□□□□
□□□□□□□□□□□□□□□□□□□□□□□□□□□□
```

