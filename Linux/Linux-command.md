<header>
  <h2> Linux CLI(Command Line Interface) 정리 </h2>
</header>

<body>
  
  <dl>
    <li> 압축 / 압축해제 </li>
<pre>
* tar [-option]<hr>
<li>-c : 파일을 tar로 압축</li>
<li>-x : tar 압축풀기</li>
<li>-f : 파일 이름을 지정</li>
<li>-z : gzip으로 압축하거나 gzip(tar.gz) 해제</li>
</ol><hr>
<ol>
<li>tar 압축을 할 때 : tar -cvf [압축파일명.tar] [폴더명] </li>
<li>tar 압축을 풀 때 : tar -cxvf [압축파일명.tar] </li>
<li>tar.gz 압축을 할 때 : tar -cvf [압축파일명.tar] [폴더명] </li>
<li>tar.gz 압축을 풀 때 : tar -xvf [압축파일] </li>
</pre>
  </dl><hr>
  
  <dl>
    <li> CPU 정보 확인 </li>
    <pre> cat /etc/proc/cpuinfo </pre>
  </dl><hr>
  
  <dl>
    <li> JVM 위에서 구동되는 프로세스 확인 </li>
    <pre> jps </pre>
  </dl><hr>
  
  <dl>
    <li> 네트워크 연결 확인 </li>
<pre>
* netstat [-option]<hr>
<li>-a: 모두 </li>
<li>-n : 포트넘버 </li>
<li>-t : TCP(Transaction Control Protocol) </li>
<li>-u : UDP(User Datagram Protocol) </li>
<li>-p : PID (Process ID) </li>
</ol><hr>
<ol>
<li>tar 오픈된 포트 보기 : netstat -antup | grep LISTEN | sort -n </li>
</pre>
  </dl><hr>  
  
</body>
