---
title: About Han
layout: default
---

<h1 class="owner-name"><tt>{{ site.owner.name}}</tt> </h1>
![user-avatar]({{ site.owner.avatar }})


<p>Dept. of Computer Science. Kangwon National Univ.</p>

<p>ChunCheon, Kangwon, Republic of Korea.</p>

<p>Email : dkhan@kangwon.ac.kr</p>

{{site.about}}

<div id="map" style="width:500px;height:400px;"></div>

<script type="text/javascript" src="//dapi.kakao.com/v2/maps/sdk.js?appkey= 13aa235812cf144e4e2c4706cc4a063c."></script>

<script>
var container = document.getElementById('map'); 
var options = {
	center: new daum.maps.LatLng(33.450701, 126.570667), 
	level: 3 
};
</script>

<div class="pagination">
  {% if site.owner.linkedin %}
    <a href="{{ site.owner.linkedin }}" class="social-media-icons"><i class="fa fa-2x fa-linkedin" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.email %}
    <a href="mailto:{{ site.owner.email }}" class="social-media-icons"><i class="fa fa-2x fa-envelope" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.twitter %}
    <a href="{{ site.owner.twitter }}" class="social-media-icons"><i class="fa fa-2x fa-twitter" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.github %}
    <a href="{{ site.owner.github }}" class="social-media-icons"><i class="fa fa-2x fa-github" aria-hidden="true"></i></a>
  {% endif %}
  {% if site.owner.stackexchange %}
    <a href="{{ site.owner.stackexchange }}" class="social-media-icons"><i class="fa fa-2x fa-stack-overflow" aria-hidden="true"></i></a>
  {% endif %}
</div>