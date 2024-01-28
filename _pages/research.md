---
layout: archive
title: " "
permalink: /research/
author_profile: true
---

# Research Overview 

As we enter an era of autonomy and artificial intelligence (AI), humans are being liberated from conducting tedious, complex, or even hazardous missions by robots. The planning and control algorithms are the nuclei of such an autonomous and intelligent robot to perform tasks. In real world applications, such as autonomous transportation/delivery, smart manufacturing/construction, and aerospace/marine engineering, the robot is subjected to uncertain external disturbances, parametric variations, actuator saturation/delay, and modeling/estimation/measurement errors. Furthermore, teams of robots are needed to perform collaboratively while ensuring inter-robot and robot-obstacle collision avoidance. This requires safety, robustness, resilience, scalability, sustainability, and computational efficiency to be indispensable features of the planning and control algorithms, which attracts ongoing research efforts within the robotics and control community.  

To address these needs, I have developed a new control paradigm that is _defined entirely by the active subset of a full set of inequality constraints at any instant_ for general (i.e., nonlinear, time-varying, arbitrary-order) dynamical systems. Distinct from the literature, my work poses the control problem as a constrained optimization that does **_not_** involve a cost function, a time horizon, or any linearization, and the stability, performance (e.g., path tracking and collision avoidance), and structure (i.e., centralized or decentralized) of the controller are realized by constraints alone. I have successfuly applied this paradigm to controlling swarms of navigation systems such as quadrotor UAVs and wheeled mobile robots and published the results in several highly-ranked journals and conferences in automation and control. 

<!---
I propose a new control paradigm for general dynamical systems such as robots in my dissertation by rejuvenating a fundamental principle conceived by the polymath Gauss in 1829. The methodology poses the control problem at hand as a constrained minimization problem whose objective function, the unconstrained dynamics, is always satisfied. The performance of e.g., virtual leader tracking and collision avoidance and the controller structure (i.e., centralized or decentralized) are achieved by constraints alone. This approach has been applied to the navigation control of hundreds of double integrators, nonlinear quadrotor drones, and two-wheeled mobile robots. I feel humbled and excited that my method is recognized by highly-ranked journals and conferences in automation and control. 
--> 

# Research Projects:

## Navigation Control of Swarms of Double Integrators 

### Centralized Control with Vector-Norm-Based Constraints 

{% include base_path %}

[//]: # (<center>)

[//]: # (  <img src="../images/TAC22/100Agent-path.jpeg" width="50%" />)

[//]: # (</center>)

<iframe width="200" height="100" src="https://www.youtube.com/embed/HkIxFIba1sI" title="100-agent swarm navigation and control;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<details>
  <summary><b>[Abstract]</b></summary>

Multiagent navigation systems present opportunities for many applications due to their agility and cooperation. In any multiagent navigation system, it is critical that actual interagent collisions are strictly prevented. In this article, we present a solution to the 2-D multiagent navigation problem with collision avoidance. Our solution to this problem is based on a novel extension to Gauss's principle of least constraint (GPLC), in which a fixed set of strict equality constraints is replaced by time-varying sets of active inequality constraints. To the best of our knowledge, this is the first instance that extends GPLC with dynamic incorporation and stabilization of active inequality constraints and with actuator delay and saturation. Herein, the dynamics of a collision-free multiagent system satisfies the Karush-Kuhn-Tucker conditions. Active inequality constraints enforce collision avoidance, leader following, and agglomeration behaviors, and they are stabilized using Baumgarte's error stabilization approach. We show that in dense configurations, the positional arrangement of the agents can lead to linearly dependent constraints, and we propose specialized solutions involving QR decomposition and regularization. The efficacy and efficiency of the proposed method are demonstrated by a dimensional analysis of a worst-case scenario and numerical studies of up to 100 agents tracking a prescribed virtual leader.
</details>

- Access our paper via [[paper](https://ieeexplore.ieee.org/document/9354990)].
- Watch the demo via: [[YouTube](https://youtu.be/HkIxFIba1sI)].


### Centralized Control with Vector-Component-Based Constraints 

{% include base_path %}

[//]: # (<center>)

[//]: # (  <img src="../images/CDC21/2Agent-path.png" width="50%" />)

[//]: # (</center>)

<iframe width="200" height="100" src="https://www.youtube.com/embed/ogNqEoryYIQ" title="Two-Agent Deadlock Resolution;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

[//]: # (<center>)

[//]: # (  <img src="../images/CDC21/2Swarm-path.png" width="40%" />)

[//]: # (</center>)

<iframe width="200" height="100" src="https://www.youtube.com/embed/10CXrmDop48" title="Two 15-Agent Swarms Deadlock Resolution;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<details>
  <summary><b>[Abstract]</b></summary>

This paper presents a nonlinear and discontinuous control scheme for two-dimensional (2-D) multi-agent multi-swarm navigation that resolves deadlocks, without heuristics, by agents reacting purely to their constrained dynamics. The method is based on extensions of Gauss's Principle of Least Constraint that dynamically identify, incorporate, and stabilize time-varying sets of constraints and that integrate actuator saturation and delay. The deadlocks are naturally resolved by formulating the 2-D leader following and collision avoidance requirements as decomposed inequality constraints along the X and Y axes and by asymmetrically assigning zero collision avoidance constraint value to a specific branch. Numerical results are presented for two agents and two 15-agent swarms resolving nominal deadlocks at a computation time order of 10 microseconds, demonstrating the efficacy and efficiency of the proposed approach.
</details>

- Access our paper via [[paper](https://ieeexplore.ieee.org/document/9683102)].
- Watch the demos via: [[YouTube-1](https://youtu.be/ogNqEoryYIQ)] and [[YouTube-2](https://youtu.be/10CXrmDop48)].

### Decentralized Control with Vector-Component-Based Constraints 

<iframe width="200" height="100" src="https://www.youtube.com/embed/C0_q3lxDYyY" title="Fully Decentralized Navigation Control of 200 Agents;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<details>
  <summary><b>[Abstract]</b></summary>

In this letter, we introduce a decentralized, nonlinear, discontinuous, and computationally simple control law for large scale multiagent navigation systems. The control is based on extending Gauss's principle of least constraint with a dynamic incorporation of inequality constraints, actuator saturation, and actuator dynamics. With no individual path planner, each agent executes its motion and generates its control actions by reacting solely to the evolution of its constrained dynamics, which is equivalent to solving a linear matrix equation with a dimension up to around 20 without iteration at each time instant. Numerical experiments are conducted on hundreds of two-dimensional (2-D) double integrators subjected to path and collision constraints, demonstrating the promise of the proposed method.

</details>

- Access our paper via [[paper](https://ieeexplore.ieee.org/document/9763476)].
- Watch the demo via: [[YouTube](https://youtu.be/C0_q3lxDYyY)].

{% include base_path %}

## High-Speed Navigation Control of Nonholonomic Wheeled Mobile Robots

### High-Speed Tracking Control of A Two-Wheeled Mobile Robot Subject to Unknown External Disturbances

<iframe width="200" height="100" src="https://www.youtube.com/embed/RdBtaXrZVq8" title="Tracking Control of A High-Speed, Differential Drive Wheeled Mobile Robot under Sinusoidal Forcing;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="200" height="100" src="https://www.youtube.com/embed/hPRplXrn8HQ" title="Tracking Control of A High-Speed, Differential Drive Wheeled Mobile Robot under Gaussian Forcing;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<details>
  <summary><b>[Abstract]</b></summary>

This paper presents a computationally efficient, heuristic-free, and nonlinear feedback control framework for the tracking control of the position and orientation of a differential drive wheeled mobile robot (WMR) subjected to high-speed maneuvers and external disturbances. We synthesize the control law by an extension of Gauss’s principle of least constraint with dynamic incorporation of holonomic and nonholonomic equality constraints and with coordinate transformation. The command control actions for the WMR’s constrained dynamics result from solving a linear matrix equation (a Karush-Kuhn-Tucker system) at each point in time. No dynamics linearization or iterative solution is involved in the framework. Numerical experiments of a high-speed, differential drive WMR under sinusoidal and Gaussian external disturbances are presented to showcase the effectiveness of the proposed method.

</details>

- Access our paper via [[paper](https://ieeexplore.ieee.org/document/10156242)].
- Watch the demos via: [[YouTube-1](https://youtu.be/RdBtaXrZVq8)] and [[YouTube-2](https://youtu.be/hPRplXrn8HQ)].

{% include base_path %}

## Unified Position-Attitude Control of Nonlinear Quadrotor UAVs

### Unified Position and Attitude Control of A Fully Nonlinear Quadrotor

<iframe width="200" height="100" src="https://www.youtube.com/embed/-1QB2EVS2fQ" title="Unified Position and Attitude Control of A Fully Nonlinear Quadrotor;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<details>
  <summary><b>[Abstract]</b></summary>

This paper presents a departure from hierarchical cascade methods to control the position and attitude of a fully nonlinear quadrotor. The paper presents a nonlinear feedback control scheme that simultaneously controls position and attitude. The proposed method is based on a generalization of the Gauss's Principle of Least Constraint (GPLC) for higherorder constrained dynamical systems. By double differentiating the rigid-body position dynamics of a fully nonlinear quadrotor with respect to time, the translational and rotational dynamics become fully coupled at the levels of snap and angular acceleration, and the quadrotor is turned into a fully actuated system in a reduced configuration space. A generalized Baumgarte's error stabilization (BES) is developed to asymptotically drive constraint errors to zero. The nonlinear control law is due purely to the natural evolution of constrained system dynamics. To the best of our knowledge, this is the first instance that GPLC and BES are both extended to higher-order systems and that the control scheme for the position and attitude of a quadrotor is unified into one step by making use of its fully nonlinear constrained dynamics. The efficiency and efficacy of the proposed method is demonstrated by numerical experiments on a quadrotor tracking a prescribed conical spiral.

</details>

- Access our paper via [[paper](https://ieeexplore.ieee.org/document/9483358)].
- Watch the demo via: [[YouTube](https://youtu.be/C0_q3lxDYyY)].


### Centralized, Unified Position-Attitude Control of Multiple Nonlinear Quadrotor UAVs

In this paper, we propose a novel nonlinear feedback control law to maneuver a swarm of nonlinear quadrotors with interagent collision avoidance. In contrast to the predominant hierarchical control architectures and dynamics linearization in controller synthesis in the literature, we control the position and attitude of each drone simultaneously in one unified step, with no dynamics linearization involved at any stage. Our method is based on generalizations of Gauss’s principle of least constraint that allows higher order constrained dynamics and that identifies, stabilizes, and incorporates the time-varying sets of active constraints. The active constraints are asymptotically stabilized to the controlled space according to a generalized constraint stabilization to provide command control actions. Numerical results are provided for a swarm of up to 80 nonlinear quadrotors executing aggressive flights and for eight nonlinear drones swapping positions on a circle, attesting to the efficacy and efficiency of the proposed scheme.

### Decentralized, Unified Position-Attitude Control of Multiple Nonlinear Quadrotor UAVs

<iframe width="200" height="100" src="https://www.youtube.com/embed/HyypDPPdLzk" title="Decentralized Unified Position-Attitude Control of 10 Nonlinear Quadrotor UAVs Following a Virtual Leader;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="200" height="100" src="https://www.youtube.com/embed/ZAmDssH8h74" title="Decentralized Unified Position-Attitude Control of 8 Nonlinear Quadrotor UAVs Swapping Positions on A Circle;" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<details>
  <summary><b>[Abstract]</b></summary>

In this paper, we propose a fully decentralized, nonlinear feedback control law to maneuver multiple nonlinear quadrotor UAVs with interagent collision avoidance and natural deadlock resolution. Most existing work on this problem adopts a cascaded position-attitude control scheme and utilizes linearized dynamics in controller synthesis. In this work, each UAV controls its position and attitude simultaneously in one unified step, with no dynamics linearization involved at any stage. The proposed scheme is based on a generalization of Gauss’s principle of least constraint that allows constrained systems of any order and any type and that identifies, differentiates, stabilizes, partitions, and incorporates the active constraints at each time instant. The control actions result from asymptotically stabilizing the active constraints by user-specified natural frequencies and damping ratios according to a generalized constraint stabilization. Two numerical examples are used to demonstrate the effectiveness of the present method, whose performance on collision avoidance and deadlock resolution is sufficiently close to that of a centralized method.

</details>

- Access our paper via [[paper](https://ieeexplore.ieee.org/document/9992624)].
- Watch the demos via: [[YouTube-1](https://youtu.be/HyypDPPdLzk)] and [[YouTube-2](https://youtu.be/ZAmDssH8h74)].

