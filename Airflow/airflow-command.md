<header>
  <h2> Airflow 커맨드 정리 </h2>
</header>

<body>
 
  <dl>
    <li> 메타데이터 DB 초기화  </li>
    <pre> airflow db init </pre>
  </dl><hr>  

  <dl>
    <li> 메타데이터 DB 소각 및 재구축기  </li>
    <pre> airflow db reset </pre>
  </dl><hr>  

  <dl>
    <li> Airflow 유저 생성 </li>
<pre>
airflow users create \
--username <유저> \
--password <비밀번호> \
--firstname <성> \
--lastname <이름> \
--email <이메일> \
</pre>
  </dl><hr> 

  <dl>
    <li> Airflow 유저 조회 </li>
    <pre>airflow users list </pre>
  </dl><hr> 
  
</body>
