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
    <td>&ensp;<a href="#lyapunov-function">2.3 Lyapunov Function</a></td>
    <td>&ensp;<a href="#actor-critic">2.4 Actor Critic</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#latent-representation">2.5 Latent Representation</a></td>
    <td>&ensp;<a href="#policy-optimization">2.6 Policy Optimization</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#inverse-rl">2.7 Inverse RL</a></td>
    <td>&ensp;<a href="#modeling">2.8 Modeling</a></td>
</tr>Evaluation
<tr>
    <td>&ensp;<a href="#offline-learning">2.9 Offline Learning</a></td>
    <td>&ensp;<a href="#evaluation">2.10 Evaluation</a></td>
</tr>
<tr><td colspan="2"><a href="#mechanism">3. Mechanism</a></td></tr>
<tr>
    <td>&ensp;<a href="#analysis">3.1 Analysis</a></td>
    <td>&ensp;<a href="#library">3.2 Library</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#theory">3.3 Theory</a></td>
    <td>&ensp;<a href="#primal-dual">3.4 Primal Dual</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#deployment">3.5 Deployment</a></td>
    <td>&ensp;<a href="#continual-learning">3.6 Continual Learning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#reward">3.7 Reward</a></td>
    <td>&ensp;<a href="#lagrangian-method">3.8 Lagrangian Method</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#out-of-distribution">3.9 Out of Distribution</a></td>
    <td>&ensp;<a href="#meta-learning">3.10 Meta Learning</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#transformer">3.11 Transformer</a></td>
    <td>&ensp;<a href="#safe-set">3.12 Safe Set</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#multi-agent">3.13 Multi Agent</a></td>
    <td>&ensp;<a href="#knowledge-distillation">3.14 Knowledge Distillation</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#causal-reasoning">3.15 Causal Reasoning</a></td>
    <td>&ensp;<a href="#diffusion-model">3.16 Diffusion Model</a></td>
</tr>
<tr><td colspan="2"><a href="#application">4. Application</a></td></tr>
<tr>
    <td>&ensp;<a href="#three-dimension">4.1 Three Dimension<//a></td>
    <td>&ensp;<a href="#cyber-attack">4.2 Cyber Attack</a></td>
</tr>
<tr>
    <td>&ensp;<a href="#autonomous-vehicles">4.3 Autonomous Vehicles</a></td>
    <td>&ensp;<a href="#bandits">4.4 Bandits</a></td>
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

   *Honghao Wei, Arnob Ghosh, Ness Shroff, Lei Ying, and Xingyu Zhouf.* 

### [Lyapunov Function](#content)
1. **Lyapunov-based safe policy optimization for continuous control.** ICML, 2019. [paper](https://openreview.net/forum?id=SJgUYBVLsN)

   *Yinlam Chow, Ofir Nachum, Aleksandra Faust, Edgar Duez-Guzmn, and Mohamamd Ghavamzadeh.* 

1. **Lyapunov design for safe reinforcement learning.** JMLR, 2002. [paper](https://www.jmlr.org/papers/v3/perkins02a.html)

   *Theodore J. Perkins and Andrew G. Barto.* 

1. **Value functions are control barrier functions: Verification of safe policies using control theory.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.04026)

   *Daniel C.H. Tan, Fernando Acero, Robert McCarthy, Dimitrios Kanoulas, and Zhibin Li.* 

1. **A barrier-Lyapunov actor-critic reinforcement learning approach for safe and stable control.** CDC, 2023. [paper](https://arxiv.org/abs/2304.04066)

   *Liqun Zhao, Konstantinos Gatsis, and Antonis Papachristodoulou.* 

1. **Enforcing hard constraints with soft barriers: Safe reinforcement learning in unknown stochastic environments.** ICML, 2023. [paper](https://openreview.net/forum?id=NbC9a9zS5K)

   *Yixuan Wang, Simon Sinong Zhan, Ruochen Jiao, Zhilu Wang, Wanxin Jin, Zhuoran Yang, Zhaoran Wang, Chao Huang, and Qi Zhu.* 

### [Actor Critic](#content) 
1. **WCSAC: Worst-case soft actor critic for safety-constrained reinforcement learning.** AAAI, 2021. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/17272)

   *Qisong Yang, Thiago D. Simao, Simon H. Tindemans, and Matthijs T. J. Spaan.* 

### [Latent Representation](#content) 
1. **Safe reinforcement learning from pixels using a stochastic latent representation.** ICLR, 2023. [paper](https://openreview.net/forum?id=b39dQt_uffW)

   *Yannick Hogewind, Thiago D. Simao, Tal Kachman, and Nils Jansen.* 

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

### [Inverse RL](#content)
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

### [Modeling](#content)
1. **SaFormer: A conditional sequence modeling approach to offline safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2301.12203)

   *Qin Zhang, Linrui Zhang, Haoran Xu, Li Shen, Bowen Wang, Yongzhe Chang, Xueqian Wang, Bo Yuan, and Dacheng Tao.* 

### [Offline Learning](#content)
1. **Safe evaluation for offline learning: Are we ready to deploy?** arXiv, 2022. [paper](https://arxiv.org/abs/2212.08302)

   *Hager Radi, Josiah P. Hanna, Peter Stone, and Matthew E. Taylor.* 

1. **Safe offline reinforcement learning with real-time budget constraints.** ICML, 2023. [paper](https://openreview.net/forum?id=jrYVLd3wqk)

   *Qian Lin, Bo Tang, Zifan Wu, Chao Yu, Shangqin Mao, Qianlong Xie, Xingxing Wang, and Dong Wang.* 

### [Evaluation](#content)
1. **Evaluating model-free reinforcement learning toward safety-critical tasks.** AAAI, 2023. [paper](https://arxiv.org/abs/2212.05727)

   *Linrui Zhang, Qin Zhang, Li Shen, Bo Yuan, Xueqian Wang, and Dacheng Tao.* 

### [Adversarial Training](#content)
1. **Learning-aware safety for interactive autonomy.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.01267)

   *Haimin Hu, Zixu Zhang, Kensuke Nakamura, Andrea Bajcsy, and Jaime F. Fisac.* 


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

1. **Continual learning as computationally constrained reinforcement learning..** arXiv, 2023. [paper](https://arxiv.org/abs/2307.04345)

   *Saurabh Kumar, Henrik Marklund, Ashish Rao, Yifan Zhu, Hong Jun Jeon, Yueyang Liu, and Benjamin Van Roy.*

### [Library](#content) 
1. **GUARD: A safe reinforcement learning benchmark.** arXiv, 2023. [paper](https://arxiv.org/abs/2305.13681)

   *Weiye Zhao, Rui Chen, Yifan Sun, Ruixuan Liu, Tianhao Wei, and Changliu Liu.*

1. **Datasets and benchmarks for offline safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.09303)

   *Zuxin Liu, Zijian Guo, Haohong Lin, Yihang Yao, Jiacheng Zhu, Zhepeng Cen, Hanjiang Hu, Wenhao Yu, Tingnan Zhang, Jie Tan, and Ding Zhao.*

1. **InterCode: Standardizing and benchmarking interactive coding with execution feedback.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.14898)

   *John Yang, Akshara Prabhakar, Karthik Narasimhan, and Shunyu Yao.*

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

### [Deployment](#content) 
1. **Towards deployment-efficient reinforcement learning: Lower bound and optimality.** ICLR, 2022. [paper](https://openreview.net/forum?id=ccWaPGl9Hq)

   *Jiawei Huang, Jinglin Chen, Li Zhao, Tao Qin, Nan Jiang, and Tie-Yan Liu.*

1. **Benchmarking constraint inference in inverse reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=vINj_Hv9szL)

   *Guiliang Liu, Yudong Luo, Ashish Gaurav, Kasra Rezaee, and Pascal Poupart.* 

### [Continual Learning](#content) 
1. **Experience replay for continual learning.** NIPS, 2019. [paper](https://papers.nips.cc/paper/2019/hash/fa7cdfad1a5aaf8370ebeda47a1ff1c3-Abstract.html)

   *David Rolnick, Arun Ahuja, Jonathan Schwarz, Timothy Lillicrap, and Gregory Wayne.* 

### [Reward](#content) 
1. **Redeeming intrinsic rewards via constrained optimization.** arXiv, 2022. [paper](https://arxiv.org/abs/2211.07627)

   *Eric Chen, Zhang-Wei Hong, Joni Pajarinen, and Pulkit Agrawal.* 

1. **Redeeming intrinsic rewards via constrained optimization.** AAAI, 2023. [paper](https://arxiv.org/abs/2301.10339)

   *Tairan He, Weiye Zhao, and Changliu Liu.* 

1. **Anchor-changing regularized natural policy gradient for multi-objective reinforcement learning.** NIPS, 2022. [paper](https://arxiv.org/abs/2206.05357v2)

   *Ruida Zhou, Tao Liu, Dileep Kalathil, P. R. Kumar, and Chao Tian.* 

1. **ROSARL: Reward-only safe reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.00035)

   *Geraud Nangue Tasse, Tamlin Love, Mark Nemecek, Steven James, and Benjamin Rosman.* 

### [Lagrangian Method](#content) 
1. **Responsive safety in reinforcement learning by PID lagrangian methods.** ICML, 2020. [paper](https://proceedings.mlr.press/v119/stooke20a.html)

   *Adam Stooke, Joshua Achiam, and Pieter Abbeel.* 

1. **Safe DreamerV3: Safe reinforcement learning with world mdels.** arXiv 2023. [paper](https://arxiv.org/abs/2307.07176)

   *Weidong Huang, Jiaming Ji, Borong Zhang, Chunhe Xia, and Yaodong Yang.* 

1. **Robust Lagrangian and adversarial policy gradient for robust constrained Markov decision processes.** arXiv 2023. [paper](https://arxiv.org/abs/2308.11267)

   *David M. Bossens.* 

### [Out of Distribution](#content) 
1. **Can agents run relay race with dtrangers? Generalization of RL to out-of-distribution trajectories.** ICRL, 2023. [paper](https://openreview.net/forum?id=ipflrGaf7ry)

   *Licheng Lan, Huan Zhang, andCho-Jui Hsieh.* 

### [Meta Learning](#content)
1. **A CMDP-within-online framework for meta-safe reinforcement learning.** ICLR, 2023. [paper](https://openreview.net/forum?id=mbxz9Cjehr)

   *Vanshaj Khattar, Yuhao Ding, Bilgehan Sel, Javad Lavaei, and Ming Jin.* 

### [Transformer](#content)
1. **Constrained decision Transformer for offline safe reinforcement learning.** ICML, 2023. [paper](https://openreview.net/forum?id=9VKCBHESq0)

   *Zuxin Liu, Zijian Guo, Yihang Yao, Zhepeng Cen, Wenhao Yu, Tingnan Zhang, and Ding Zhao.* 

1. **Transdreamer: Reinforcement learning with Transformer world models.** arXiv, 2022. [paper](https://arxiv.org/abs/2202.09481)

   *Chang Chen, Yi-Fu Wu, Jaesik Yoon, and Sungjin Ahn.* 

### [Safe Set](#content) 
1. **Safe reinforcement learning in constrained Markov decision processes.** ICML, 2020. [paper](http://proceedings.mlr.press/v119/wachi20a.html)

   *Akifumi Wachi and Yanan Sui.*

1. **Reachability constrained reinforcement learning.** ICML, 2022. [paper](https://proceedings.mlr.press/v162/yu22d.html)

   *Dongjie Yu, Haitong Ma, Shengbo Li, and Jianyu Chen.*

1. **A near-optimal algorithm for safe reinforcement learning under instantaneous hard constraints.** ICML, 2023. [paper](https://openreview.net/forum?id=3HMO9iSBdy)

   *Ming Shi, Yingbin Liang, and Ness Shroff.*

### [Multi Agent](#content)
1. **Provably efficient generalized Lagrangian policy optimization for safe multi-agent reinforcement learning.** JMLR, 2023. [paper](https://dongshed.github.io/papers/22dingprovably.pdf)

   *Dongsheng Ding, Xiaohan Wei, Zhuoran Yang, Zhaoran Wang, and Mihailo R. Jovanovic.* 

1. **Safe model-based multi-agent mean-field reinforcement learning.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.17052)

   *Matej Jusup, Barna Pásztor, Tadeusz Janik, Kenan Zhang, Francesco Corman, Andreas Krause, and Ilija Bogunovic.* 

### [Knowledge Distillation](#content)
1. **Coaching a teachable student.** CVPR, 2023. [paper](https://arxiv.org/abs/2306.10014)

   *Jimuyang Zhang, Zanming Huang, and Eshed Ohn-Bar.* 

### [Causal Reasoning](#content)
1. **Causal temporal reasoning for Markov decision processes.** arXiv, 2022. [paper](https://arxiv.org/abs/2212.08712v2)

   *Milad Kazemi and Nicola Paoletti.* 

### [Diffusion Model](#content)
1. **Trajectory generation, control, and safety with denoising diffusion probabilistic models.** arXiv, 2023. [paper](https://arxiv.org/abs/2306.15512)

   *Nicolò Botteghi, Federico Califano, Mannes Poel, and Christoph Brune.* 

### [Variation Optimization](#content)
1. **Safe reinforcement learning as Wasserstein variational inference: Formal methods for interpretability.** arXiv, 2023. [paper](https://arxiv.org/abs/2307.07084)

   *Yanran Wang and David Boyle.* 

### [Generative Model](#content)
1. **Policy learning for robust markov decision process with a mismatched generative model.** AAAI, 2022. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/20705)

   *Jialian Li, Tongzheng Ren, Dong Yan, Hang Su, and  Jun Zhu.* 

### [Cost Function](#content)
1. **AutoCost: Evolving intrinsic cost for zero-violation reinforcement learning.** AAAI, 2023. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/26734)

   *Tairan He, Weiye Zhao, and Changliu Liu.* 

### [Multi Task](#content)
1. **Learning shared safety constraints from multi-task demonstrations.** arXiv, 2023. [paper](https://arxiv.org/abs/2309.00711)

   *Konwoo Kim, Gokul Swamy, Zuxin Liu, Ding Zhao, Sanjiban Choudhury, and Zhiwei Steven Wu.* 


## [Application](#content) 
### [Three Dimension](#content) 
1. **Online 3D bin packing with constrained deep reinforcement learning.** AAAI, 2021. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/16155)

   *Hang Zhao, Qijin She, Chenyang Zhu, Yin Yang, and Kai Xu.*

### [Cyber Attack](#content) 
1. **Spatiotemporally constrained action space attacks on deep reinforcement learning agents.** AAAI, 2020. [paper](https://ojs.aaai.org/index.php/AAAI/article/view/5887)

   *Xian Yeow Lee, Sambit Ghadai, Kai Liang Tan, Chinmay Hegde, and Soumik Sarkar.*

### [Autonomous Vehicles](#content) 
1. **Dense reinforcement learning for safety validation of autonomous vehicles.** Nature, 2023. [paper](https://www.nature.com/articles/s41586-023-05732-2)

   *Shuo Feng, Haowei Sun, Xintao Yan, Haojie Zhu, Zhengxia Zou, Shengyin Shen, and Henry X. Liu.*

### [Bandits](#content) 
1. **Probably anytime-safe stochastic combinatorial semi-bandits.** ICML, 2023. [paper](https://openreview.net/forum?id=14fSjJyJAR)

   *Yunlong Hou, Vincent Tan, and Zixin Zhong.*