---
layout: page
title: A collaborative Passwords Manager
tagline: Welcome to Teampass.Net
---
{% include JB/setup %}


<div class="post">
	TeamPass is a Passwords Manager dedicated for managing passwords in a collaborative way on any server Apache, MySQL and PHP. It is especially designed to 
provide passwords access security for allowed people. This makes TeamPass really useful in a Business/Enterprise environment and will provide to IT or Team Manager a 
powerful and easy tool for customizing passwords access depending on the user's role.
<br />
</div>

## Follow Teampass
<div class="posts">
        <!-- FACEBOOK -->
        <div id="fb-root"></div>
        <script>(function(d, s, id) {
                var js, fjs = d.getElementsByTagName(s)[0];
                if (d.getElementById(id)) return;
                js = d.createElement(s); js.id = id;
                js.src = "//connect.facebook.net/fr_FR/all.js#xfbml=1&appId=244629032269611";
                fjs.parentNode.insertBefore(js, fjs);
        }(document, 'script', 'facebook-jssdk'));</script>
        <div class="fb-like-box" data-href="http://www.facebook.com/pages/TeamPass-Passwords-for-Teams/163627833721400" data-width="600" data-show-faces="true"
data-header="false" data-stream="false" data-show-border="false"></div>
        <br /><br />
        <!-- TWITTER -->
        <a href="https://twitter.com/TheTeamPass" class="twitter-follow-button" data-show-count="true" data-lang="en" data-size="large">Follow @theteampass</a>
        <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
	<br />
</div>

## Latest Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



<div class="posts">
<br /><br />
</div>


<div class="posts">
	<h1 class="post-title">
		Last Posts
	</h1>
  {% for post in paginator.posts %}
  <div class="post">
    <h2 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>
    <span class="post-date">
			{{ post.date | date_to_string }} *
			<a href="{{ site.baseurl }}{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.path | split:'/' | last | cgi_escape }}">View 
Comments</a>
		</span>
		{% if post.content contains '<span class="linkmore"></span>' %}
			{{ post.content | split:'<span class="linkmore"></span>' | first }}
			<p><a href="{{ site.baseurl }}{{ post.url }}">[Continue reading]</a></p>
		{% else %}
				{{ post.content }}
		{% endif %}
		
  </div>
  {% endfor %}
	
</div>
<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ site.baseurl }}/page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="{{ site.baseurl }}/">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="{{ site.baseurl }}/page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div>
