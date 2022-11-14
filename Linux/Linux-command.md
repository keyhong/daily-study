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
  
</body>
