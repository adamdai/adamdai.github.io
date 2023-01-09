---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

{% comment %} 
    TODO:
    - embed paper links to title
{% endcomment %}

### Journal Papers
<!-- ============ -->
1. Kousik, S., **Dai, A.**, & Gao, G. (2022). Ellipsotopes: Uniting Ellipsoids and Zonotopes for Reachability Analysis and Fault Detection. *IEEE Transactions on Automatic Control*. [[paper]](https://ieeexplore.ieee.org/document/9832489) [[code]](https://github.com/Stanford-NavLab/ellipsotopes) <!-- July 2022 -->

2. Yu, Y., Nassar, J., Xu, C., Min, J., Yang, Y., **Dai, A.**, ... & Gao, W. (2020). Biofuel-powered soft electronic skin with multiplexed and wireless sensing for human-machine interfaces. *Science robotics*. [[paper]](https://robotics.sciencemag.org/content/5/41/eaaz7946) <!-- April 2022 -->


### Conference Papers
<!-- ============ -->
1. **Dai, A.**, Lund, G., & Gao, G. (2023). PlaneSLAM: Plane-based LiDAR SLAM for Motion Planning in Structured 3D Environments. *IEEE International Conference on Robotics and Automation (ICRA)*. (Submitted) [[paper]](https://arxiv.org/abs/2209.08248) [[code]](https://github.com/Stanford-NavLab/planeslam) <!-- May 2023 -->
2. Shetty, A., **Dai, A.**, Tzikas, A., & Gao, G. (2023). Safeguarding Learning-Based Planners Under Motion and Sensing Uncertainties Using Reachability Analysis. *IEEE International Conference on Robotics and Automation (ICRA)*. (Submitted) [[paper]](https://drive.google.com/file/d/1nUy85KAPGuyS12BPPwr6f4EkbrU95JsG/view?usp=sharing) [[code]](https://github.com/Stanford-NavLab/rover_ros_ws) <!-- May 2023 -->
3. Chung, L. K.\*, **Dai, A.**\*, Knowles, D., Kousik, S., & Gao, G. (2021). Constrained feedforward neural network training via reachability analysis. *Robotics: Science and Systems (RSS) Robotics for People (R4P) Workshop*. [[paper]](https://arxiv.org/abs/2107.07696) [[code]](https://github.com/Stanford-NavLab/constrained-nn-training) <!-- July 2021 -->
4. Liu, Q., Nakahira, Y., Mohideen, A., **Dai, A.**, Choi, S., Pan, A., Ho, D.M., & Doyle, J. C. (2019). "Experimental and educational platforms for studying architecture and tradeoffs in human sensorimotor control." *2019 American Control Conference (ACC)*. [[paper]](https://ieeexplore.ieee.org/document/8814470) <!-- July 2019 -->



\* Equal authorship

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

<!-- {% include base_path %} -->

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
