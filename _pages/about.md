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
     <!-- 核心逻辑：
       1. site.updates - Jekyll自动读取_updates文件夹中的所有文件，形成一个集合
       2. | sort: 'date' - 管道符后的sort按照每个文件中的date字段排序
       3. | reverse - 反转排序（从新到旧）
       4. assign sorted_updates - 将排序后的结果赋值给变量sorted_updates
  -->
  {% for update in sorted_updates limit:5 %}
   <!-- 循环遍历sorted_updates变量 limit:5 - 限制只循环前5个元素（最新的5条更新）;每次循环中，当前项存储在update变量中-->
    <div class="update-item" style="margin-bottom: 15px; padding-bottom: 10px; border-bottom: 1px solid #eee;">
      <!-- 标题链接 -->
      <h3 style="margin-bottom: 5px; font-size: 1.1em;">
        <a href="{{ update.url | relative_url }}">{{ update.title }}</a>
      </h3>
      <!-- 日期 -->
      <p style="color: #666; font-size: 0.85em; margin: 0;">
        {{ update.date | date: "%B %d, %Y" }}
      </p>
    </div>
  {% endfor %}
</div>

<p style="text-align: right; margin-top: 20px;">
  <a href="{{ '/updates/' | relative_url }}" style="font-weight: bold;">View All Updates →</a>
</p>




