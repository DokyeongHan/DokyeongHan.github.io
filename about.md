---
title: About
layout: page
permalink: "/about/"
---

<h1>{{ site.theme_settings.name}} </h1>
![avatar]({{ site.theme_settings.avatar }})

<p>Dept. of Computer Science. Kangwon National Univ.</p>

<p>Chuncheon, Kangwon, Republic of Korea.</p>

<p>Email : dkhan@kangwon.ac.kr</p>



<div id = "map" style = "width:100%;height:400px;"></div>

<script type="text/javascript" src="//dapi.kakao.com/v2/maps/sdk.js?appkey=9847219f5cf71d8e7d7d258ff825eb77"></script>
<script>
var mapContainer = document.getElementById('map'), // 지도를 표시할 div 
    mapOption = { 
        center: new daum.maps.LatLng(37.86874913546466, 127.7379924938739), // 지도의 중심좌표
        level: 3 // 지도의 확대 레벨
    };

var map = new daum.maps.Map(mapContainer, mapOption); // 지도를 생성합니다

// 마커가 표시될 위치입니다 
var markerPosition  = new daum.maps.LatLng(37.86874913546466, 127.7379924938739); 

// 마커를 생성합니다
var marker = new daum.maps.Marker({
    position: markerPosition
});

// 마커가 지도 위에 표시되도록 설정합니다
marker.setMap(map);

// 아래 코드는 지도 위의 마커를 제거하는 코드입니다
// marker.setMap(null);    
</script>