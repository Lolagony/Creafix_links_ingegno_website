---
title:  "Creafix Mini Machines"
date:   2023-04-14 11:11:07 +0200
categories: jekyll update
permalink: "/Creafix/machine-sets/Creafix_Mini_Machines"
---
<b>What you need:<br></b>
{% for partM in site.data.parts_machines %}
{% if partM.Mini_Machines == null %}
{% else %}
[![{{ partM.PartName }} image](https://www.viewhotels.jp/ryogoku/wp-content/uploads/sites/9/2020/03/test-img.jpg)]({{ partM.Link }})<br>
<b>{{ partM.PartName }}</b> x {{ partM.Mini_Machines }} [Part link]({{ partM.Link }})
{% endif %}
{% endfor %}
