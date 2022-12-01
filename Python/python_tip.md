<header>
  <h2> Python Tip 정리 </h2>
</header>

<body>
  
  <dl>
    <li> Import 가능한 패키지 보기 </li>
<pre>
from pprint import pprint # 리스트 형식의 패키지와 버전을 이쁘게 보기 위해 사용
from pkg_resources import working_set # 파이썬의 내장 모듈. working_set의 reuturn은 <class 'pkg_resources.WorkingSet'>. 이를 리스트로 변환 필요

pprint(list(working_set))

* [패키지] [버전] [경로]
* numpy 1.21.6 (/home/user/b2en/.anaconda3/lib/python3.7/site-packages) 
* pip install [패키지를 하면] 기본적인 설치경로는 anaconda 디렉토리의 lib/python[version]/site-packages 이다.
* 나의 추가 Tip : 패키지를 수동으로 지워주려면 .anaconda/bin 의 패키지 binary 파일과 위 경로의 패키지를 지워주면 된다.
* 나의 추가 Tip2
: 패키지(pip, seaborn, pandas, airflow 등) 역시 파이썬으로 구동되는 파이썬 프로그램이므로 기본 실행 파이썬을 확인하려면
 (리눅스 환경에서) which python을 한다. 다만 .anaconda/bin 안에 셔뱅(#!)이 있는 파이썬 파일은 그 경로에 있는
 python binary 파일로 실행하므로 유의한다. (conda 가상환경을 만들고, 그 안에 있는 bin 파일들의 셔뱅을 확인하면 이해하기 쉽다)

</pre>
  </dl><hr>
  
  

</body>
