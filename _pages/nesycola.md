---
title: "NesyCola"
layout: textlay
excerpt: "NesyCola"
sitemap: false
permalink: /nesycola/
---


{% for p in site.data.projects %}
{% if p.title == page.title %}
{% assign project = p %}
{% endif %}
{% endfor %}

{% assign project = site.data.projects | where: "title", page.title %}
{% assign project = project[0] %}
<div>
<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/projects/{{ project.logo }}" style="width: 90px; float: left; border: 10px; margin-right: 20px"/>
<br>



<!-- ([Members](#members), [Funding](#funding), [Publications](#pubs), [News](#news)) -->





## {{ project.title }} 
<p> {{ project.description }} </p>
</div>
<br>

### Menu

<ul>
<li> <a href="{{ site.url }}{{ site.baseurl }}/domiknows-nlp/">Demo</a> </li>
<li> <a href="{{ site.url }}{{ site.baseurl }}/gluecons/">GLUECons: A generic benchmark for learning under constraints.</a> </li>
<li> <a href="#members">Team</a> </li>
<li> <a href="#fund">Funding</a> </li>
<li> <a href="#newssection">News</a> </li>
<li> <a href="#pubs">Publications</a> </li>
</ul>
<br><br>
<p> {{ project.info }} </p>
<p><img src="{{ site.url }}{{ site.baseurl }}/images/picpic/projects/{{ project.image }}" class="img-responsive" width="80%" style="margin:auto"></p>
<br>
<br>
<h4 id="members"><b>Team Members</b></h4>
<ul>
<li><em> {{ project.members }}. </em> </li>
<li><em>{{project.graduate_students}} </em> </li>
</ul>

<!-- (<p>Github: <strong><a href="{{ project.webpage }}">{{ project.title }}</a></strong></p>)  -->
<br>
<h4 id="fund"><b>Source of funding</b></h4>
<ul>
<li><i>{{ project.funding_resource }}</i> </li>
</ul>

<br>
<h4 id="newssection"><b>News</b></h4>
<ul>
<h5><em> {{ project.news }}. </em></h5>
<h6><em><a href="https://msutoday.msu.edu/news/2023/making-ai-more-reliable">link</a></em></h6>

<h5><em> {{ project.news_2 }}. </em></h5>
<h6><em><a href="https://www.youtube.com/watch?v=EiH6kXfdG6Q">link</a></em></h6>
</ul>

<br>
{% if project.publications %}
<h4 id="pubs">List of <b>publications</b>: </h4>
<br>
{% for pub in project.publications %}
<ul>
<li><strong>{{ pub.title }}</strong>. {{ pub.authors }} {% if pub.webpage %} <a href="{{ pub.webpage }}">More detail</a>. {% endif %} {% if pub.github %} <a href="{{ pub.github }}">GitHub</a>. {% endif %} {% if pub.link %} <a href="{{ pub.link }}">Download</a>. {% endif %} </li>
</ul>
{% endfor %}
{% endif %}
<br>


