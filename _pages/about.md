---
layout: about
title: Home
permalink: /
nav: true
nav_rank: 1
sitetitle: true
description: Welcome to the DAIR Group at Peking University.

profile:
    name: Prof. Dr. Wentao Zhang
    position: Head of the DAIR Group
    align: right
    image: wentao.png
    href: '/members/salvaneschi'
    email: wentao.zhang@pku.edu.cn
    address: >
        Center of Machine Learning Research<br />
        Courtyard No.6, Jingyuan<br />
        PKU, Beijing, China

news: true # includes a list of news items
projects: true # includes a tile list of projects
supports: true # includes a tile list of supports
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false  # includes social icons at the bottom of the page
---

> <i class="fas fa-quote-left"></i>
> “Where should I go?” –&nbsp;Alice. <br />
> “That depends on where you want to end up.” –&nbsp;The&nbsp;Cheshire&nbsp;Cat.
> <i class="fas fa-quote-right"></i><br />
> —&nbsp;Lewis Carroll

Welcome to the DAIR Group!
We are part of the [Center of Machine Learning Research (CMLR)](https://cmlr.pku.edu.cn/){: target="_blank"} at the [University of Peking University (PKU)](https://www.pku.edu.cn/){: target="_blank"}. 
Together we enjoy working on **Data-centric Machine Learning**, **Graph Machine Learning**, 
**Machine Learning Systems**, and **Interdisciplinary Applications**.

[Talk to us](mailto:wentao.zhang@pku.edu.cn) or
[join our group]({{ '/open-positions' | relative_url }})
when you are interested in these topics or our work.
Students at PKU,
please find [our courses, theses, and jobs]({{ '/teaching' | relative_url }}).
{: class="clearfix"}

{% assign members = site.members | where: "team_frontpage", true | sort: "lastname" %}
<div class="d-flex flex-wrap align-content-stretch justify-content-center m-n2 pt-5 no-gutters">
    {% for member in members %}
        {% assign colsMod6 = forloop.length | modulo: 6 %}
        {% assign colIdMod4 = forloop.index | modulo: 4 %}
        {% if colsMod6 == 1 and colIdMod4 == 1 %}<div class="col-md-2 w-100"></div>{% endif %}
        <div class="col-6 col-sm-3 col-md-2 mb-3">
            <a href="{{ member.url | relative_url }}" class="no-decoration">
                <div class="card hoverable h-100 m-2">
                    <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img-top" alt="{{ member.profile.name }}" />
                    <div class="card-body p-2">
                        <div class="card-title m-0">{{ member.title }}</div>
                    </div>
                </div>
            </a>
        </div>
    {% endfor %}
</div>
