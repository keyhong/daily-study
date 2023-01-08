<header>
  <h2> VS Code에서 원격 PC에 SSH로 연결하기 </h2>
</header>

<body>
  
  <dl>
    <li> (Windows) /etc/hosts 구성 </li>
    <pre> [ip] [HOSTNAME] [Alias] </pre>
  </dl>

  <dl>
    <li> VS Code에서 ssh로 aws 접속하는 법 </li>
<pre>
&#35; 1. 확장팩 설치 : Remote - SSH
&#35; 2. Ctrl + P로 "원격-SSH: 호스트에 연결..." 선택
&#35; 3. "SSH 호스트 구성..." 선택
&#35; 4. local의 계정의 config 선택
&#35; 5. config 파일 작성
</pre>
  </dl>

  <dl>
    <li> VS Code에서 config 파일 작성하기 </li>
<pre>
Host DataLake2 # VS Code에서 앞으로 설정할 호스트 별칭
    HostName DH_DataLake_02 # 접속할 원격 PC의 [IP] 혹은 [IP의 HOSTNAME]
    User b2en # 접속할 원격 PC의 사용자 계정
    port 22 # 접속할 포트 번호 (SSH는 보통 22번 포트 사용)
</pre>
  </dl>  
</body>
