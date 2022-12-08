   <dl>
    <li> 일급함수(first-class function) </li>
<pre>
프로그래밍 언어가 함수를 1급 객체(first-class citizen)으로 취급하는 것.
적용이 되는 언어는 Python 이외에도 JavaScript 또한 일급함수가 있다.
</pre>
  </dl><hr>
 
   <dl>
    <li> 응용  </li>
<pre> 
1. 함수 자체를 다른 함수의 인자로 전달하는 것
2. 다른 함수의 리턴 값으로 리턴
3. Runtime에 생성 가능
4. 데이터의 변수나 구조체에 할당 가능하다
</pre>
  </dl><hr>
 
   <dl>
<li> 코드 활용하기 </li>
 
from typing import Callalbe <br>
  
&#35; 인자로 넣을 함수
def get_query() -> str: <br>
&nbsp;&nbsp;&nbsp;&nbsp;return 'SELECT * FROM SOSS.DM_SAFE_IDEX GRID WHERE PT_STDR_DE = "20221208"'
  
&#35; 인자를 받은 함수  
def print_query(query_function: Callabe[[None], str]): <br>
&nbsp;&nbsp;&nbsp;&nbsp;print(query_function())
 
print_query(get_query)
  
&#35; 출력값 <br>
SELECT * FROM SOSS.DM_SAFE_IDEX GRID WHERE PT_STDR_DE = "20221208"
