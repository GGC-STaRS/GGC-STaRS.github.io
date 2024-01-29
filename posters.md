---
layout: about
title: Posters
permalink: /posters/
posters:
    
# use categories for stars2021 and posters/activities/etc
# and use tags for discipline (so it can have multiple)
# go through tags in this page? or show tags next to title?
---
 <style>
    .blue-tag {
        color: #fff !important;
        border-radius: 4px;
        background-color: #2196F3 !important;
        padding-left: 8px;
        padding-right: 8px;
        text-align: center;
    }
    .red-tag {
        color: #fff !important;
        border-radius: 4px;
        background-color: #f44336 !important;
        padding-left: 8px;
        padding-right: 8px;
        text-align: center;
    }
 </style>
 
<!-- ### ✨ Poster Submission Instructions ✨

Please follow instructions in <a href="https://ggc-stars.github.io/stars2021/update/2021/03/07/poster-submission-instructions.html"> this post </a> to submit your posters.

### ✨ Poster Judging Information ✨

Posters will be judged according to criteria posted <a href="https://ggc-stars.github.io/stars2021/update/2021/03/09/rubrics-feedback-posters.html">here</a>.

Note: <b>Live presentations of posters are preferred over pre-recorded videos of posters. Submissions with only pre-recorded videos get 1 pt deduction from final score.</b>

### ✨ STaRS 2021 Posters ✨

👏👏THANK YOU to all participating students and faculty! 👏👏
-->

### ✨ STaRS 2021 Poster Competition Winners✨

🔥🔥🔥 Congratulations to our top 3 winners and all honorable mentions that scored within 3 points from the podium.🔥🔥🔥

👏👏THANK YOU to all participating students and faculty! 👏👏

<div class="page-segments">
    <ul class="page-segments-list">
    {% for poster in site.data.stars2021.posters %}
        <li style="list-style-type: 'P{{ poster["id"] }}. '">
            <span class="post-meta">{{ poster["students"] }} - supervised by {{ poster["advisor"] }}</span><br>
            <span>
                <a class="post-link" href="{{ poster["group"] | datapage_url: '/posters' | relative_url }}">
                {{ poster["group"] | escape }}
                </a>
            </span><br>
            {% assign tag_list = poster["subject"] | split: "," %}
            <span class="post-excerpt">
                {% for tag in tag_list %}
                {% assign naked_tag = tag | strip %}
                    {% if tag contains "place" or tag contains "Honorable" %}
                        <span class="red-tag">{{ site.subject_emojis[naked_tag] }}</span>
                    {% else %}
                        <span class="blue-tag">{{ site.subject_emojis[naked_tag] }}</span>
                    {% endif %}
                {% endfor %}
                    {% assign score = poster["Judge score"] | round %}
                    {% if score > 1000 and poster["Judged?"] == "Yes" %}
                        <span class="red-tag">Competing 🏃‍♂️ </span>
                    {% endif %}
            </span>
        </li>
    {% endfor %}
</ul>
</div>



