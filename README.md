# Safe-Reinforcement-Learning

Safe Reinforcement Learning: Process of learning policies that maximize the expectation of the return in problems in which it is important to ensure reasonable system performance and/or respect safety constraints during the learning and/or deployment processes.

Contributed by Chunyang Zhang.

## [Content](#content)

<table>
<tr><td colspan="2"><a href="#survey-papers">1. Survey</a></td></tr> 
<tr><td colspan="2"><a href="#methods">2. Methods</a></td></tr>
<tr>
    <td>&ensp;<a href="#pinn">2.1 PINN</a></td>
    <td>&ensp;<a href="#deeponet">2.2 DeepONet</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#fourier-operator">2.3 Fourier Operator</a></td>
    <td>&ensp;<a href="#graph-networks">2.4 Graph Networks</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#machine-learning">2.5 Machine Learning</a></td>
    <td>&ensp;<a href="#identification">2.6 Identification</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#finite-element">2.7 Finite Element</a></td>
    <td>&ensp;<a href="#convolutional-filter">2.8 Convolutional Filter</a></td>
</tr>
</table>


## [Survey papers](#content)
1. **A comprehensive survey on safe reinforcement learning.** Journal of Machine Learning Research, 2015. [paper](https://www.jmlr.org/papers/v16/garcia15a.html)

   *Javier Garcí and Fern o Fernández.*

1. **Policy learning with constraints in model-free reinforcement learning: A survey.** IJCAI, 2021. [paper](https://www.ijcai.org/proceedings/2021/614)

   *Yongshuai Liu, Avishai Halev, and Xin Liu.* 

1. **Safe learning in robotics: From learning-based control to safe reinforcement learning.** Annual Review of Control, Robotics, and Autonomous Systems, 2022. [paper](https://www.annualreviews.org/doi/10.1146/annurev-control-042920-020211)

   *Lukas Brunke, Melissa Greeff, Adam W. Hall, Zhaocong Yuan, Siqi Zhou, Jacopo Panerati, and Angela P. Schoellig.* 

1. **A review of safe reinforcement learning: Methods, theory and applications.** arXiv, 2022. [paper](https://arxiv.org/abs/2205.10330)

   *Shangding Gu, Long Yang, Yali Du, Guang Chen, Florian Walter, Jun Wang, Yaodong Yang, and Alois Knoll.* 

1. **Deep reinforcement learning for autonomous driving: A survey.** IEEE Transactions on Intelligent Transportation Systems, 2021. [paper](https://ieeexplore.ieee.org/document/9351818)

   *Kiran, B Ravi and Sobh, Ibrahim and Talpaert, Victor and Mannion, Patrick and Sallab, Ahmad A. Al and Yogamani, Senthil, and Pérez, Patrick.* 


## [Methods](#content) 
### [Lyapunov Function](#content) 
1. **Lyapunov design for safe reinforcement learning.** Journal of Machine Learning Research, 2002. [paper](https://www.jmlr.org/papers/v3/perkins02a.html)

   *Theodore J. Perkins and Andrew G. Barto.* 

### [Latent Representation](#content) 
1. **Safe reinforcement learning from pixels using a stochastic latent representation.** ICLR, 2023. [paper](https://openreview.net/forum?id=b39dQt_uffW)

   *Yannick Hogewind, Thiago D. Simao, Tal Kachman, and Nils Jansen.* 

## [Mechanism](#content) 
### [Deployment](#content) 
1. **Towards deployment-efficient reinforcement learning: Lower bound and optimality.** ICLR, 2022. [paper](https://openreview.net/forum?id=ccWaPGl9Hq)

   *Jiawei Huang, Jinglin Chen, Li Zhao, Tao Qin, Nan Jiang, and Tie-Yan Liu.*

### [Model-Shift Optimization](#content) 
1. **When to update your model: Constrained model-based reinforcement learning.** NIPS, 2022. [paper](https://openreview.net/forum?id=ccWaPGl9Hq)

   *Tianying Ji, Yu Luo, Fuchun Sun, Mingxuan Jing, Fengxiang He, Wenbing Huang.*

### [Continual Learning](#content) 
1. **Experience replay for continual learning.** NIPS, 2019. [paper](https://papers.nips.cc/paper/2019/hash/fa7cdfad1a5aaf8370ebeda47a1ff1c3-Abstract.html)

   *David Rolnick, Arun Ahuja, Jonathan Schwarz, Timothy Lillicrap, and Gregory Wayne.* 

### [Intrinsic Rewards](#content) 
1. **Redeeming intrinsic rewards via constrained optimization.** arXiv, 2022. [paper](https://arxiv.org/abs/2211.07627)

   *Eric Chen, Zhang-Wei Hong, Joni Pajarinen, and Pulkit Agrawal.* 
