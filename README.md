# Safe-Deep-Reinforcement-Learning

***Safe Reinforcement Learning***: Process of learning policies that maximize the expectation of the return in problems in which it is important to ***ensure reasonable system performance*** and/or ***respect safety constraints*** during the learning and/or deployment processes.

Contributed by Chunyang Zhang.

## [Content](#content)

<table>
<tr><td colspan="2"><a href="#survey-papers">1. Survey</a></td></tr> 
<tr><td colspan="2"><a href="#methodology">2. Methodology</a></td></tr>
<tr>
    <td>&ensp;<a href="#model-based">2.1 Model Based</a></td>
    <td>&ensp;<a href="#model-free">2.2 Model Free</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#lyapunov-function">2.3 Lyapunov Function</a></td>
    <td>&ensp;<a href="#actor-critic">2.4 Actor Critic</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#latent-representation">2.5 Latent Representation</a></td>
    <td>&ensp;<a href="#policy-optimization">2.6 Policy Optimization</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#inverse-rl">2.7 Inverse RL</a></td>
    <td>&ensp;<a href="#multi-agent">2.8 Multi Agent</a></td>
</tr>
<tr><td colspan="2"><a href="#mechanism">3. Mechanism</a></td></tr>
<tr>
    <td>&ensp;<a href="#analysis">3.1 Analysis</a></td>
    <td>&ensp;<a href="#library">3.2 Library</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#deployment">3.3 Deployment</a></td>
    <td>&ensp;<a href="#continual-learning">3.4 Continual Learning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#reward">3.5 Reward</a></td>
    <td>&ensp;<a href="#lagrangian-method">3.6 Lagrangian Method</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#out-of-distribution">3.7 Out of Distribution</a></td>
    <td>&ensp;<a href="#meta-learning">3.8 Meta Learning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#transformer">3.9 Transformer</a></td>
    <td>&ensp;<a href="#safe-set"></a>3.10 Safe Set</td>
</tr>
<tr><td colspan="2"><a href="#application">4. Application</a></td></tr>
<tr>
    <td>&ensp;<a href="#3-dimensional">4.1 3-Dimensional</a></td>
    <td>&ensp;<a href="#cyber-attack">4.2 Cyber-Attack</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#autonomous vehicles">4.3 Autonomous Vehicles</a></td>
    <td>&ensp;<a href="#"></a></td>
</tr>
</table>


## [Survey papers](#content)
1. **A comprehensive survey on safe reinforcement learning.** JMLR, 2015. [paper](https://www.jmlr.org/papers/v16/garcia15a.html)

   *Javier Garcí and Fern o Fernández.*

1. **Policy learning with constraints in model-free reinforcement learning: A survey.** IJCAI, 2021. [paper](https://www.ijcai.org/proceedings/2021/614)

   *Yongshuai Liu, Avishai Halev, and Xin Liu.* 

1. **Safe learning in robotics: From learning-based control to safe reinforcement learning.** Annual Review of Control, Robotics, and Autonomous Systems, 2022. [paper](https://www.annualreviews.org/doi/10.1146/annurev-control-042920-020211)

   *Lukas Brunke, Melissa Greeff, Adam W. Hall, Zhaocong Yuan, Siqi Zhou, Jacopo Panerati, and Angela P. Schoellig.* 

1. **A review of safe reinforcement learning: Methods, theory and applications.** arXiv, 2022. [paper](https://arxiv.org/abs/2205.10330)

   *Shangding Gu, Long Yang, Yali Du, Guang Chen, Florian Walter, Jun Wang, Yaodong Yang, and Alois Knoll.* 

1. **Deep reinforcement learning for autonomous driving: A survey.** IEEE Transactions on Intelligent Transportation Systems, 2021. [paper](https://ieeexplore.ieee.org/document/9351818)

   *Kiran, B Ravi and Sobh, Ibrahim and Talpaert, Victor and Mannion, Patrick and Sallab, Ahmad A. Al and Yogamani, Senthil, and Pérez, Patrick.* 


## [Methodology](#content)
### [Model Based](#content) 
1. **Provably efficient reinforcement learning with linear function approximation.** ICML, 2020. [paper](https://proceedings.mlr.press/v125/jin20a.html)

   *Chi Jin, Zhuoran Yang, Zhaoran Wang, and Michael I Jordan.* 

1. **Model-based safe deep reinforcement learning via a constrained proximal policy optimization algorithm.** NIPS, 2022. [paper](https://arxiv.org/abs/2210.07573)

   *Ashish Kumar Jayant and Shalabh Bhatnagar.* 

1. **Conservative and adaptive penalty for model-based safe reinforcement learning.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20478)

   *Yecheng Jason Ma, Andrew Shen, Osbert Bastani, and Dinesh Jayaraman.* 

### [Model Free](#content)
1. **Model-free safe control for zero-violation reinforcement learning.** CoRL, 2022. [paper](https://proceedings.mlr.press/v164/zhao22a.html)

   *Weiye Zhao, Tairan He, and Changliu Liu.* 

1. **More for less: Safe policy improvement with stronger performance guarantees.** IJCAI, 2023. [paper](https://arxiv.org/abs/2305.07958)

   *Patrick Wienhöft, Marnix Suilen, Thiago D. Simão, Clemens Dubslaff, Christel Baier, and Nils Jansen.* 

1. **Model-free safe reinforcement learning through neural barrier certificate.** RAL, 2023. [paper](https://ieeexplore.ieee.org/abstract/document/10023989)

   *Yujie Yang, Yuxuan Jiang, Yichen Liu,  Jianyu Chen, and Shengbo Eben Li.* 

### [Lyapunov Function](#content)
1. **Lyapunov-based safe policy optimization for continuous control.** ICML, 2019. [paper](https://openreview.net/forum?id=SJgUYBVLsN)

   *Yinlam Chow, Ofir Nachum, Aleksandra Faust, Edgar Duez-Guzmn, and Mohamamd Ghavamzadeh.* 

1. **Lyapunov design for safe reinforcement learning.** JMLR, 2002. [paper](https://www.jmlr.org/papers/v3/perkins02a.html)

   *Theodore J. Perkins and Andrew G. Barto.* 

1. **Value functions are control barrier functions: Verification of safe policies using control theory.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.04026)

   *Daniel C.H. Tan, Fernando Acero, Robert McCarthy, Dimitrios Kanoulas, and Zhibin Li.* 

### [Actor Critic](#content) 
1. **WCSAC: Worst-case soft actor critic for safety-constrained reinforcement learning.** AAAI, 2021. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/17272)

   *Qisong Yang, Thiago D. Simao, Simon H. Tindemans, and Matthijs T. J. Spaan.* 

### [Latent Representation](#content) 
1. **Safe reinforcement learning from pixels using a stochastic latent representation.** ICLR, 2023. [paper](https://openreview.net/forum?id=b39dQt_uffW)

   *Yannick Hogewind, Thiago D. Simao, Tal Kachman, and Nils Jansen.* 

### [Policy Optimization](#content) 
1. **Constrained Policy Optimization.** ICML, 2017. [paper](https://proceedings.mlr.press/v70/achiam17a)

   *Joshua Achiam, David Held, Aviv Tamar, and Pieter Abbeel.* 

1. **Reward constrained policy optimization.** ICLR, 2019. [paper](https://openreview.net/forum?id=SkfrvsA9FX)

   *Chen Tessler, Daniel J. Mankowitz, and Shie Mannor.* 

1. **Projection-based constrained policy optimization.** ICLR, 2020. [paper](https://openreview.net/forum?id=rke3TJrtPS)

   *Tsung-Yen Yang, Justinian Rosca, Karthik Narasimhan, and Peter J. Ramadge.* 

1. **CRPO: A new approach for safe reinforcement learning with convergence guarantee.** ICML, 2021. [paper](https://proceedings.mlr.press/v139/xu21a.html)

   *Tengyu Xu, Yingbin Liang, and Guanghui Lan.* 

1. **When to update your model: Constrained model-based reinforcement learning.** NIPS, 2022. [paper](https://openreview.net/forum?id=ccWaPGl9Hq)

   *Tianying Ji, Yu Luo, Fuchun Sun, Mingxuan Jing, Fengxiang He, and Wenbing Huang.*

1. **Constraints penalized Q-learning for safe offline reinforcement learning.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20855)

   *Haoran Xu, Xianyuan Zhan, and Xiangyu Zhu.*

1. **Exploring safer behaviors for deep reinforcement learning.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20737)

   *Enrico Marchesini, Davide Corsi, and Alessandro Farinelli.*

1. **Constrained proximal policy optimization.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.14216)

   *Chengbin Xuan, Feng Zhang, Faliang Yin, and Hak-Keung Lam.*

### [Inverse RL](#content)
1. **Inverse constrained reinforcement learning.** ICML, 2021. [paper](https://proceedings.mlr.press/v139/malik21a.html)

   *Shehryar Malik, Usman Anwar, Alireza Aghasi, and Ali Ahmed.* 

1. **Benchmarking constraint inference in inverse reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=vINj_Hv9szL)

   *Guiliang Liu, Yudong Luo, Ashish Gaurav, Kasra Rezaee, and Pascal Poupart.* 

1. **Maximum causal entropy inverse constrained reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.02857)

   *Mattijs Baert, Pietro Mazzaglia, Sam Leroux, and Pieter Simoens.* 

### [Multi Agent](#content)
1. **Provably efficient generalized Lagrangian policy optimization for safe multi-agent reinforcement learning.** JMLR, 2023. [paper](https://dongshed.github.io/papers/22dingprovably.pdf)

   *Dongsheng Ding, Xiaohan Wei, Zhuoran Yang, Zhaoran Wang, and Mihailo R. Jovanovic.* 

1. **Benchmarking constraint inference in inverse reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=vINj_Hv9szL)

   *Guiliang Liu, Yudong Luo, Ashish Gaurav, Kasra Rezaee, and Pascal Poupart.* 


## [Mechanism](#content)
### [Analysis](#content) 
1. **On the robustness of safe reinforcement learning under observational perturbations.** ICLR, 2023. [paper](https://openreview.net/forum?id=jbIYfq4Tr-)

   *Zuxin Liu, Zijian Guo, Zhepeng Cen, Huan Zhang, Jie Tan, Bo Li, and Ding Zhao.*

1. **Detecting adversarial directions in deep reinforcement learning to make robust decisions.** ICML, 2023. [paper](https://arxiv.org/abs/2306.05873)

   *Ezgi Korkmaz and  Jonah Brown-Cohen.*

### [Linrary](#content) 
1. **GUARD: A safe reinforcement learning benchmark.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.13681)

   *Weiye Zhao, Rui Chen, Yifan Sun, Ruixuan Liu, Tianhao Wei, and Changliu Liu.*

### [Deployment](#content) 
1. **Towards deployment-efficient reinforcement learning: Lower bound and optimality.** ICLR, 2022. [paper](https://openreview.net/forum?id=ccWaPGl9Hq)

   *Jiawei Huang, Jinglin Chen, Li Zhao, Tao Qin, Nan Jiang, and Tie-Yan Liu.*

### [Continual Learning](#content) 
1. **Experience replay for continual learning.** NIPS, 2019. [paper](https://papers.nips.cc/paper/2019/hash/fa7cdfad1a5aaf8370ebeda47a1ff1c3-Abstract.html)

   *David Rolnick, Arun Ahuja, Jonathan Schwarz, Timothy Lillicrap, and Gregory Wayne.* 

### [Reward](#content) 
1. **Redeeming intrinsic rewards via constrained optimization.** arXiv, 2022. [paper](https://arxiv.org/abs/2211.07627)

   *Eric Chen, Zhang-Wei Hong, Joni Pajarinen, and Pulkit Agrawal.* 

### [Lagrangian Method](#content) 
1. **Responsive safety in reinforcement learning by PID lagrangian methods.** ICML, 2020. [paper](https://proceedings.mlr.press/v119/stooke20a.html)

   *Adam Stooke, Joshua Achiam, and Pieter Abbeel.* 

### [Out of Distribution](#content) 
1. **Can agents run relay race with dtrangers? Generalization of RL to out-of-distribution trajectories.** ICRL, 2023. [paper](https://openreview.net/forum?id=ipflrGaf7ry)

   *Licheng Lan, Huan Zhang, andCho-Jui Hsieh.* 

### [Meta Learning](#content)
1. **A CMDP-within-online framework for meta-safe reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=mbxz9Cjehr)

   *Vanshaj Khattar, Yuhao Ding, Bilgehan Sel, Javad Lavaei, and Ming Jin.* 

### [Transformer](#content)
1. **Constrained decision Transformer for offline safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2302.07351)

   *Zuxin Liu, Zijian Guo, Yihang Yao, Zhepeng Cen, Wenhao Yu, Tingnan Zhang, and Ding Zhao.* 

### [Safe Set](#content) 
1. **Safe reinforcement learning in constrained Markov decision processes.** ICML, 2020. [paper](http://proceedings.mlr.press/v119/wachi20a.html)

   *Akifumi Wachi and Yanan Sui.*


## [Application](#content) 
### [3-Dimensional](#content) 
1. **Online 3D bin packing with constrained deep reinforcement learning.** AAAI, 2021. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/16155)

   *Hang Zhao, Qijin She, Chenyang Zhu, Yin Yang, and Kai Xu.*

### [Cyber-Attack](#content) 
1. **Spatiotemporally constrained action space attacks on deep reinforcement learning agents.** AAAI, 2020. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/5887)

   *Xian Yeow Lee, Sambit Ghadai, Kai Liang Tan, Chinmay Hegde, and Soumik Sarkar.*

### [Autonomous Vehicles](#content) 
1. **Dense reinforcement learning for safety validation of autonomous vehicles.** Nature, 2023. [paper](https://www.nature.com/articles/s41586-023-05732-2)

   *Shuo Feng, Haowei Sun, Xintao Yan, Haojie Zhu, Zhengxia Zou, Shengyin Shen, and Henry X. Liu.*