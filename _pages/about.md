---
permalink: /
title: "Welcome to the Lab of Mobility Optimization and DEcision Science (MODES) at HKUST(GZ)"
author_profile: true

---

![lab](/images/MODES-3.png)

Led by Dr. Xiaotong Sun, the Lab of Mobility Optimization and DEcision Science (MODES) at HKUST (Guangzhou) focuses on the **planning, operation, and regulation** of multi-modal transportation systems empowered by emerging technologies. Drawing on analytical optimization, game theory, and data-driven approaches, MODES advances research through a **dual lens**: modeling to understand how complex transportation systems operate, and optimizing to enhance their performance.



Research Highlights
======
![1](../images/research-highlight.jpg)<br>

Recently Updates
======
1. Advance Notice: Xiaotong will attend ISTDM 2025 in Montréal, Canada, from September 3–5, 2025, and deliver presentations.
2. Professor Sun, Manlian, Miaowei, Wenjie attended the 16th International Workshop on Computational Transportation Science in Wuhan，Chinese from July 25 to 27, 2025, and made presentations.
3. Chaoyu attended ITEA in Northwest University, Chicago, America from June 23 to 27, 2025, and made presentations.
4. Hangyu published an article in Transportation Research Part C on June 22, 2025.
5. Xinzhu attended Transportation Science and Logistics Conference in Seoul，Korea from May 19 to 21, 2025, and made presentations.
   
Recently Updates Test
======
{% comment %}
  自动从_updates文件夹获取最新的5条更新
  按日期降序排列，只显示最近的内容
{% endcomment %}

<div class="recent-updates">
  {% assign sorted_updates = site.updates | sort: 'date' | reverse %}
  {% for update in sorted_updates limit:5 %}
    <div class="update-item" style="margin-bottom: 20px; padding-bottom: 15px; border-bottom: 1px solid #eee;">
      <h3 style="margin-bottom: 5px;">
        <a href="{{ update.url | relative_url }}">{{ update.title }}</a>
      </h3>
      <p style="color: #666; font-size: 0.9em; margin-bottom: 10px;">
        {{ update.date | date: "%B %d, %Y" }}
      </p>
      {% if update.excerpt %}
        <p style="margin-bottom: 5px;">{{ update.excerpt | strip_html | truncate: 200 }}</p>
      {% endif %}
      {% if update.image %}
        <img src="{{ update.image | relative_url }}" alt="{{ update.title }}" style="max-width: 100%; height: auto; margin-top: 10px;">
      {% endif %}
    </div>
  {% endfor %}
</div>

<p style="text-align: right; margin-top: 20px;">
  <a href="{{ '/updates/' | relative_url }}" style="font-weight: bold;">View All Updates →</a>
</p>




