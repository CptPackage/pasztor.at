---
layout: home
description: Latest posts by Janos Pasztor
---

{% assign posts = site.posts | where_exp:"post","post.date < site.time" %}
<div class="wall">
<div class="wall__featurelist">
    {% for post in posts limit:2 %}
        {% include wall-post.html categorylabel=true %}
    {% endfor %}
</div>
<div class="wall__postlist">
    {% for post in posts offset:2 limit:12 %}
        {% include wall-post-noimage.html categorylabel=true %}
    {% endfor %}
</div>
</div>

<div class="readmore">
    <div class="readmore__cta">Do you want more? Click the buttons below!</div>
    <div class="readmore__buttons">
        <a href="/speaking" class="readmore__button">Talks</a>
        <a href="/workshops" class="readmore__button">Workshops</a>
        <a href="/videos" class="readmore__button">Videos</a>
        <a href="/blog" class="readmore__button">Blog</a>
    </div>
</div>