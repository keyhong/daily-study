<header>
  <h2> Git 커맨드 정리 </h2>
</header>

<body>
 
  <dl>
    <li> 원격저장소 가져오기 (From GitHub)  </li>
    <pre> git clone <원격저장소 URL> [원격저장소 파일을 넣으려고 만드는 폴더] </pre>
  </dl><hr>  

  <dl>
    <li> 로컬저장소 생성하기  </li>
    <pre> git init </pre>
  </dl><hr>  

  <dl>
    <li> 로컬저장소에 파일 추가하기  </li>
    <pre> git add <추가할 파일 또는 . ( "." : 현재 디렉토리 하위 내 모든 파일)> </pre>
  </dl><hr> 
    
  <dl>
    <li> 로컬저장소 히스토리 내역 추가하기  </li>
    <pre> git commit -m <"메세지"> </pre>
  </dl><hr>     
    
  <dl>
    <li> 작업 디렉토리(Working Directoy)와 스테이징 영역(Staging Area) 확인  </li>
    <pre> git status </pre>
  </dl><hr> 

  <dl>
    <li> 원격저장소 추가 </li>
    <pre> git remote add <저장소 별칭> <원격저장소 URL> </pre>
  </dl><hr>
  
  <dl>
    <li> 원격저장소 확인 </li>
    <pre>  git remote -v </pre>
  </dl><hr>     
  
  <dl>
    <li> 원격저장소 삭제 </li>
    <pre> git remote rm <저장소 별칭> </pre>
  </dl><hr> 
  
</body>
