---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

\* Equal authorship

Journal Papers
======
1. Kousik, S., **Dai, A.**, & Gao, G. X. (2022). Ellipsotopes: Uniting Ellipsoids and Zonotopes for Reachability Analysis and Fault Detection. *IEEE Transactions on Automatic Control*.
2. Yu, Y., Nassar, J., Xu, C., Min, J., Yang, Y., **Dai, A.**, ... & Gao, W. (2020). Biofuel-powered soft electronic skin with multiplexed and wireless sensing for human-machine interfaces. *Science robotics*, 5(41), eaaz7946.


Conference Papers
======
1. **Dai, A.**, Lund, G., & Gao, G. (2022). PlaneSLAM: Plane-based LiDAR SLAM for Motion Planning in Structured 3D Environments. *IEEE International Conference on Robotics and Automation (ICRA)*. Submitted.
2. Shetty, A., **Dai, A.**, Tzikas, A., & Gao, G. (2022). Reachability-based motion planning for quadrotors in 3D environments. *IEEE International Conference on Robotics and Automation (ICRA)*. Submitted.
3. Chung, L. K.\*, **Dai, A.**\*, Knowles, D., Kousik, S., & Gao, G. X. (2021). Constrained feedforward neural network training via reachability analysis. *Robotics: Science and Systems (RSS) Robotics for People (R4P) Workshop*.
4. Liu, Q., Nakahira, Y., Mohideen, **A., Dai**, A., Choi, S., Pan, A., ... & Doyle, J. C. (2019, July). Experimental and educational platforms for studying architecture and tradeoffs in human sensorimotor control. *2019 American Control Conference (ACC)* (pp. 483-488). IEEE.



{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

<!-- {% include base_path %} -->

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
