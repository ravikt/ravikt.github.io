---
layout: page
permalink: /research/
title: Research 
pubs:

    - title:   "Imitation Learning with Human Eye Gaze via Multi-Objective Prediction"
      author:  "Thakur RK, Sunbeam MD, Goecks VG, Novoseller E, Bera R, Lawhern V, Gremillion G, Valasek J, Waytowich NR"
      journal: "ILHF Workshop International Conference on Machine Learning (ICML)"
      #note:    "Volume 56"
      year:    "2023"
      url:     "https://openreview.net/forum?id=MF1Tcmk2YB"
      #doi:     "https://doi.org/10.1016/j.mechatronics.2018.10.006"
      #image:   "https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fimages.moviepostershop.com%2Fthe-matrix-movie-poster-1999-1020518087.jpg&f=1"
      media:
        - name: "video"
          url:  "https://www.youtube.com/watch?v=vFiT293FR1Q"

    - title:   "A Conditional Adversarial Network for Scene Flow Estimation"
      author:  "Thakur, R. K., & Mukherjee, S."
      journal: "IEEE International Conference on Robotics and Human Interactive Communication"
      note:    "RO-MAN"
      year:    "2019"
      url:     "https://ieeexplore.ieee.org/document/8956310"
      doi:     "https://doi.org/10.1109/RO-MAN46459.2019.8956310"
      #image:   "https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fimages.moviepostershop.com%2Fthe-matrix-movie-poster-1999-1020518087.jpg&f=1"
      #media:
      #  - name: "IMDB"
      #    url:  "http://www.imdb.com/title/tt0133093/"

    - title:   "SceneEDNet: A Deep Learning Approach for Scene Flow Estimation"
      author:  "Thakur, R. K., & Mukherjee, S."
      journal: "IEEE International Conference on Control, Automation, Robotics and Vision"
      note:    "ICARCV"
      year:    "2018"
      url:     "https://ieeexplore.ieee.org/abstract/document/8581172"
      doi:     "https://doi.org/10.1109/ICARCV.2018.8581172"
      code:    
      #media:
        - name: "code"
          url:  "https://github.com/ravikt/sceneednet"

    - title:   "Development of an integrated haptic system for simulating upper gastrointestinal endoscopy"
      author:  "Chakravarthy, S., Balakuntala, M. V., Rao, A. M., Thakur, R. K., & Ananthasuresh, G. K."
      journal: "Mechatronics"
      note:    "Volume 56"
      year:    "2018"
      url:     "https://www.sciencedirect.com/science/article/abs/pii/S0957415818301636"
      doi:     "https://doi.org/10.1016/j.mechatronics.2018.10.006"
      #image:   "https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fimages.moviepostershop.com%2Fthe-matrix-movie-poster-1999-1020518087.jpg&f=1"
      media:
        - name: "video"
          url:  "https://www.youtube.com/watch?v=KcMPzj1OfZY"


---

My current research interest is in vision-based autonomy and control for aerospace systems. 

## Publications 

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
