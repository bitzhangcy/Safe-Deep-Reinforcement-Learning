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
    <td>&ensp;<a href="#lyapunov-function">2.5 Lyapunov Function</a></td>
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
    <td>&ensp;<a href="#lagrangian">3.12 Lagrangian</a></td>
</tr> 
<tr> 
    <td>&ensp;<a href="#knowledge-distillation">3.13 Knowledge Distillation</a></td>
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
    <td>&ensp;<a href="#multi-task">3.20 Multi Task</a></td>
</tr>
<tr>
	<td>&ensp;<a href="#multi-agent">3.21 Multi Agent</a></td>
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

   *Yujie Yang, Yuxuan Jiang, Yichen Liu,  Jianyu Chen, and Shengbo Eben Li.* 

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

1. **State-wise constrained policy optimization.** arXiv, 2023 [paper](https://arxiv.org/abs/2306.12594)

   *Weiye Zhao, Rui Chen, Yifan Sun, Tianhao Wei, and Changliu Liu.*

1. **Scalable safe policy improvement via Monte Carlo tree search.** ICML, 2023 [paper](https://openreview.net/forum?id=tevbBSzSfK)

   *Alberto Castellini, Federico Bianchi, Edoardo Zorzi, Thiago D. Simão, Alessandro Farinelli, and Matthijs T. J. Spaan.*

1. **Towards robust and safe reinforcement learning with Benign off-policy data.** ICML, 2023 [paper](https://openreview.net/forum?id=LB0aNUgIaB)

   *Zuxin Liu, Zijian Guo, Zhepeng Cen, Huan Zhang, Yihang Yao, Hanjiang Hu, and Ding Zhao.*

1. **Constraint-conditioned policy optimization for versatile safe reinforcement learning.** arXiv, 2023 [paper](https://arxiv.org/abs/2310.03718)

   *Yihang Yao, Zuxin Liu, Zhepeng Cen, Jiacheng Zhu, Wenhao Yu, Tingnan Zhang, and Ding Zhao.*

1. **Quantile constrained reinforcement learning: A reinforcement learning framework constraining outage probability.** NIPS, 2022 [paper](https://openreview.net/forum?id=MOGt8ZizQJL)

   *Whiyoung Jung, Myungsik Cho, Jongeui Park, and Youngchul Sung.*

1. **Reinforcement learning in a safety-embedded MDP with trajectory optimization.** arXiv, 2023 [paper](https://arxiv.org/abs/2310.06903)

   *Fan Yang, Wenxuan Zhou, Zuxin Liu, Ding Zhao, and David Held.*

1. **Recursively-constrained partially observable Markov decision processes.** arXiv, 2023 [paper](https://arxiv.org/abs/2310.09688)

   *Qi Heng Ho, Tyler Becker, Ben Kraske, Zakariya Laouar, Martin Feather, Federico Rossi, Morteza Lahijanian, and Zachary N. Sunberg.*

1. **TRC: Trust region conditional value at risk for safe reinforcement learning.** arXiv, 2023 [paper](https://arxiv.org/abs/2312.00344)

   *Dohyeong Kim and Songhwai Oh.*

### [Bandit](#content) 
1. **Probably anytime-safe stochastic combinatorial semi-bandits.** ICML, 2023. [paper](https://openreview.net/forum?id=14fSjJyJAR)

   *Yunlong Hou, Vincent Tan, and Zixin Zhong.*

### [Lyapunov Function](#content)
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

1. **Safe RLHF: Safe reinforcement learning from human feedback.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.12773)

   *Josef Dai, Xuehai Pan, Ruiyang Sun, Jiaming Ji, Xinbo Xu, Mickel Liu, Yizhou Wang, and Yaodong Yang.* 

### [Dynamics Modeling](#content)
1. **SaFormer: A conditional sequence modeling approach to offline safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2301.12203)

   *Qin Zhang, Linrui Zhang, Haoran Xu, Li Shen, Bowen Wang, Yongzhe Chang, Xueqian Wang, Bo Yuan, and Dacheng Tao.* 

1. **Model-free, regret-optimal best policy identification in online CMDPs.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.15395)

   *Zihan Zhou, Honghao Wei, and Lei Ying.* 

1. **Scalable and efficient continual learning from demonstration via hypernetwork-generated stable dynamics model.** arXiv, 2023. [paper](https://arxiv.org/abs/2311.03600)

   *Sayantan Auddy, Jakob Hollenstein, Matteo Saveriano, Antonio Rodríguez-Sánchez, and Justus Piater.* 

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

   *Ezgi Korkmaz and  Jonah Brown-Cohen.*

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

1. **Sample-efficient and safe deep reinforcement learning via reset deep ensemble agents.** NIPS, 2023. [paper](https://arxiv.org/abs/2310.20287)

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

1. **Interior point constrained reinforcement learning with global convergence guarantees.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.00561)

   *Tingting Ni and Maryam Kamgarpour.*

### [Reward](#content) 
1. **Redeeming intrinsic rewards via constrained optimization.** AAAI, 2023. [paper](https://arxiv.org/abs/2301.10339)

   *Tairan He, Weiye Zhao, and Changliu Liu.* 

1. **Anchor-changing regularized natural policy gradient for multi-objective reinforcement learning.** NIPS, 2022. [paper](https://arxiv.org/abs/2206.05357v2)

   *Ruida Zhou, Tao Liu, Dileep Kalathil, P. R. Kumar, and Chao Tian.* 

1. **ROSARL: Reward-only safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.00035)

   *Geraud Nangue Tasse, Tamlin Love, Mark Nemecek, Steven James, and Benjamin Rosman.* 

1. **Solving richly constrained reinforcement learning through state augmentation and reward penalties.** arXiv, 2023. [paper](https://arxiv.org/abs/2301.11592)

   *Hao Jiang, Tien Mai, Pradeep Varakantham, and Minh Huy Hoang.* 

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

### [Diffusion Model](#content)
1. **Trajectory generation, control, and safety with denoising diffusion probabilistic models.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.15512)

   *Nicolò Botteghi, Federico Califano, Mannes Poel, and Christoph Brune.* 

1. **DiffCPS: Diffusion model based constrained policy search for offline reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2310.05333)

   *Longxiang He, Linrui Zhang, Junbo Tan, and Xueqian Wang.* 

### [Transformer](#content)
1. **Constrained decision Transformer for offline safe reinforcement learning.** ICML, 2023. [paper](https://openreview.net/forum?id=9VKCBHESq0)

   *Zuxin Liu, Zijian Guo, Yihang Yao, Zhepeng Cen, Wenhao Yu, Tingnan Zhang, and Ding Zhao.* 

1. **Transdreamer: Reinforcement learning with Transformer world models.** arXiv, 2022. [paper](https://arxiv.org/abs/2202.09481)

   *Chang Chen, Yi-Fu Wu, Jaesik Yoon, and Sungjin Ahn.* 

### [Generative Model](#content)
1. **Policy learning for robust markov decision process with a mismatched generative model.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20705)

   *Jialian Li, Tongzheng Ren, Dong Yan, Hang Su, and  Jun Zhu.* 

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

### [Knowledge Distillation](#content)
1. **Coaching a teachable student.** CVPR, 2023. [paper](https://arxiv.org/abs/2306.10014)

   *Jimuyang Zhang, Zanming Huang, and Eshed Ohn-Bar.* 

### [Causal Reasoning](#content)
1. **Causal temporal reasoning for Markov decision processes.** arXiv, 2022. [paper](https://arxiv.org/abs/2212.08712v2)

   *Milad Kazemi and Nicola Paoletti.* 

### [Out of Distribution](#content) 
1. **Can agents run relay race with dtrangers? Generalization of RL to out-of-distribution trajectories.** ICRL, 2023. [paper](https://openreview.net/forum?id=ipflrGaf7ry)

   *Licheng Lan, Huan Zhang, andCho-Jui Hsieh.* 

### [Curriculum Learning](#content) 
1. **Safe reinforcement learning via curriculum induction.** NIPS, 2020. [paper](https://proceedings.neurips.cc/paper/2020/hash/8df6a65941e4c9da40a4fb899de65c55-Abstract.html)

   *Matteo Turchetta, Andrey Kolobov, Shital Shah, Andreas Krause, and Alekh Agarwal.* 

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

### [Latent Space](#content) 
1. **Safe reinforcement learning from pixels using a stochastic latent representation.** ICLR, 2023. [paper](https://openreview.net/forum?id=b39dQt_uffW)

   *Yannick Hogewind, Thiago D. Simao, Tal Kachman, and Nils Jansen.* 

### [Multi Task](#content)
1. **Learning shared safety constraints from multi-task demonstrations.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.00711)

   *Konwoo Kim, Gokul Swamy, Zuxin Liu, Ding Zhao, Sanjiban Choudhury, and Zhiwei Steven Wu.* 

### [Multi Agent](#content)
1. **Provably efficient generalized Lagrangian policy optimization for safe multi-agent reinforcement learning.** JMLR, 2023. [paper](https://dongshed.github.io/papers/22dingprovably.pdf)

   *Dongsheng Ding, Xiaohan Wei, Zhuoran Yang, Zhaoran Wang, and Mihailo R. Jovanovic.*

1. **Learning adaptive safety for multi-agent systems.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.10657)

   *Luigi Berducci, Shuo Yang, Rahul Mangharam, and Radu Grosu.*


## [Application](#content)
### [Autonomous Driving](#content) 
1. **Dense reinforcement learning for safety validation of autonomous vehicles.** Nature, 2023. [paper](https://www.nature.com/articles/s41586-023-05732-2)

   *Shuo Feng, Haowei Sun, Xintao Yan, Haojie Zhu, Zhengxia Zou, Shengyin Shen, and Henry X. Liu.*

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

   *Abhineet Jain , Jack Kolb, and Harish Ravichandar.*

1. **Safe multi-agent reinforcement learning for formation control without individual reference targets.** arXiv, 2023. [paper](https://arxiv.org/abs/2312.12861)

   *Murad Dawood, Sicong Pan, Nils Dengler, Siqi Zhou, Angela P. Schoellig, and Maren Bennewitz.*