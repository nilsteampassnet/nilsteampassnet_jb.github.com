---
layout: page
title: A collaborative Passwords Manager
tagline: Welcome to Teampass.Net
---
{% include JB/setup %}

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)


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
        <!-- TWITTER -->
        <div><br />
        <a href="https://twitter.com/TheTeamPass" class="twitter-follow-button" data-show-count="true" data-lang="en" data-size="large">Follow @theteampass</a>
        <script>!function(d,s,id){var
js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs)$
        </div>
</div>

test

## Update Author Attributes

In `_config.yml` remember to specify your own data:
    
    title : My Blog =)
    
    author :
      name : Name Lastname
      email : blah@email.test
      github : username
      twitter : username

The theme should reference these variables whenever needed.
    
## Latest Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

