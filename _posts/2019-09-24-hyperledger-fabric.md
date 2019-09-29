---
title: 하이퍼레저  패브릭 네트워크 구성하기 - (1) 사전작업
tags:
- blockchain
- hyperledger fabric
date: '2019-09-24 22:38:00'
layout: post
---

<center><img width = "30%" src="/assets/img/hyperledger.png"></center>
<br>
<center><a href = "https://github.com/hlkug/meetup/tree/master/201903" target="_blank">hyperledger korea user group의 2019년 3월 밋업 자료</a>를 바탕으로 네트워크를 구성했습니다.</center>

---
<details>
<summary><h3>1.가상환경 구성</h3></summary>
<div markdown="1">

- Virtual Box 설치 (<a href = "https://www.virtualbox.org/wiki/Downloads" target="_blank">https://www.virtualbox.org/wiki/Downloads</a>)
- Ubuntu 16.04(Server) 다운로드(<a href = "http://ftp.kaist.ac.kr/ubuntu-cd/16.04/ubuntu-16.04.6-server-amd64.iso" target="_blank">http://ftp.kaist.ac.kr/ubuntu-cd/16.04/ubuntu-16.04.6-server-amd64.iso</a>)
- Virtual Box에 VM(Virtual Machine) 생성 및 네트워크 설정 (<a href = "https://dokyeonghan.github.io/2019/09/29/virtual-box-vmvirtual-machine.html" target="_blank">Click</a>)<br>

| **<center>VM 갯수</center>** | <center>2개 </center> |
| **<center>VM 명</center>** | <center>node1, node2 </center> |
| **<center>CPU</center>** | <center>2개 </center> |
| **<center>Memory</center>** | <center>1~2GB </center> |
| **<center>Disk</center>** | <center>15GB~ </center> |

</div>
</details>


---
<details>
<summary><h3>2.Docker 설치</h3></summary>
<div markdown="1">

- 기존 설치된 Docker 엔진 삭제<br>
<span style="color:green">`$ sudo apt-get remove docker docker-engine docker.i`<br><br></span>
- 의존성(depedencies) 패키지 설치<br>
<span style="color:green">`$ sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
software-properties-common`</span><br><br>
- 바이너리 파일 다운<br>
<span style="color:green">`$ sudo curl -sSL https://goo.gl/6wtTN5 | bash -s 1.1.0`<br><br></span>
- Docker 레포지토리 GPG 키 추가<br>
<span style="color:green">`$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`<br><br></span>
- Docker 설치<br>
<span style="color:green">`$ sudo apt-get update `<br>
`$ sudo apt-get install docker-ce`<br><br></span>
- Docker 엔진 제어 권한 부여<br>
<span style="color:green">`$ sudo usermod -a -G docker $USER`<br><br></span>
- 재 로그인 후 설치 확인<br>
<span style="color:green">`$ docker version`</span>

</div>
</details>




---
<details>
<summary><h3>3.Docker Compose 설치</h3></summary>
<div markdown="1">

- Docker Compose 파일을 /usr/local/bin 디렉토리에 다운로드<br>
<span style="color:green">`$ sudo curl -L https://github.com/docker/compose/releases/download/1.23.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose`<br><br></span>
- Docker Compose 파일(docker-compose)에 실행권한 설정<br>
<span style="color:green">`$ sudo chmod +x /usr/local/bin/docker-compose`<br><br></span>
- Docker Compose가 정상적으로 설치되었는 지 확인<br>
<span style="color:green">`$ docker-compose --version`<br></span>

</div>
</details>


---
<details>
<summary><h3>4.First Network 구성하기</h3></summary>
<div markdown="1">

- Github에서 fabric-samples 소스를 다운로드<br>
<span style="color:green">`$ git clone https://github.com/hyperledger/fabric-samples.git ~/fabric-samples`</span><br><br>
- 네트워크 구성에 필요한 바이너리 파일 및 Docker Image 다운로드<br>
<span style="color:green">`$ cd ~/fabric-samples/scripts`</span><br>
<span style="color:green">`$ ./bootstrap.sh 1.4.0`</span><br><br>
- first-network 디렉토리로 이동<br>
<span style="color:green">`$ cd ../first-network`</span><br><br>
- 네트워크 구성에 필요한 MSP, Genesis Block, Channel Tx,…등을 생성<br>
<span style="color:green">`$ sudo ./byfn.sh -m generate`</span><br><br>
- 네트워크 실행하기<br>
<span style="color:green">`$ sudo ./byfn.sh -m up`</span><br><br>
- 네트워크 제거하기<br>
<span style="color:green">`$ sudo ./byfn.sh -m down`</span><br><br>

</div>
</details>


---