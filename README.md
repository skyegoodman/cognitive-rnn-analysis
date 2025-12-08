Cognitive RNN Analysis: Coursework Codebase

This repository contains the code used for the coursework report Integrating Brain-Inspired Constraints in Neural Network Models .
All models are trained on tasks from NeuroGym, using recurrent neural networks with biologically inspired constraints.

The repository includes three Jupyter notebooks:

CDM_TASK.ipynb: Baseline leaky RNN and L2-regularised RNN trained on ContextDecisionMaking-v0. 

DMS_TASK.ipynb: The same models trained on DelayMatchSample-v0 to test generalisation to a working-memory task.

ATTENTION.ipynb: A biologically inspired feature-based attention mechanism added to the ContextDecisionMaking task.

Important note about input channels:

The ContextDecisionMaking-v0 environment in recent versions of NeuroGym provides a 5-dimensional observation space:

0: fixation
1: stim_mod1
2: stim_mod2
3: context1
4: context2

Older documentation refers to a 7-channel version, but the current implementation already compresses the stimulus inputs into two scalar evidence channels.

All three notebooks in this repository therefore use the 5-channel format exactly as returned by the environment, and the attention mechanism simply applies multiplicative gain to channels 1 and 2 without modifying the environment.
