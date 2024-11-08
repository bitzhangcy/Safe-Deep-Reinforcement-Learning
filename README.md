# Safe-Deep-Reinforcement-Learning

***Safe Reinforcement Learning***: Process of learning policies that maximize the expectation of the return in problems in which it is important to ***ensure reasonable system performance*** and/or ***respect safety constraints*** during the learning and/or deployment processes.

Contributed by Chunyang Zhang.

## [Content](#content)
<table>
<tr><td colspan="2"><a href="#survey">1. Survey</a></td></tr> 
<tr><td colspan="2"><a href="#methodology">2. Methodology</a></td></tr>
<tr>
    <td>&ensp;<a href="#model-based">2.1 Model Based</a></td>
    <td>&ensp;<a href="#model-free">2.2 Model Free</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#policy-optimization">2.3 Policy Optimization</a></td>
    <td>&ensp;<a href="#bandit">2.4 Bandit</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#barrier-function">2.5 Barrier Function</a></td>
    <td>&ensp;<a href="#actor-critic">2.6 Actor Critic</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#large-model">2.7 Large Model</a></td>
    <td>&ensp;<a href="#dynamics-modeling">2.8 Dynamics Modeling</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#evaluation">2.9 Evaluation</a></td>
    <td>&ensp;<a href="#offline-learning">2.10 Offline Learning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#adversarial-reinforcement-learning">2.11 Adversarial Reinforcement Learning</a></td>
    <td>&ensp;<a href="#inverse-reinforcement-learning">2.12 Inverse Reinforcement Learning</a></td>
</tr>
<tr><td colspan="2"><a href="#mechanism">3. Mechanism</a></td></tr>
<tr>
    <td>&ensp;<a href="#analysis">3.1 Analysis</a></td>
    <td>&ensp;<a href="#library">3.2 Library</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#theory">3.3 Theory</a></td>
    <td>&ensp;<a href="#reward">3.4 Reward</a></td>
</tr>
<tr> 
    <td>&ensp;<a href="#cost-function">3.5 Cost Function</a></td>
    <td>&ensp;<a href="#primal-dual">3.6 Primal Dual</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#deployment">3.7 Deployment</a></td>
    <td>&ensp;<a href="#domain-adaptation">3.8 Domain Adaptation</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#diffusion-model">3.9 Diffusion Model</a></td>
    <td>&ensp;<a href="#transformer">3.10 Transformer</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#generative-model">3.11 Generative Model</a></td>
    <td>&ensp;<a href="#simulation">3.12 Simulation</a></td>
</tr> 
<tr> 
    <td>&ensp;<a href="#lagrangian">3.13 Lagrangian</a></td>
    <td>&ensp;<a href="#causal-reasoning">3.14 Causal Reasoning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#out-of-distribution">3.15 Out of Distribution</a></td>
    <td>&ensp;<a href="#curriculum-learning">3.16 Curriculum Learning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#continual-learning">3.17 Continual Learning</a></td>
    <td>&ensp;<a href="#safe-set">3.18 Safe Set</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#latent-space">3.19 Latent Space</a></td>
    <td>&ensp;<a href="#knowledge-distillation">3.20 Knowledge Distillation</a></td>
</tr>
<tr>
	<td>&ensp;<a href="#multi-agent">3.21 Multi Agent</a></td>
    <td>&ensp;<a href="#multi-task">3.22 Multi Task</a></td>
</tr>
<tr>
	<td>&ensp;<a href="#markov-decision-process">3.23 Markov Decision Process</a></td>
    <td>&ensp;<a href="#solver">3.24 Solver</a></td>
</tr>
<tr>
	<td>&ensp;<a href="#policy-identification">3.25 Policy Identification</a></td>
    <td>&ensp;<a href="#"></a></td>
</tr>
<tr><td colspan="2"><a href="#application">4. Application</a></td></tr>
<tr>
    <td>&ensp;<a href="#autonomous-driving">4.1 Autonomous Driving<//a></td>
    <td>&ensp;<a href="#three-dimension">4.2 Three Dimension</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#cyber-attack">4.3 Cyber Attack</a></td>
    <td>&ensp;<a href="#robotics">4.4 Robotics</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#power-systems ">4.5 Power System</a></td>
    <td>&ensp;<a href="#medicine">4.6 Medicine</a></td>
</tr>
</table>


## [Survey](#content)
1. **A comprehensive survey on safe reinforcement learning.** JMLR, 2015. [paper](https://www.jmlr.org/papers/v16/garcia15a.html)

   *Javier Garcí and Fern o Fernández.*

1. **Policy learning with constraints in model-free reinforcement learning: A survey.** IJCAI, 2021. [paper](https://www.ijcai.org/proceedings/2021/614)

   *Yongshuai Liu, Avishai Halev, and Xin Liu.* 

1. **Safe learning in robotics: From learning-based control to safe reinforcement learning.** Annual Review of Control, Robotics, and Autonomous Systems, 2022. [paper](https://www.annualreviews.org/doi/10.1146/annurev-control-042920-020211)

   *Lukas Brunke, Melissa Greeff, Adam W. Hall, Zhaocong Yuan, Siqi Zhou, Jacopo Panerati, and Angela P. Schoellig.* 

1. **A review of safe reinforcement learning: Methods, theory and applications.** arXiv, 2022. [paper](https://arxiv.org/abs/2205.10330)

   *Shangding Gu, Long Yang, Yali Du, Guang Chen, Florian Walter, Ju*n Wang, Yaodong Yang, and Alois Knoll.* 

1. **Deep reinforcement learning for autonomous driving: A survey.** IEEE Transactions on Intelligent Transportation Systems, 2021. [paper](https://ieeexplore.ieee.org/document/9351818)

   *Kiran, B Ravi and Sobh, Ibrahim and Talpaert, Victor and Mannion, Patrick and Sallab, Ahmad A. Al and Yogamani, Senthil, and Pérez, Patrick.* 

1. **State-wise safe reinforcement learning: A survey.** arXiv, 2023. [paper](https://arxiv.org/abs/2302.03122)

   *Weiye Zhao, Tairan He, Rui Chen, Tianhao Wei, and Changliu Liu.* 

1. **Modeling risk in reinforcement learning: A literature mapping.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.05231)

   *Leonardo Villalobos-Arias, Derek Martin, Abhijeet Krishnan, Madeleine Gagné, Colin M. Potts, and Arnav Jhala.* 

1. **Safe and robust reinforcement-learning: Principles and practice.** arXiv, 2024. [paper](https://arxiv.org/abs/2403.18539)

   *Taku Yamagata and Raul Santos-Rodriguez.* 


## [Methodology](#content)
### [Model Based](#content) 
1. **Provably efficient reinforcement learning with linear function approximation.** ICML, 2020. [paper](https://proceedings.mlr.press/v125/jin20a.html)

   *Chi Jin, Zhuoran Yang, Zhaoran Wang, and Michael I Jordan.* 

1. **Model-based safe deep reinforcement learning via a constrained proximal policy optimization algorithm.** NIPS, 2022. [paper](https://arxiv.org/abs/2210.07573)

   *Ashish Kumar Jayant and Shalabh Bhatnagar.* 

1. **Conservative and adaptive penalty for model-based safe reinforcement learning.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20478)

   *Yecheng Jason Ma, Andrew Shen, Osbert Bastani, and Dinesh Jayaraman.* 

1. **DOPE: Doubly optimistic and pessimistic exploration for safe reinforcement learning.** NIPS, 2022. [paper](https://openreview.net/forum?id=U4BUMoVTrB2)

   *Archana Bura, Aria Hasanzadezonuzy, Dileep Kalathil, Srinivas Shakkottai, and Jean-Francois Chamberland.* 

1. **Risk sensitive model-based reinforcement learning using uncertainty guided planning.** NIPS, 2021. [paper](https://arxiv.org/abs/2111.04972)

   *Garrett Thomas, Yuping Luo, and Tengyu Ma.* 

1. **Safe reinforcement learning by imagining the near future.** NIPS, 2021. [paper](https://proceedings.neurips.cc/paper/2021/hash/73b277c11266681122132d024f53a75b-Abstract.html)

   *Stefan Radic Webster and Peter Flach.* 

1. **Approximate model-based shielding for safe reinforcement learning.** ECAL, 2023. [paper](https://arxiv.org/abs/2308.00707)

   *Alexander W. Goodall and Francesco Belardinelli.* 

### [Model Free](#content)
1. **Model-free safe control for zero-violation reinforcement learning.** CoRL, 2022. [paper](https://proceedings.mlr.press/v164/zhao22a.html)

   *Weiye Zhao, Tairan He, and Changliu Liu.* 

1. **More for less: Safe policy improvement with stronger performance guarantees.** IJCAI, 2023. [paper](https://arxiv.org/abs/2305.07958)

   *Patrick Wienhöft, Marnix Suilen, Thiago D. Simão, Clemens Dubslaff, Christel Baier, and Nils Jansen.* 

1. **Model-free safe reinforcement learning through neural barrier certificate.** RAL, 2023. [paper](https://ieeexplore.ieee.org/abstract/document/10023989)

   *Yujie Yang, Yuxuan Jiang, Yichen Liu, Jianyu Chen, and Shengbo Eben Li.* 

1. **Provably efficient model-free constrained RL with linear function approximation.** NIPS, 2022. [paper](https://proceedings.neurips.cc/paper_files/paper/2022/hash/56b8f22d895c45f60eaac9580152afd9-Abstract-Conference.html)

   *Arnob Ghosh, Xingyu Zhou, and Ness Shroff.* 

1. **Provably efficient model-free algorithms for non-stationary CMDPs.** arXiv, 2023. [paper](https://arxiv.org/abs/2303.05733)

   *Honghao Wei, Arnob Ghosh, Ness Shroff, Lei Ying, and Xingyu Zhou.* 

1. **Anytime-competitive reinforcement learning with policy prior.** NIPS, 2023. [paper](https://arxiv.org/abs/2311.01568)

   *Jianyi Yang, Pengfei Li, Tongxin Li, Adam Wierman, and Shaolei Ren.* 

1. **Anytime-constrained reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.05511)

   *Jeremy McMahan and Xiaojin Zhu.* 

### [Policy Optimization](#content) 
1. **Constrained policy optimization.** ICML, 2017. [paper](https://proceedings.mlr.press/v70/achiam17a)

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

1. **Safe policy improvement for POMDPs via finite-state controllers.** AAAI, 2023. [paper](https://arxiv.org/abs/2301.04939)

   *Thiago D. Simão, Marnix Suilen, and Nils Jansen.*

1. **Policy regularization with dataset constraint for offline reinforcement learning.** ICML, 2023. [paper](https://arxiv.org/abs/2306.06569)

   *Yuhang Ran, Yichen Li, Fuxiang Zhang, Zongzhang Zhang, and Yang Yu.*

1. **Constrained update projection approach to safe policy optimization.** NIPS, 2022. [paper](https://openreview.net/forum?id=22hMrSbQXzt)

   *Long Yang, Jiaming Ji, Juntao Dai, Linrui Zhang, Binbin Zhou, Pengfei Li, Yaodong Yang, and Gang Pan.*

1. **Constrained variational policy optimization for safe reinforcement learning.** ICML, 2022. [paper](https://proceedings.mlr.press/v162/liu22b.html)

   *Zuxin Liu, Zhepeng Cen, Vladislav Isenbaev, Wei Liu, Steven Wu, Bo Li, and Ding Zhao.*

1. **Towards safe reinforcement learning with a safety editor policy.** NIPS, 2022. [paper](https://openreview.net/forum?id=U1m_93ansV)

   *Haonan Yu, Wei Xu, and Haichao Zhang.*

1. **CUP: A conservative update policy algorithm for safe reinforcement learning.** arXiv, 2022. [paper](https://arxiv.org/abs/2202.07565)

   *Long Yang, Jiaming Ji, Juntao Dai, Yu Zhang, Pengfei Li, and Gang Pan.*

1. **State-wise constrained policy optimization.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.12594)

   *Weiye Zhao, Rui Chen, Yifan Sun, Tianhao Wei, and Changliu Liu.*

1. **Scalable safe policy improvement via Monte Carlo tree search.** ICML, 2023. [paper](https://openreview.net/forum?id=tevbBSzSfK)

   *Alberto Castellini, Federico Bianchi, Edoardo Zorzi, Thiago D. Simão, Alessandro Farinelli, and Matthijs T. J. Spaan.*

1. **Towards robust and safe reinforcement learning with Benign off-policy data.** ICML, 2023. [paper](https://openreview.net/forum?id=LB0aNUgIaB)

   *Zuxin Liu, Zijian Guo, Zhepeng Cen, Huan Zhang, Yihang Yao, Hanjiang Hu, and Ding Zhao.*

1. **Constraint-conditioned policy optimization for versatile safe reinforcement learning.** arXiv, 2023 [paper](https://arxiv.org/abs/2310.03718)

   *Yihang Yao, Zuxin Liu, Zhepeng Cen, Jiacheng Zhu, Wenhao Yu, Tingnan Zhang, and Ding Zhao.*

1. **Quantile constrained reinforcement learning: A reinforcement learning framework constraining outage probability.** NIPS, 2022. [paper](https://openreview.net/forum?id=MOGt8ZizQJL)

   *Whiyoung Jung, Myungsik Cho, Jongeui Park, and Youngchul Sung.*

1. **Reinforcement learning in a safety-embedded MDP with trajectory optimization.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.06903)

   *Fan Yang, Wenxuan Zhou, Zuxin Liu, Ding Zhao, and David Held.*

1. **Recursively-constrained partially observable Markov decision processes.** arXiv, 2023。 [paper](https://arxiv.org/abs/2310.09688)

   *Qi Heng Ho, Tyler Becker, Ben Kraske, Zakariya Laouar, Martin Feather, Federico Rossi, Morteza Lahijanian, and Zachary N. Sunberg.*

1. **Trust region-based safe distributional reinforcement learning for multiple constraints.** NIPS, 2024. [paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/3f20f2b0315c72201e23512fdbd1ee91-Abstract-Conference.html)

   *Dohyeong Kim, Kyungjae Lee, and Songhwai Oh.*

1. **TRC: Trust region conditional value at risk for safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.00344)

   *Dohyeong Kim and Songhwai Oh.*

1. **Transition constrained bayesian optimization via Markov decision processes.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.08406)

   *Jose Pablo Folch, Calvin Tsay, Robert M Lee, Behrang Shafei, Weronika Ormaniec, Andreas Krause, Mark van der Wilk, Ruth Misener, and Mojmír Mutný.*

1. **Safety optimized reinforcement learning via multi-objective policy optimization.** ICRA, 2024. [paper](https://arxiv.org/abs/2402.15197)

   *Homayoun Honari, Mehran Ghafarian Tamizi, and Homayoun Najjaran.*

1. **Double duality: Variational primal-dual policy optimization for constrained reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.10810)

   *Zihao Li, Boyi Liu, Zhuoran Yang, Zhaoran Wang, and Mengdi Wang.*

1. **ACPO: A policy optimization algorithm for average MDPs with constraints.** ICML, 2024. [paper](https://arxiv.org/abs/2302.00808)

   *Akhil Agnihotri, Rahul Jain, and Haipeng Luo.*

1. **Spectral-risk safe reinforcement learning with convergence guarantees.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.18698)

   *Dohyeong Kim, Taehyun Cho, Seungyub Han, Hojun Chung, Kyungjae Lee, and Songhwai Oh.*

1. **Enhancing efficiency of safe reinforcement learning via sample manipulation.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.20860)

   *Shangding Gu, Laixi Shi, Yuhao Ding, Alois Knoll, Costas Spanos, Adam Wierman, and Ming Jin.*

1. **Confident natural policy gradient for local planning in qπ-realizable constrained MDPs.** arXiv, 2024. [paper](https://arxiv.org/abs/2406.18529)

   *Tian Tian, Lin F. Yang, and Csaba Szepesvári.*

1. **CVaR-constrained policy optimization for safe reinforcement learning.** TNNLS, 2024. [paper](https://ieeexplore.ieee.org/abstract/document/10444044)

   *Qiyuan Zhang, Shu Leng, Xiaoteng Ma, Qihan Liu, Xueqian Wang, Bin Liang, Yu Liu, and Jun Yang.*

1. **Safe reinforcement learning using finite-horizon gradient-based estimation.** ICML, 2024. [paper](https://openreview.net/forum?id=BiENLaUwlK)

   *Juntao Dai, Yaodong Yang, Qian Zheng, and Gang Pan.*

1. **Exterior penalty policy optimization with penalty metric network under constraints.** IJCAI, 2024. [paper](https://arxiv.org/abs/2407.15537)

   *Shiqing Gao, Jiaxin Ding, Luoyi Fu, Xinbing Wang, and Chenghu Zhou.*

1. **Solving truly massive budgeted monotonic POMDPs with oracle-guided meta-reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2408.07192)

   *Manav Vora, Michael N Grussing, and Melkior Ornik.*

1. **Absolute state-wise constrained policy optimization: High-probability state-wise constraints satisfaction.** arXiv, 2024. [paper](https://arxiv.org/abs/2410.01212)

   *Weiye Zhao, Feihan Li, Yifan Sun, Yujie Wang, Rui Chen, Tianhao Wei, and Changliu Liu.*

### [Bandit](#content) 
1. **Probably anytime-safe stochastic combinatorial semi-bandits.** ICML, 2023. [paper](https://openreview.net/forum?id=14fSjJyJAR)

   *Yunlong Hou, Vincent Tan, and Zixin Zhong.*

### [Barrier Function](#content)
1. **Lyapunov-based safe policy optimization for continuous control.** ICML, 2019. [paper](https://openreview.net/forum?id=SJgUYBVLsN)

   *Yinlam Chow, Ofir Nachum, Aleksandra Faust, Edgar Duez-Guzmn, and Mohamamd Ghavamzadeh.* 

1. **Lyapunov design for safe reinforcement learning.** JMLR, 2002. [paper](https://www.jmlr.org/papers/v3/perkins02a.html)

   *Theodore J. Perkins and Andrew G. Barto.* 

1. **Value functions are control barrier functions: Verification of safe policies using control theory.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.04026)

   *Daniel C.H. Tan, Fernando Acero, Robert McCarthy, Dimitrios Kanoulas, and Zhibin Li.* 

1. **Safe exploration in model-based reinforcement learning using control barrier functions.** Automatica, 2023. [paper](https://www.sciencedirect.com/science/article/abs/pii/S0005109822005489)

   *Max H. Cohen and Calin Belta.* 

1. **Enforcing hard constraints with soft barriers: Safe reinforcement learning in unknown stochastic environments.** ICML, 2023. [paper](https://openreview.net/forum?id=NbC9a9zS5K)

   *Yixuan Wang, Simon Sinong Zhan, Ruochen Jiao, Zhilu Wang, Wanxin Jin, Zhuoran Yang, Zhaoran Wang, Chao Huang, and Qi Zhu.* 

1. **State wise safe reinforcement learning with pixel observations.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.02227)

   *Simon Sinong Zhan, Yixuan Wang, Qingyuan Wu, Ruochen Jiao, Chao Huang, and Qi Zhu.* 

1. **Enforcing hard constraints with soft barriers: Safe reinforcement learning in unknown stochastic environments.** ICML, 2023. [paper](https://proceedings.mlr.press/v202/wang23as.html)

   *Yixuan Wang, Simon Sinong Zhan, Ruochen Jiao, Zhilu Wang, Wanxin Jin, Zhuoran Yang, Zhaoran Wang, Chao Huang, and Qi Zhu.* 

1. **Safe and efficient reinforcement learning using disturbance-observer-based control barrier functions.** ICML, 2023. [paper](https://proceedings.mlr.press/v211/cheng23a.html)

   *Yikun Cheng, Pan Zhao, and Naira Hovakimyan.* 

1. **NLBAC: A neural ordinary differential equations-based framework for stable and safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2401.13148)

   *Liqun Zhao, Keyan Miao, Konstantinos Gatsis, and Antonis Papachristodoulou.* 

1. **Log barriers for safe black-box optimization with application to safe reinforcement learning.** JMLR, 2024. [paper](https://www.jmlr.org/papers/v25/22-0878.html)

   *Ilnura Usmanova, Yarden As, Maryam Kamgarpour, and Andreas Krause.* 

### [Actor Critic](#content) 
1. **WCSAC: Worst-case soft actor critic for safety-constrained reinforcement learning.** AAAI, 2021. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/17272)

   *Qisong Yang, Thiago D. Simao, Simon H. Tindemans, and Matthijs T. J. Spaan.* 

1. **Finite time analysis of constrained actor critic and constrained natural actor critic algorithms.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.16363)

   *Prashansa Panda and Shalabh Bhatnagar.* 

1. **DSAC-C: Constrained maximum entropy for robust discrete soft-actor critic.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.17173)

   *Dexter Neo and Tsuhan Chen.* 

1. **SCPO: Safe reinforcement learning with safety critic policy optimization.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.00880)

   *Jaafar Mhamed and Shangding Gu.* 

1. **Adversarially trained actor critic for offline CMDPs.** arXiv, 2024. [paper](https://arxiv.org/abs/2401.00629)

   *Honghao Wei, Xiyue Peng, Xin Liu, and Arnob Ghosh.* 

### [Large Model](#content)
1. **Parameter-efficient tuning helps language model alignment.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.00819)

   *Tianci Xue, Ziqi Wang, and Heng Ji.* 

1. **Confronting reward model overoptimization with constrained RLHF.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.04373)

   *Ted Moskovitz, Aaditya K. Singh, DJ Strouse, Tuomas Sandholm, Ruslan Salakhutdinov, Anca D. Dragan, and Stephen McAleer.* 

1. **Safe RLHF: Safe reinforcement learning from human feedback.** ICLR, 2024. [paper](https://openreview.net/forum?id=TyFrPOKYXw)

   *Josef Dai, Xuehai Pan, Ruiyang Sun, Jiaming Ji, Xinbo Xu, Mickel Liu, Yizhou Wang, and Yaodong Yang.* 

1. **Safe reinforcement learning with free-form natural language constraints and pre-trained language models.** arXiv, 2024. [paper](https://arxiv.org/abs/2401.07553)

   *Xingzhou Lou, Junge Zhang, Ziyan Wang, Kaiqi Huang, and Yali Du.* 

1. **Progressive safeguards for safe and model-agnostic reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2410.24096)

   *Nabil Omi, Hosein Hasanbeig, Hiteshi Sharma, Sriram K. Rajamani, and Siddhartha Sen.* 

### [Dynamics Modeling](#content)
1. **SaFormer: A conditional sequence modeling approach to offline safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2301.12203)

   *Qin Zhang, Linrui Zhang, Haoran Xu, Li Shen, Bowen Wang, Yongzhe Chang, Xueqian Wang, Bo Yuan, and Dacheng Tao.* 

1. **Model-free, regret-optimal best policy identification in online CMDPs.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.15395)

   *Zihan Zhou, Honghao Wei, and Lei Ying.* 

1. **Scalable and efficient continual learning from demonstration via hypernetwork-generated stable dynamics model.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.03600)

   *Sayantan Auddy, Jakob Hollenstein, Matteo Saveriano, Antonio Rodríguez-Sánchez, and Justus Piater.* 

1. **SafeDreamer: Safe reinforcement learning with world models.** ICLR, 2024. [paper](https://openreview.net/forum?id=tsE5HLYtYg)

   *Weidong Huang, Jiaming Ji, Borong Zhang, Chunhe Xia, and Yaodong Yang.* 

1. **Dynamic model predictive shielding for provably safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.13863)

   *Arko Banerjee, Kia Rahmani, Joydeep Biswas, and Isil Dillig.* 

1. **Verified safe reinforcement learning for neural network dynamic models.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.15994)

   *Junlin Wu, Huan Zhang, and Yevgeniy Vorobeychik.* 

### [Evaluation](#content)
1. **Evaluating model-free reinforcement learning toward safety-critical tasks.** AAAI, 2023. [paper](https://arxiv.org/abs/2212.05727)

   *Linrui Zhang, Qin Zhang, Li Shen, Bo Yuan, Xueqian Wang, and Dacheng Tao.* 

### [Offline Learning](#content)
1. **Safe evaluation for offline learning: Are we ready to deploy?** arXiv, 2022. [paper](https://arxiv.org/abs/2212.08302)

   *Hager Radi, Josiah P. Hanna, Peter Stone, and Matthew E. Taylor.* 

1. **Safe offline reinforcement learning with real-time budget constraints.** ICML, 2023. [paper](https://openreview.net/forum?id=jrYVLd3wqk)

   *Qian Lin, Bo Tang, Zifan Wu, Chao Yu, Shangqin Mao, Qianlong Xie, Xingxing Wang, and Dong Wang.* 

1. **Efficient off-policy safe reinforcement learning using trust region conditional value at risk.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.00342)

   *Dohyeong Kim and Songhwai Oh.* 

1. **Provable safe reinforcement learning with binary feedback.** AISTATS, 2023. [paper](https://proceedings.mlr.press/v206/bennett23a.html)

   *Andrew Bennett, Dipendra Misra, and Nathan Kallus.* 

1. **Long-term safe reinforcement learning with binary feedback.** AAAI, 2024. [paper](https://arxiv.org/abs/2401.03786)

   *Akifumi Wachi, Wataru Hashimoto, and Kazumune Hashimoto.* 

1. **Off-policy primal-dual safe reinforcement learning.** ICLR, 2024. [paper](https://openreview.net/forum?id=vy42bYs1Wo)

   *Zifan Wu, Bo Tang, Qian Lin, Chao Yu, Shangqin Mao, Qianlong Xie, Xingxing Wang, and Dong Wang.* 

1. **OASIS: Conditional distribution shaping for offline safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2407.14653)

   *Yihang Yao, Zhepeng Cen, Wenhao Ding, Haohong Lin, Shiqi Liu, Tingnan Zhang, Wenhao Yu, and Ding Zhao.* 

### [Adversarial Reinforcement Learning](#content)
1. **Learning-aware safety for interactive autonomy.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.01267)

   *Haimin Hu, Zixu Zhang, Kensuke Nakamura, Andrea Bajcsy, and Jaime F. Fisac.* 

1. **Robust safe reinforcement learning under adversarial disturbances.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.07207)

   *Zeyang Li, Chuxiong Hu, Shengbo Eben Li, Jia Cheng, and Yunan Wang.* 

### [Inverse Reinforcement Learning](#content)
1. **Inverse constrained reinforcement learning.** ICML, 2021. [paper](https://proceedings.mlr.press/v139/malik21a.html)

   *Shehryar Malik, Usman Anwar, Alireza Aghasi, and Ali Ahmed.* 

1. **Benchmarking constraint inference in inverse reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=vINj_Hv9szL)

   *Guiliang Liu, Yudong Luo, Ashish Gaurav, Kasra Rezaee, and Pascal Poupart.* 

1. **Maximum causal entropy inverse constrained reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.02857)

   *Mattijs Baert, Pietro Mazzaglia, Sam Leroux, and Pieter Simoens.* 

1. **Identifiability and generalizability in constrained inverse reinforcement learning.** ICML, 2023. [paper](https://arxiv.org/abs/2306.00629)

   *Andreas Schlaginhaufen and Maryam Kamgarpour.* 

1. **FP-IRL: Fokker-Planck-based inverse reinforcement learning -- A physics-constrained approach to Markov decision processes.** ICML, 2023. [paper](https://arxiv.org/abs/2306.10407)

   *Chengyang Huang, Siddhartha Srivastava, Xun Huan, and Krishna Garikipati.* 


## [Mechanism](#content)
### [Analysis](#content) 
1. **On the robustness of safe reinforcement learning under observational perturbations.** ICLR, 2023. [paper](https://openreview.net/forum?id=jbIYfq4Tr-)

   *Zuxin Liu, Zijian Guo, Zhepeng Cen, Huan Zhang, Jie Tan, Bo Li, and Ding Zhao.*

1. **Detecting adversarial directions in deep reinforcement learning to make robust decisions.** ICML, 2023. [paper](https://arxiv.org/abs/2306.05873)

   *Ezgi Korkmaz and Jonah Brown-Cohen.*

1. **Efficient trust region-based safe reinforcement learning with low-bias distributional actor-critic.** arXiv, 2023. [paper](https://arxiv.org/abs/2301.10923)

   *Dohyeong Kim, Kyungjae Lee, and Songhwai Oh.*

1. **Don't do it: Safer reinforcement learning with rule-based guidance.** arXiv, 2022. [paper](https://arxiv.org/abs/2212.13819)

   *Ekaterina Nikonova, Cheng Xue, and Jochen Renz.*

1. **Saute RL: Almost surely safe reinforcement learning using state augmentation.** ICML, 2022. [paper](https://proceedings.mlr.press/v162/sootla22a)

   *Aivar Sootla, Alexander I Cowen-Rivers, Taher Jafferjee, Ziyan Wang, David H Mguni, Jun Wang, and Haitham Ammar.*

1. **Provably efficient exploration in constrained reinforcement learning: Posterior sampling is all you need.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.15737)

   *Danil Provodin, Pratik Gajane, Mykola Pechenizkiy, and Maurits Kaptein.*

1. **Safe exploration in reinforcement learning: A generalized formulation and algorithms.** NIPS, 2023. [paper](https://arxiv.org/abs/2310.03225)

   *Akifumi Wachi, Wataru Hashimoto, Xun Shen, and Kazumune Hashimoto.*

1. **Sample-efficient and safe deep reinforcement learning via reset deep ensemble agents.** NIPS, 2023. [paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/a6f6a5c517b2b92f3d309786af64086c-Abstract-Conference.html)

   *Woojun Kim, Yongjae Shin, Jongeui Park, and Youngchul Sung.*

1. **Imitate the good and avoid the bad: An incremental approach to safe reinforcement learning.** AAAI, 2024. [paper](https://arxiv.org/abs/2312.10385)

   *Huy Hoang and Tien Mai Pradeep Varakantham.*

### [Library](#content) 
1. **GUARD: A safe reinforcement learning benchmark.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.13681)

   *Weiye Zhao, Rui Chen, Yifan Sun, Ruixuan Liu, Tianhao Wei, and Changliu Liu.*

1. **OmniSafe: An infrastructure for accelerating safe reinforcement learning research.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.09304)

   *Jiaming Ji, Jiayi Zhou, Borong Zhang, Juntao Dai, Xuehai Pan, Ruiyang Sun, Weidong Huang, Yiran Geng, Mickel Liu, and Yaodong Yang.*

1. **Datasets and benchmarks for offline safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.09303)

   *Zuxin Liu, Zijian Guo, Haohong Lin, Yihang Yao, Jiacheng Zhu, Zhepeng Cen, Hanjiang Hu, Wenhao Yu, Tingnan Zhang, Jie Tan, and Ding Zhao.*

1. **InterCode: Standardizing and benchmarking interactive coding with execution feedback.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.14898)

   *John Yang, Akshara Prabhakar, Karthik Narasimhan, and Shunyu Yao.*

1. **Safety-Gymnasium: A unified safe reinforcement learning benchmark.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.12567)

   *Jiaming Ji, Borong Zhang, Jiayi Zhou, Xuehai Pan, Weidong Huang, Ruiyang Sun, Yiran Geng, Yifan Zhong, Juntao Dai, and Yaodong Yang.*

1. **Controlgym: Large-scale safety-critical control environments for benchmarking reinforcement learning algorithms.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.18736)

   *Xiangyuan Zhang, Weichao Mao, Saviz Mowlavi, Mouhacine Benosman, and Tamer Başar.*

### [Theory](#content) 
1. **Near-optimal conservative exploration in reinforcement learning under episode-wise constraints.** ICML, 2023. [paper](https://arxiv.org/abs/2306.06265)

   *Donghao Li, Ruiquan Huang, Cong Shen, and Jing Yang.*

1. **Near-optimal sample complexity bounds for constrained MDPs.** NIPS, 2022. [paper](https://openreview.net/forum?id=ZJ7Lrtd12x_)

   *Sharan Vaswani, Lin F. Yang, and Csaba Szepesvári.*

1. **Learning policies with zero or bounded constraint violation for constrained MDPs.** NIPS, 2021. [paper](https://openreview.net/forum?id=Nl7VO_Y7K4Q)

   *Tao Liu, Ruida Zhou, Dileep Kalathil, Panganamala Kumar, and Chao Tian.*

1. **Provably learning Nash policies in constrained Markov potential games.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.07749)

   *Pragnya Alatur, Giorgia Ramponi, Niao He, and Andreas Krause.*

1. **Provably safe reinforcement learning: A theoretical and experimental comparison.** arXiv, 2022. [paper](https://arxiv.org/abs/2205.06750)

   *Hanna Krasowski, Jakob Thumm, Marlon Müller, Lukas Schäfer, Xiao Wang, and Matthias Althoff.*

1. **Shielded reinforcement learning for hybrid systems.** CoRL, 2023. [paper](https://arxiv.org/abs/2308.14424)

   *Asger Horn Brorholt, Peter Gjøl Jensen, Kim Guldstrand Larsen, Florian Lorber, and Christian Schilling.*

1. **Safe reinforcement learning in tensor reproducing kernel Hilbert space.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.00727)

   *Xiaoyuan Cheng, Boli Chen, Liz Varga, and Yukun Hu.*

1. **Joint chance-constrained Markov decision processes.** Annals of Operations Research, 2022. [paper](https://link.springer.com/article/10.1007/s10479-022-05025-3)

   *V Varagapriya, Vikas Vikram Singh, and Abdel Lisser.*

1. **Approximate solutions to constrained risk-sensitive Markov decision processes.** European Journal of Operational Research, 2023. [paper](https://www.sciencedirect.com/science/article/abs/pii/S0377221723001893)

   *Uday M Kumar, Sanjay P. Bhat, Veeraruna Kavitha, and Nandyala Hemachandra.*

1. **Nearly minimax optimal reinforcement learning for linear Markov decision processes.** ICML, 2023. [paper](https://proceedings.mlr.press/v202/he23d.html)

   *Jiafan He, Heyang Zhao, Dongruo Zhou, and Quanquan Gu.*

1. **Truly no-regret learning in constrained MDPs.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.15776)

   *Adrian Müller, Pragnya Alatur, Volkan Cevher, Giorgia Ramponi, and Niao He.*

1. **Achieving O~(1/ε) sample complexity for constrained markov decision process.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.16324)

   *Jiashuo Jiang and Yinyu Ye.*

1. **Sampling-based safe reinforcement learning for nonlinear dynamical systems.** arXiv, 2024. [paper](https://arxiv.org/abs/2403.04007)

   *Wesley A. Suttle, Vipul K. Sharma, Krishna C. Kosaraju, S. Sivaranjani, Ji Liu, Vijay Gupta, and Brian M. Sadler.*

1. **Learning adversarial MDPs with stochastic hard constraints.** arXiv, 2024. [paper](https://arxiv.org/abs/2403.03672)

   *Francesco Emanuele Stradi, Matteo Castiglioni, Alberto Marchesi, and Nicola Gatti.*

1. **ConstrainedZero: Chance-constrained POMDP planning using learned probabilistic failure surrogates and adaptive safety constraints.** IJCAI, 2024. [paper](https://arxiv.org/abs/2405.00644)

   *Robert J. Moss, Arec Jamgochian, Johannes Fischer, Anthony Corso, and Mykel J. Kochenderfer.*

1. **Efficient exploration in average-reward constrained reinforcement learning: Achieving near-optimal regret with posterior sampling.** ICML, 2024. [paper](https://arxiv.org/abs/2405.19017)

   *Danil Provodin, Maurits Kaptein, and Mykola Pechenizkiy.*

1. **Achieving tractable minimax optimal regret in average reward MDPs.** arXiv, 2024. [paper](https://arxiv.org/abs/2406.01234)

   *Victor Boone and Zihan Zhang.*

1. **Improved regret bound for safe reinforcement learning via tighter cost pessimism and reward optimism.** arXiv, 2024. [paper](https://arxiv.org/abs/2410.10158)

   *Kihyun Yu, Duksang Lee, William Overman, and Dabeen Lee.*

### [Reward](#content) 
1. **Redeeming intrinsic rewards via constrained optimization.** AAAI, 2023. [paper](https://arxiv.org/abs/2301.10339)

   *Tairan He, Weiye Zhao, and Changliu Liu.* 

1. **Anchor-changing regularized natural policy gradient for multi-objective reinforcement learning.** NIPS, 2022. [paper](https://arxiv.org/abs/2206.05357v2)

   *Ruida Zhou, Tao Liu, Dileep Kalathil, P. R. Kumar, and Chao Tian.* 

1. **ROSARL: Reward-only safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.00035)

   *Geraud Nangue Tasse, Tamlin Love, Mark Nemecek, Steven James, and Benjamin Rosman.* 

1. **Solving richly constrained reinforcement learning through state augmentation and reward penalties.** arXiv, 2023. [paper](https://arxiv.org/abs/2301.11592)

   *Hao Jiang, Tien Mai, Pradeep Varakantham, and Minh Huy Hoang.* 

1. **State augmented constrained reinforcement learning: Overcoming the limitations of learning with rewards.** TAC, 2023. [paper](https://ieeexplore.ieee.org/abstract/document/10262328)

   *Miguel Calvo-Fullana, Santiago Paternain, Luiz F. O. Chamon, and Alejandro Ribeiro.* 

1. **Balance reward and safety optimization for safe reinforcement learning: A perspective of gradient manipulation.** AAAI, 2024. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/30102)

   *Shangding Gu, Bilgehan Sel, Yuhao Ding, Lu Wang, Qingwei Lin, Ming Jin, and Alois Knoll* 

### [Cost Function](#content)
1. **AutoCost: Evolving intrinsic cost for zero-violation reinforcement learning.** AAAI, 2023. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/26734)

   *Tairan He, Weiye Zhao, and Changliu Liu.* 

### [Primal Dual](#content) 
1. **Semi-infinitely constrained markov decision processes and efficient reinforcement learning.** NIPS, 2022. [paper](https://openreview.net/forum?id=ohk8bILFDkk)

   *Liangyu Zhang, Yang Peng, Wenhao Yang, and Zhihua Zhang.*

1. **Policy-based primal-dual methods for convex constrained markov decision processes.** AAAI, 2023. [paper](https://arxiv.org/abs/2205.10715v3)

   *Donghao Ying, Mengzi Amy Guo, Yuhao Ding, Javad Lavaei, and Zuo-Jun Max Shen.*

1. **Provably efficient primal-dual reinforcement learning for CMDPs with non-stationary objectives and constraints.** AAAI, 2023. [paper](https://arxiv.org/abs/2201.11965v4)

   *Yuhao Ding and Javad Lavaei.*

1. **Achieving zero constraint violation for constrained reinforcement learning via primal-dual approach.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20281)

   *Qinbo Bai, Amrit Singh Bedi, Mridul Agarwal, Alec Koppel, and Vaneet Aggarwal.*

1. **Probabilistic constraint for safety-critical reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.17279)

   *Weiqin Chen, Dharmashankar Subramanian, and Santiago Paternain.*

1. **Last-iterate convergent policy gradient primal-dual methods for constrained MDPs.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.11700)

   *Dongsheng Ding, Chen-Yu Wei, Kaiqing Zhang, and Alejandro Ribeiro.*

1. **Learning-aware safety for interactive autonomy.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.01267)

   *Haimin Hu, Zixu Zhang, Kensuke Nakamura, Andrea Bajcsy, and Jaime Fernandez Fisac.*

1. **Safe reinforcement learning with dual robustness.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.06835)

   *Zeyang Li, Chuxiong Hu, Yunan Wang, Yujie Yang, and Shengbo Eben Li.*

1. **Achieving zero constraint violation for constrained reinforcement learning via conservative natural policy gradient primal-dual algorithm.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20281)

   *Qinbo Bai, Amrit Singh Bedi, Mridul Agarwal, Alec Koppel, and Vaneet Aggarwal.*

1. **Distributionally safe reinforcement learning under model uncertainty: A single-level approach by differentiable convex programming.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.02459)

   *Alaa Eddine Chriat and Chuangchuang Sun.*

1. **A policy gradient primal-dual algorithm for constrained MDPs with uniform PAC guarantees.** arXiv, 2024. [paper](https://arxiv.org/abs/2401.17780)

   *Toshinori Kitamura, Tadashi Kozuno, Masahiro Kato, Yuki Ichihara, Soichiro Nishimori, Akiyoshi Sannai, Sho Sonoda, Wataru Kumagai, and Yutaka Matsuo.*

1. **Adaptive primal-dual method for safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.00355)

   *Weiqin Chen, James Onyejizu, Long Vu, Lan Hoang, Dharmashankar Subramanian, Koushik Kar, Sandipan Mishra, and Santiago Paternain.*

1. **Learning general parameterized policies for infinite horizon average reward constrained MDPs via primal-dual policy gradient algorithm.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.02042)

   *Qinbo Bai, Washim Uddin Mondal, and Vaneet Aggarwal.*

1. **POCE: Primal policy optimization with conservative estimation for multi-constraint offline reinforcement learning.** CVPR, 2024. [paper](https://openaccess.thecvf.com/content/CVPR2024/html/Guan_POCE_Primal_Policy_Optimization_with_Conservative_Estimation_for_Multi-constraint_Offline_CVPR_2024_paper.html)

   *iayi Guan, Li Shen, Ao Zhou, Lusong Li, Han Hu, Xiaodong He, Guang Chen, and Changjun Jiang.*

### [Deployment](#content) 
1. **Towards deployment-efficient reinforcement learning: Lower bound and optimality.** ICLR, 2022. [paper](https://openreview.net/forum?id=ccWaPGl9Hq)

   *Jiawei Huang, Jinglin Chen, Li Zhao, Tao Qin, Nan Jiang, and Tie-Yan Liu.*

1. **Benchmarking constraint inference in inverse reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=vINj_Hv9szL)

   *Guiliang Liu, Yudong Luo, Ashish Gaurav, Kasra Rezaee, and Pascal Poupart.* 
### [Domain Adaptation](#content)
1. **A CMDP-within-online framework for meta-safe reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=mbxz9Cjehr)

   *Vanshaj Khattar, Yuhao Ding, Bilgehan Sel, Javad Lavaei, and Ming Jin.* 

1. **Reinforcement learning by guided safe exploration.** ECAI, 2023. [paper](https://arxiv.org/abs/2307.14316)

   *Qisong Yang, Thiago D. Simão, Nils Jansen, Simon H. Tindemans, and Matthijs T. J. Spaan.* 

1. **Meta SAC-Lag: Towards deployable safe reinforcement learning via metagradient-based hyperparameter tuning.** IROS, 2024. [paper](https://arxiv.org/abs/2408.07962)

   *Homayoun Honari, Amir Mehdi Soufi Enayati, Mehran Ghafarian Tamizi, and Homayoun Najjaran* 

### [Diffusion Model](#content)
1. **Trajectory generation, control, and safety with denoising diffusion probabilistic models.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.15512)

   *Nicolò Botteghi, Federico Califano, Mannes Poel, and Christoph Brune.* 

1. **DiffCPS: Diffusion model based constrained policy search for offline reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.05333)

   *Longxiang He, Linrui Zhang, Junbo Tan, and Xueqian Wang.* 

1. **Feasibility-guided safe offline reinforcement learning.** ICLR, 2024. [paper](https://arxiv.org/abs/2310.05333)

   *Longxiang He, Linrui Zhang, Junbo Tan, and Xueqian Wang.* 

### [Transformer](#content)
1. **Constrained decision Transformer for offline safe reinforcement learning.** ICML, 2023. [paper](https://openreview.net/forum?id=9VKCBHESq0)

   *Zuxin Liu, Zijian Guo, Yihang Yao, Zhepeng Cen, Wenhao Yu, Tingnan Zhang, and Ding Zhao.* 

1. **Transdreamer: Reinforcement learning with Transformer world models.** arXiv, 2022. [paper](https://arxiv.org/abs/2202.09481)

   *Chang Chen, Yi-Fu Wu, Jaesik Yoon, and Sungjin Ahn.* 

1. **Temporal logic specification-conditioned decision Transformer for offline safe reinforcement learning.** ICML, 2024. [paper](https://openreview.net/forum?id=7bg10Jj3bG)

   *Zijian Guo, Weichao Zhou, and Wenchao Li.* 

### [Generative Model](#content)
1. **Policy learning for robust markov decision process with a mismatched generative model.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20705)

   *Jialian Li, Tongzheng Ren, Dong Yan, Hang Su, and Jun Zhu.* 

### [Simulation](#content)
1. **Sim-to-Lab-to-Real: Safe reinforcement learning with shielding and generalization guarantees.** Artificial Intelligence, 2023. [paper](https://www.sciencedirect.com/science/article/abs/pii/S0004370222001515)

   *Kai-Chieh Hsu, Allen Z. Ren, Duy P. Nguyen, Anirudha Majumdar, and Jaime F. Fisac.* 

### [Lagrangian](#content) 
1. **Responsive safety in reinforcement learning by PID lagrangian methods.** ICML, 2020. [paper](https://proceedings.mlr.press/v119/stooke20a.html)

   *Adam Stooke, Joshua Achiam, and Pieter Abbeel.* 

1. **Safe Dreamer: Safe reinforcement learning with world mdels.** arXiv 2023. [paper](https://arxiv.org/abs/2307.07176)

   *Weidong Huang, Jiaming Ji, Borong Zhang, Chunhe Xia, and Yaodong Yang.* 

1. **Robust Lagrangian and adversarial policy gradient for robust constrained Markov decision processes.** arXiv 2023. [paper](https://arxiv.org/abs/2308.11267)

   *David M. Bossens.* 

1. **Safe reinforcement learning as Wasserstein variational inference: Formal methods for interpretability.** arXiv, 2023. [paper](https://arxiv.org/abs/2307.07084)

   *Yanran Wang and David Boyle.* 

1. **Gradient shaping for multi-constraint safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.15127)

   *Yihang Yao, Zuxin Liu, Zhepeng Cen, Peide Huang, Tingnan Zhang, Wenhao Yu, and Ding Zhao.* 

### [Causal Reasoning](#content)
1. **Causal temporal reasoning for Markov decision processes.** arXiv, 2022. [paper](https://arxiv.org/abs/2212.08712v2)

   *Milad Kazemi and Nicola Paoletti.* 

### [Out of Distribution](#content) 
1. **Can agents run relay race with dtrangers? Generalization of RL to out-of-distribution trajectories.** ICRL, 2023. [paper](https://openreview.net/forum?id=ipflrGaf7ry)

   *Licheng Lan, Huan Zhang, andCho-Jui Hsieh.* 

### [Curriculum Learning](#content) 
1. **Safe reinforcement learning via curriculum induction.** NIPS, 2020. [paper](https://proceedings.neurips.cc/paper/2020/hash/8df6a65941e4c9da40a4fb899de65c55-Abstract.html)

   *Matteo Turchetta, Andrey Kolobov, Shital Shah, Andreas Krause, and Alekh Agarwal.* 

1. **Concurrent learning of policy and unknown safety constraints in reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.15893)

   *Lunet Yifru and Ali Baheri.* 

### [Continual Learning](#content) 
1. **Experience replay for continual learning.** NIPS, 2019. [paper](https://papers.nips.cc/paper/2019/hash/fa7cdfad1a5aaf8370ebeda47a1ff1c3-Abstract.html)

   *David Rolnick, Arun Ahuja, Jonathan Schwarz, Timothy Lillicrap, and Gregory Wayne.* 

1. **Safe model-based multi-agent mean-field reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.17052)

   *Matej Jusup, Barna Pásztor, Tadeusz Janik, Kenan Zhang, Francesco Corman, Andreas Krause, and Ilija Bogunovic.* 

1. **Continual learning as computationally constrained reinforcement learning..** arXiv, 2023. [paper](https://arxiv.org/abs/2307.04345)

   *Saurabh Kumar, Henrik Marklund, Ashish Rao, Yifan Zhu, Hong Jun Jeon, Yueyang Liu, and Benjamin Van Roy.*

### [Safe Set](#content) 
1. **Safe reinforcement learning in constrained Markov decision processes.** ICML, 2020. [paper](http://proceedings.mlr.press/v119/wachi20a.html)

   *Akifumi Wachi and Yanan Sui.*

1. **Reachability constrained reinforcement learning.** ICML, 2022. [paper](https://proceedings.mlr.press/v162/yu22d.html)

   *Dongjie Yu, Haitong Ma, Shengbo Li, and Jianyu Chen.*

1. **A near-optimal algorithm for safe reinforcement learning under instantaneous hard constraints.** ICML, 2023. [paper](https://openreview.net/forum?id=3HMO9iSBdy)

   *Ming Shi, Yingbin Liang, and Ness Shroff.*

1. **Iterative reachability estimation for safe reinforcement learning.** NIPS, 2023. [paper](https://arxiv.org/abs/2309.13528)

   *Milan Ganai, Zheng Gong, Chenning Yu, Sylvia Herbert, and Sicun Gao.*

1. **Risk-sensitive inhibitory control for safe reinforcement learning.** ACC, 2023. [paper](https://arxiv.org/abs/2310.01538)

   *Armin Lederer, Erfaun Noorani, John S. Baras, and Sandra Hirche.*

1. **Progressive adaptive chance-constrained safeguards for reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.03379)

   *Zhaorun Chen, Binhao Chen, Tairan He, Liang Gong, and Chengliang Liu.* 

1. **Learn with imagination: Safe set guided state-wise constrained policy optimization.** AAAI, 2024. [paper](https://arxiv.org/abs/2308.13140)

   *Weiye Zhao, Yifan Sun, Feihan Li, Rui Chen, Tianhao Wei, and Changliu Liu.* 

1. **Safe reinforcement learning via shielding under partial observability.** AAAI, 2023. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/26723)

   *Steven Carr, Nils Jansen, Sebastian Junges, and Ufuk Topcu.* 

1. **Safe reinforcement learning with learned non-Markovian safety constraints.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.03005)

   *Siow Meng Low and Akshat Kumar.* 

1. **Feasibility consistent representation learning for safe reinforcement learning.** ICML, 2024. [paper](https://arxiv.org/abs/2405.11718)

   *Zhepeng Cen, Yihang Yao, Zuxin Liu, and Ding Zhao.* 

1. **Safe reinforcement learning in black-box environments via adaptive shielding.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.18180)

   *Daniel Bethell, Simos Gerasimou, Radu Calinescu, and Calum Imrie.* 

1. **Realizable continuous-space shields for safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2410.02038)

   *Kyungmin Kim, Davide Corsi, Andoni Rodriguez, JB Lanier, Benjami Parellada, Pierre Baldi, Cesar Sanchez, and Roy Fox.* 

### [Latent Space](#content) 
1. **Safe reinforcement learning from pixels using a stochastic latent representation.** ICLR, 2023. [paper](https://openreview.net/forum?id=b39dQt_uffW)

   *Yannick Hogewind, Thiago D. Simao, Tal Kachman, and Nils Jansen.* 

### [Knowledge Distillation](#content)
1. **Coaching a teachable student.** CVPR, 2023. [paper](https://arxiv.org/abs/2306.10014)

   *Jimuyang Zhang, Zanming Huang, and Eshed Ohn-Bar.* 

### [Multi Agent](#content)
1. **Provably efficient generalized Lagrangian policy optimization for safe multi-agent reinforcement learning.** JMLR, 2023. [paper](https://dongshed.github.io/papers/22dingprovably.pdf)

   *Dongsheng Ding, Xiaohan Wei, Zhuoran Yang, Zhaoran Wang, and Mihailo R. Jovanovic.*

1. **Learning adaptive safety for multi-agent systems.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.10657)

   *Luigi Berducci, Shuo Yang, Rahul Mangharam, and Radu Grosu.*

1. **Safe multi-agent reinforcement learning with natural language constraints.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.20018)

   *Ziyan Wang, Meng Fang, Tristan Tomilin, Fei Fang, and Yali Du.*

### [Multi Task](#content)
1. **Learning shared safety constraints from multi-task demonstrations.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.00711)

   *Konwoo Kim, Gokul Swamy, Zuxin Liu, Ding Zhao, Sanjiban Choudhury, and Zhiwei Steven Wu.* 

1. **Safe and balanced: A framework for constrained multi-objective reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.16390)

   *Shangding Gu, Bilgehan Sel, Yuhao Ding, Lu Wang, Qingwei Lin, Alois Knoll, and Ming Jin* 

### [Markov Decision Process](#content)
1. **GenSafe: A generalizable safety enhancer for safe reinforcement learning algorithms based on reduced order Markov decision process model.** arXiv, 2024. [paper](https://arxiv.org/abs/2406.03912)

   *Zhehua Zhou, Xuan Xie, Jiayang Song, Zhan Shu, and Lei Ma.* 

### [Solver](#content)
1. **Langevin policy for safe reinforcement learning.** ICML, 2024. [paper](https://openreview.net/forum?id=xgoilgLPGD)

   *Fenghao Lei, Long Yang, Shiting Wen, Zhixiong Huang, Zhiwang Zhang, and Chaoyi Pang.* 

### [Policy Identification](#content)
1. **Near-optimal policy identification in robust constrained Markov decision processes via epigraph form.** arXiv, 2024. [paper](https://arxiv.org/abs/2408.16286)

   *Toshinori Kitamura, Tadashi Kozuno, Wataru Kumagai, Kenta Hoshino, Yohei Hosoe, Kazumi Kasaura, Masashi Hamaya, Paavo Parmas, and Yutaka Matsuo.* 


## [Application](#content)
### [Autonomous Driving](#content) 
1. **Dense reinforcement learning for safety validation of autonomous vehicles.** Nature, 2023. [paper](https://www.nature.com/articles/s41586-023-05732-2)

   *Shuo Feng, Haowei Sun, Xintao Yan, Haojie Zhu, Zhengxia Zou, Shengyin Shen, and Henry X. Liu.*

1. **Enhancing system-level safety in mixed-autonomy platoon via safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2401.11148)

   *Jingyuan Zhou, Longhao Yan, and Kaidi Yang.*

1. **Multi-constraint safe RL with objective suppression for safety-critical applications.** arXiv, 2024. [paper](https://arxiv.org/abs/2402.15650)

   *Zihan Zhou, Jonathan Booher, Wei Liu, Aleksandr Petiushko, and Animesh Garg.*

1. **Do no harm: A counterfactual approach to safe reinforcement learning.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.11669)

   *Sean Vaskov, Wilko Schwarting, and Chris L. Baker.*

1. **Safe multi-agent reinforcement learning with bilevel optimization in autonomous driving.** arXiv, 2024. [paper](https://arxiv.org/abs/2405.18209)

   *Zhi Zheng and Shangding Gu.*

### [Three Dimension](#content)
1. **Online 3D bin packing with constrained deep reinforcement learning.** AAAI, 2021. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/16155)

   *Hang Zhao, Qijin She, Chenyang Zhu, Yin Yang, and Kai Xu.*

### [Cyber Attack](#content)
1. **Spatiotemporally constrained action space attacks on deep reinforcement learning agents.** AAAI, 2020. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/5887)

   *Xian Yeow Lee, Sambit Ghadai, Kai Liang Tan, Chinmay Hegde, and Soumik Sarkar.*

### [Robotics](#content)
1. **Evaluation of constrained reinforcement learning algorithms for legged locomotion.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.15430)

   *Joonho Lee, Lukas Schroth, Victor Klemm, Marko Bjelonic, Alexander Reske, and Marco Hutter.*

1. **Learning safe control for multi-robot systems: Methods, verification, and open challenges.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.13714)

   *Kunal Garg, Songyuan Zhang, Oswin So, Charles Dawson, and Chuchu Fan.*

1. **Constrained reinforcement learning for dexterous manipulation.** IJCAI, 2022. [paper](https://arxiv.org/abs/2301.09766)

   *Abhineet Jain, Jack Kolb, and Harish Ravichandar.*

1. **Safe multi-agent reinforcement learning for formation control without individual reference targets.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.12861)

   *Murad Dawood, Sicong Pan, Nils Dengler, Siqi Zhou, Angela P. Schoellig, and Maren Bennewitz.*

1. **Safe reinforcement learning in uncertain contexts.** TRO, 2024. [paper](https://arxiv.org/abs/2401.05876)

   *Dominik Baumann and Thomas B. Schon.*

1. **Offline goal-conditioned reinforcement learning for safety-critical tasks with recovery policy.** ICRA, 2024. [paper](https://arxiv.org/abs/2403.01734)

   *Chenyang Cao, Zichen Yan, Renhao Lu, Junbo Tan, and Xueqian Wang.*

1. **Safe reinforcement learning on the constraint manifold: Theory and applications.** arXiv, 2024. [paper](https://arxiv.org/abs/2404.09080)

   *Puze Liu, Haitham Bou-Ammar, Jan Peters, and Davide Tateo.*

1. **SRL-VIC: A variable stiffness-based safe reinforcement learning for contact-rich robotic tasks.** RA-L, 2024. [paper](https://arxiv.org/abs/2406.13744)

   *Heng Zhang, Gokhan Solak, Gustavo J. G. Lahr, and Arash Ajoudani.*

### [Power System](#content)
1. **District cooling system control for providing operating reserve based on safe deep reinforcement learning.** TPS, 2023. [paper](https://ieeexplore.ieee.org/abstract/document/10019581)

   *Peipei Yu, Hongcai Zhang, Yonghua Song, Hongxun Hui, and Ge Chen.*

1. **Safe reinforcement learning for power system control: A review.** arXiv, 2024. [paper](https://arxiv.org/abs/2407.00681)

   *Peipei Yu, Zhenyi Wang, Hongcai Zhang, and Yonghua Song.*

1. **A review of safe reinforcement learning methods for modern power systems.** arXiv, 2024. [paper](https://arxiv.org/abs/2407.00304)

   *Tong Su, Tong Wu, Junbo Zhao, Anna Scaglione, and Le Xie.*

### [Medicine](#content)
1. **Offline inverse constrained reinforcement learning for safe-critical decision making in healthcare.** arXiv, 2024. [paper](https://arxiv.org/abs/2410.07525)

   *Nan Fang, Guiliang Liu, and Wei Gong*
