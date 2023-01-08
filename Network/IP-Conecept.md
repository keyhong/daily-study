<header>
  <h2> HiveQL DDL(Data Definition Language) 정리 </h2>
</header>

<body>
 
  <dl>
    <li> 아이피(IP, Internet Protocol) </li>
<pre>
&#35; 인터넷에서 다른 컴퓨터와 통신할 때 사용하는 프로토콜 <br>
&#35; 컴퓨터의 논리적 주소를 구분 (구분자는 dot(.)을 사용) <br>
&#35; 1과 0으로 표현 <br>
&#35; IP 주소 체계
(1) IPv4 (Internet Protocol version 4)
&#45; 8비트씩(2^8 bit) 4부분으로 10진수(0&#126;255)로 표시
&#45; 약 43억개의 주소를 표현 가능
&#45; 예) 202.30.64.22 <br>
(2) IPv6 (Internet Protocol version 6)
&#45; 16비트씩(2^16 bit) 8부분으로 16진수(0000&#126;ffff)로 표시
&#45; 약 43억×43억×43억×43억개의 주소를 표현 가능 
&#45; 예) 2001:0230:abcd:ffff:0000:0000:ffff:1111
</pre>
  </dl><hr>
  
  <li> 웹(web)에 접속할 때 </li>
<pre>
&#35; 웹(web)에 접속할 때 DNS(Domain Name Service)와 통신함으로써 IP주소를 얻어낸다
&#35; 인터넷 주소창에 "https://www.naver.com/" 검색 &#61;&#62; DNS 서버를 통해 네이버의 IP주소를 획득 => IP주소로 접속

&#35; cmd 창에서 nslookup (name server lookup) 명령어를 통해 확인 가능
&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;
서버:    kns.kornet.net
Address:  168.126.63.1

권한 없는 응답:
이름:    naver.com
Addresses:  223.130.200.107
          223.130.195.200
          223.130.195.95
          223.130.200.104
&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;&#61;
</pre>
  </dl><hr>
  
  <dl>
    <li> 공인 IP </li>
    <pre> 세계에서 단 하나만 존재하는 IP 주소 </pre>  
  </dl><hr>
  
  <dl>
    <li> 사설 IP </li>
    <pre> 공유기(라우터)를 이용해 만들 수 있는 가상의 IP 주소 </pre>  
  </dl><hr>

  <dl>
    <li> 고정 IP </li>
    <pre> 해당 컴퓨터의 IP 주소를 고정적으로 사용 </pre>  
  </dl><hr>

  <dl>
    <li> 유동 IP </li>
    <pre> 수시로 변화하는 IP 주소 </pre>  
  </dl><hr>  
 
</body>