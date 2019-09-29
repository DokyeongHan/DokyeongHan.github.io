---
title: Virtual Box에 VM(Virtual Machine) 생성 및 네트워크 설정
tags:
- virtual box
- hyperledger fabric
layout: post
date: '2019-09-29 16:20:40'
---

<center><img width = "30%" src="/assets/img/hyperledger.png"></center>

<center><a href = "https://dokyeonghan.github.io/2019/09/24/hyperledger-fabric.html" target="_blank">하이퍼레저  패브릭 네트워크 구성하기 - (1) 사전작업</a>의 <br>Virtual Box에 VM(Virtual Machine) 생성 및 네트워크 설정 과정입니다.</center>

| **<center>VM 갯수</center>** | <center>2개 </center> |
| **<center>VM 명</center>** | <center>node1, node2 </center> |
| **<center>CPU</center>** | <center>2개 </center> |
| **<center>Memory</center>** | <center>1~2GB </center> |
| **<center>Disk</center>** | <center>15GB~ </center> |

<br>
<center>1.새로 만들기</center>
<center><img width = "80%" src="/assets/img/virtual/1virtual.png"></center><br>
<center>2.Name, Folder, 종류, 버전 설정</center>
<center><img width = "80%" src="/assets/img/virtual/2virtual.png"></center><br>
<center>3.메모리 설정</center>
<center><img width = "80%" src="/assets/img/virtual/3virtual.png"></center><br>
<center>4.지금 새 가상 디스크 만들기</center>
<center><img width = "80%" src="/assets/img/virtual/4virtual.png"></center><br>
<center>5.VDI (virtualbox 디스크 이미지)</center>
<center><img width = "80%" src="/assets/img/virtual/5virtual.png"></center><br>
<center>6.동적 할당</center>
<center><img width = "80%" src="/assets/img/virtual/6virtual.png"></center><br>
<center>7.하드디스크 크기(15GB~)</center>
<center><img width = "80%" src="/assets/img/virtual/7virtual.png"></center><br>
<center>8.생성 완료</center>
<center><img width = "80%" src="/assets/img/virtual/8virtual.png"></center><br>
<center>9.시동 디스크 선택</center>
<center><img width = "80%" src="/assets/img/virtual/9virtual.png"></center><br>
<center>10.한국어</center>
<center><img width = "80%" src="/assets/img/virtual/10virtual.png"></center><br>
<center>11.우분투 서버 설치</center>
<center><img width = "80%" src="/assets/img/virtual/11virtual.png"></center><br>
<center>12.예</center>
<center><img width = "80%" src="/assets/img/virtual/12virtual.png"></center><br>
<center>13.대한민국</center>
<center><img width = "80%" src="/assets/img/virtual/13virtual.png"></center><br>
<center>14.아니요</center>
<center><img width = "80%" src="/assets/img/virtual/14virtual.png"></center><br>
<center>15.English (US)</center>
<center><img width = "80%" src="/assets/img/virtual/15virtual.png"></center><br>
<center>16.English (US)</center>
<center><img width = "80%" src="/assets/img/virtual/16virtual.png"></center><br>
<center>17.호스트 이름 설정</center>
<center><img width = "80%" src="/assets/img/virtual/17virtual.png"></center><br>
<center>18.사용자 이름 설정</center>
<center><img width = "80%" src="/assets/img/virtual/18virtual.png"></center><br>
<center>19.사용자 이름 설정</center>
<center><img width = "80%" src="/assets/img/virtual/19virtual.png"></center><br>
<center>20.암호 설정</center>
<center><img width = "80%" src="/assets/img/virtual/20virtual.png"></center><br>
<center>21.아니요</center>
<center><img width = "80%" src="/assets/img/virtual/21virtual.png"></center><br>
<center>22.예</center>
<center><img width = "80%" src="/assets/img/virtual/22virtual.png"></center><br>
<center>23.자동 - 디스크 전체 사용하고 LVM 설정</center>
<center><img width = "80%" src="/assets/img/virtual/23virtual.png"></center><br>
<center>24.확인</center>
<center><img width = "80%" src="/assets/img/virtual/24virtual.png"></center><br>
<center>25.예</center>
<center><img width = "80%" src="/assets/img/virtual/25virtual.png"></center><br>
<center>26.계속</center>
<center><img width = "80%" src="/assets/img/virtual/26virtual.png"></center><br>
<center>27.예</center>
<center><img width = "80%" src="/assets/img/virtual/27virtual.png"></center><br>
<center>28.계속</center>
<center><img width = "80%" src="/assets/img/virtual/28virtual.png"></center><br>
<center>29.자동 업데이트 하지 않음</center>
<center><img width = "80%" src="/assets/img/virtual/29virtual.png"></center><br>
<center>30.스페이스바로 체크하고 계속</center>
<center><img width = "80%" src="/assets/img/virtual/30virtual.png"></center><br>
<center>31.예</center>
<center><img width = "80%" src="/assets/img/virtual/31virtual.png"></center><br>
<center>32.계속</center>
<center><img width = "80%" src="/assets/img/virtual/32virtual.png"></center><br>
<center>33.로그인</center>
<center><img width = "80%" src="/assets/img/virtual/33virtual.png"></center><br>
<center>34.로그인 성공</center>
<center><img width = "80%" src="/assets/img/virtual/34virtual.png"></center><br>
<center>35.VM간 통신을 위해 어댑터 2에 호스트 전용 어댑터를 설정</center>
<center><img width = "80%" src="/assets/img/virtual/35virtual.png"></center><br>
<center>36.호스트 네트워크 관리자</center>
<center><img width = "80%" src="/assets/img/virtual/36virtual.png"></center><br>
<center>37.IP주소: 192.168.56.1 <br>서브넷 마스크: 255.255.255.0</center>
<center><img width = "80%" src="/assets/img/virtual/37virtual.png"></center><br>
<center>38.설정</center>
<center><img width = "80%" src="/assets/img/virtual/38virtual.png"></center><br>
<center>39.어탭터2 설정</center>
<center><img width = "80%" src="/assets/img/virtual/39virtual.png"></center><br>
<center>40.sudo vi /etc/network/interfaces 로 수정</center>
<center>node1 VM - 192.168.56.2</center>
<center>node2 VM - 192.168.56.3</center>
<center><img width = "80%" src="/assets/img/virtual/41virtual.png"></center><br>
<center>41.sudo systemctl restart networking 로 네트워크 서비스 재시작</center>
<br><br>