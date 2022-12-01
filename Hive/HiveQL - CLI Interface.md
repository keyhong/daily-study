   <dl>
    <li> hive CLI로 DML 명령어 실행하기 (** 환경변수(PATH)에 hive binary 파일의 경로가 등록되어 있어야, 어떤 폴더에서든 실행 가능) </li>
    <pre> hive -e &lt;쿼리&gt; <br> EX) hive -e "SELECT * FROM SOSS.DM_SAFE_IDEX_GRID WHERE PT_STDR_DE = 20221201" </pre>
  </dl><hr>
 
   <dl>
    <li> hive CLI로 DML 명령어 실행하기 (컬럼명까지 출력하기 - hive.cli.print.header 옵션)  </li>
    <pre> hive --hiveconf hive.cli.print.header=True -e &lt;쿼리&gt; <br> EX) hive --hiveconf hive.cli.print.header=True -e "SELECT * FROM SOSS.DM_SAFE_IDEX_GRID WHERE PT_STDR_DE = 20221201" </pre></pre>
  </dl><hr>
 
   <dl>
    <li> hive CLI로 스크립트 명령어 실행하기  </li>
    <pre> hive -f &lt;쿼리 스크립트&gt; <br> EX) hive -f &lt;select_idex_info.hql&gt; </pre>
  </dl><hr>

   <dl>
    <li> hive CLI로 스크립트 명령어 실행하기 (변수에 값을 넣어 전달하기)  </li>
    <pre> hive --hivevar &lt;key&gt;=&lt;value&gt; -f &lt;쿼리 스크립트&gt; <br> EX) hive --hivevar dt=20221201 -f &lt;select_idex_info.hql&gt; <br> (스크립트 내부) SELECT * FROM SOSS.DM_SAFE_IDEX_GRID WHERE PT_STDR_DE = ${dt} </pre>
  </dl><hr>

   <dl>
    <li> hive CLI로 스크립트 명령어 출력 내용(컬럼명 포함)을 CSV 파일로 추출하기  </li>
    <pre> hive --hiveconf hive.cli.print.header=True --hivevar &lt;key&gt;=&lt;value&gt; -f &lt;쿼리 스크립트&gt; | sed 's/[\t]/,/g' > .(현재경로)/&lt;파일명.csv&gt; <br> Ex) hive --hiveconf hive.cli.print.header=True --hivevar dt='20221201' -f select_idex_info.hql | sed 's/[\t]/,/g' > ./output.csv </pre>	

  </dl><hr>
