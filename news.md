---
layout: default
title: Anvishi News
permalink: /news/
---

    <div id="content">
    
    <h2>News from across Anvishi Holdings and Ventures:</h2>
    <ul class="post-list">
    {% for post in paginator.posts %}
      <li><span class="datetitle"><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></span><br /><span class="excerpt-text">{{ post.excerpt | remove: '<p>' | remove: '</p>' | strip_html | truncatewords:50 }} <a href="{{ post.url | prepend: site.baseurl }}">Read more....</a></span></li>
      
    {% endfor %}
  </ul>
  <hr />
  <div class="pagination" align="center">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">Previous</a>
  {% else %}
    <span class="previous">Previous</span>
  {% endif %}
  <span class="page_number ">Page: {{ paginator.page }} of {{ paginator.total_pages }}</span>
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% else %}
    <span class="next ">Next</span>
  {% endif %}
</div>
</div>

  </div>
  

</div>
