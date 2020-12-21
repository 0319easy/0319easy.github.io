---
layout  : post
title   : '[gas mask] IntelliJ - spring - gas mask 호스트 설정'
categories  : ['omg']
date    : 2020-12-22T01:29:000
---

회사에서 하는 프로젝트가 spring + tomcat 조합과 spring boot + 내장 tomcat 조합이 있다~(귀찮다)~  

로컬로 웹서버 띄워서 개발할 때가 많은데 사실 127.0.0.1이나 localhost로 들어가는게 젤 편하고 좋지만,,  

쿠키 설정 때문에 도메인 뒤쪽을 맞춰줘야 했다ㅠ.ㅠ  

로컬에서의 도메인 이름은 보통 local-\[띄우는 서버의 상용 도메인주소\]로 한다  

글에서 설명하기 쉽게 상용 도메인은 smelting.com이라 하고 로컬 주소는 local-smelting.com이라고 하자  

spring에 tomcat 조합은 run/debug confinguration을 아래처럼 설정해서 사용하고 있다  

![gasmask1](/public/img/gasmask2-1.png)

URL 옵션은 별로 필요 없고 밑에 HTTP port만 잘 알아두면 된다  

![gasmask2](/public/img/gasmask2-5.png)

gas mask에 들어가서 127.0.0.1에 내가 원하는 주소를 넣어놓는다  

그러고 나서 save & activate!  

![gasmask3](/public/img/gasmask2-2.png)

그리고 그냥 chrome이든 사파리든 주소 치고 들어가면 끝~이다  

spring boot 프로젝트의 경우에는  

![gasmask4](/public/img/gasmask2-3.png)

알아서 인텔리제이에서 run/debug configuration을 잡아주고 url이나 http port 설정하는 부분도 없다  

그냥 실행시키고 gas mask에 설정해둔 도메인 + 80 or 8080포트로 들어가면 된다  

![gasmask5](/public/img/gasmask2-4.png)

다른 포트로 바꾸고 싶으면 run/debug configuration에서 parameter를 오버라이딩하면 된다고한다  

or application.yml이나 application.properties파일에서 port를 바꿔주면된다  

(프로젝트 설정이 복잡해서 오버라이딩이 안 먹혀서 나는 아래 방법으로,,ㅠㅠ)  
