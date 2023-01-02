---
layout: archive
permalink: /research/
title: ""
author_profile: true
redirect_from: 
  - /research/
  - /research.md
---

<!-- My research focuses on  -->

<!-- ============================================== -->
## Simultaneous Localization and Mapping
------------------------------------------

### Plane-based SLAM

LiDAR is a powerful sensor, but point cloud maps generated from LiDAR SLAM quickly grow in memory and become expensive
to store. By converting point clouds to sets of planes, we can generate much more lightweight maps.

<p align="middle">
  <img src="{{site.url}}/files/planeslam_env.jpg" width="320" hspace="20" />
  <img src="{{site.url}}/files/planeslam_map.png" width="400" /> 
  <!-- <img src="{{site.url}}/files/planeslam.gif" width="750" /> -->
</p>
<!-- TODO: replace with GIF -->

These plane-based maps also lend themselves to fast collision-checking for motion planning purposes. Given a trajectory,
we can quickly check if the trajectory intersects any planes in the map. This is much faster than checking for collisions with points in the point cloud map.

See the [video](https://www.youtube.com/watch?v=ApqB6rlaen4) for a brief summary of our approach and results.
For more details on the plane extraction process, plane registration, and pose graph backend, see our 
[paper](https://arxiv.org/abs/2209.08248) and [code](https://github.com/Stanford-NavLab/planeslam). 


<!-- ### LiDAR GPS Factor Graphs

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer blandit aliquet neque id accumsan. Praesent vel lorem tincidunt, vestibulum neque sit amet, malesuada nulla. -->


<!-- ============================================== -->
## Reachability Analysis
------------------------------------------

Reachabiity analysis is a powerful tool for motion planning. It allows us to quickly compute the reachable set of a robot
given a set of constraints. This is useful for planning trajectories that avoid obstacles, or for planning trajectories 
that satisfy a set of safety constraints. My work in particular leverages set-based reachability analysis, in which reachable sets are represented as collections of geometric sets.

### Multi-robot trajectory planning
NorCal Control Workshop: Multi-Robot Trajectory Planning using Reachability Analysis 
[video](https://www.youtube.com/watch?v=i1VyQX4kDoQ)
<!-- TODO: replace with GIF -->

<img src="{{site.url}}/files/multi_robot.gif" width="500" style="float: left" />

We can use reachability analysis to plan trajectories online for multiple robots that avoid collisions. Each robot plans
in a decentralized manner, computing a collision-free trajectory based on other robots' reachable sets, then broadcasting
its trajectory to the other robots. This approach is scalable to large numbers of robots, and can be used to guarantee safety even in the presence of robot sensing and motion uncertainties.

Currently, we are working in collaboration with JPL's Cooperative Autonomous Distributed Robotic Exploration (CADRE) team 
to apply this approach to exploration of the moon's surface with multiple rovers. 


### Novel representations: Ellipsotopes

<!-- <figure>
  <img src="{{site.url}}/files/etopes.png" width="100" style="float: right" />
  <figcaption>Fig.1 - Trulli, Puglia, Italy.</figcaption>
</figure> -->
<img src="{{site.url}}/files/etopes.png" width="400" style="float: right" />
<!-- TODO: create GIF of robot body + uncertainty being computed -->

Set-based reachability analysis hinges the choice of set representation for the reachable set. In particular, the choice of set representation can have a significant impact on the computational complexity of the reachability analysis. 
In this work, we introduced a novel set representation called an ellipsotope, which is a generalization of two popular set representations: ellipsoids and polytopes. Ellipsotopes allow us to combine the advantages of both ellipsoids and polytopes, while preserving computational efficiency of fundamental operations such as intersection and collision-checking.
For example, with ellipsotopes, we can exactly represent the reachable set of a robot with a polytopic body and Gaussian uncertainty in its dynamics, which would not be possible with ellipsoids or polytopes alone.

For more details, check out our [paper](https://ieeexplore.ieee.org/document/9832489).

### Neural network verification

<img src="{{site.url}}/files/nn_safety.png" width="500" style="float: left"  hspace="20"/>
<!-- TODO: generate GIF of training over time -->

In addition to guaranteeing safety of robot trajectories, we can also use reachability to verify and enforce safety of neural networks. Representing the set of possible inputs to a neural network as a polytope, we can use reachability analysis to compute the reachable set of the neural network's output. This allows us to verify that the neural network satisfies safety constraints, and to compute the set of inputs that will cause the neural network to violate safety constraints. Furthermore, we can re-train the network using a differentiable collision check to push the output reachable set out of collision with an unsafe set and into safety.

For more details, check out the [paper](https://arxiv.org/abs/2107.07696).

