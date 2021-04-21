# Human Motion Prediction

## [*A Hamilton-Jacobi Reachability-Based Framework for Predicting and Analyzing Human Motion for Safe Planning](https://arxiv.org/abs/1910.13369)
#### Idea
Formulate human motion prediction as Hamilton-Jacobi reachability problem in joint state space of humans and belief over model param.
#### Method
- Embed belief evolution into human dynamics z:=(x, P(lambda))
- When computing reachable set, replace action distribution with a allowable set --> reduce stochastic reachability to deterministic and solvable by HJB-PDE formulation
#### Advantage
Make prediction and analyze how incorrect prior affects prediction. Robust to misspecified models/priors, still use obs to reduce conservatism safely
#### Remarks
Full forward reachable set --> worst cases, overly conservative

## [*Confidence-aware motion prediction for real-time collision avoidance1](https://journals.sagepub.com/doi/10.1177/0278364919859436)
#### Idea
Maintain a parameter governing the variance of human motion model.
#### Advantage
This informs the confidence in future predictions. The value increases when model explains human motion, and degrades when human moves unexpectedly.

# Application of Optimal Control

## [Combining Optimal Control and Learning for Visual Navigation in Novel Environments](http://proceedings.mlr.press/v100/bansal20a/bansal20a.pdf)
#### Idea
- Use learning to generate waypoint from RGB imgaes
- Low-level control using LQR
- In data collection for training, assume map known and use MPC to label expected waypoints for first-person image + goal coordinate.

## [Provably Safe and Robust Learning-Based Model Predictive Control](https://arxiv.org/abs/1107.2487)
#### Idea
Select input to minimize cost w.r.t. learned dynamics, ensure safety under uncertainty using robust MPC theories

## [Reinforcement Learning for Safety-Critical Control under Model Uncertainty, using Control Lyapunov Functions and Control Barrier Functions](https://arxiv.org/abs/2004.07584)
#### Idea
Learn model uncertainty using RL. Solve optimal control under learned uncertainty using QP.
#### Remarks
Verified on underactuated nonlinear hybrid system

# ML Safety

## [*Dynamically Computing Adversarial Perturbations for Recurrent Neural Networks](https://arxiv.org/ftp/arxiv/papers/2009/2009.02874.pdf)
#### Idea
- Treat adversarial perturbation computation as control problem
- Resemble a feedback controller
- Existence of adv example and robustness margins of the network to such examples
#### Method
#### Advantage
Compute perturbation at each cell online, instead of requiring the whole sequences
#### Remarks
Verified on freq discrimination, MNIST digit recog, human activity recog, IMDb review sentiment analysis

# HRI Modeling

## [Feature Expansive Reward Learning: Rethinking Human Input](https://arxiv.org/abs/2006.13208)
#### Idea
- In co-robot scenarios, if human correction cannot be explained by existing features, ask human to explicitly teach the missing aspect
- The human guides the robot from states where the missing feature is highly expressed to states where it is not.
- Example: teach "distance from the laptop": move from above the laptop to a comfortable distance

## []()
#### Idea
#### Method
#### Advantage
#### Remarks




