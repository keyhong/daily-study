<header>
  <h2> HiveQL DDL(Data Definition Language) 정리 </h2>
</header>

<body>
  
  <dl>
    <li> 테이블 생성 </li>
<pre>
CREATE EXTERNAL TABLE IF NOT EXISTS [테이블명] (        --(T)<테이블명>
  ERR_DATE                   STRING               COMMENT   <'컬럼 COMMENT'> 
, IDX                        BIGINT               COMMENT   <'컬럼 COMMENT'>
, LOAD_AVERAGE_1MIN          DECIMAL(N1, N2)      COMMENT   <'컬럼 COMMENT'> 
 )
COMMENT <'테이블 COMMENT'>
ROW FORMAT DELIMITED FIELDS TERMINATED BY '\u0002'
STORED AS ORC
LOCATION  <'경로'> 
TBLPROPERTIES ('ORC.COMPRESS'='SNAPPY')
</pre>
  </dl><hr>
  
  <dl>
    <li> 파티션 생성 </li>
    <pre> ALTER TABLE <테이블명> ADD [IF NOT EXISTS] PARTITION (<'파티션 컬럼'> = <조건>) </pre>
  </dl><hr>
  
  <dl>
    <li> 테이블명 변경 </li>
<pre> ALTER TABLE RENAME <이전 테이블명> RENAME TO <새 테이블명>; </pre>
  </dl><hr> 
  
   <dl>
    <li> 파일경로 위치 변경 </li>
<pre> ALTER TABLE <테이블명> SET LOCATION <"경로"> </pre>
  </dl><hr>
  
   <dl>
    <li> 프로퍼티 COMMENT 수정 </li>
    <pre> ALTER TABLE <테이블명> SET TBLPROPERTIES ('COMMENT = <"NEW-COMMENT">') </pre>
  </dl><hr>
    
   <dl>
    <li> 프로퍼티 LOCATION 수정 </li>
    <pre> ALTER TABLE <테이블명> SET TBLPROPERTIES ('LOCATION = <"경로">') </pre>
  </dl><hr>

  
  <dl>
    <li> 삭제 프로퍼티 설정 </li>
    <pre> ALTER TABLE <테이블명> SET TBLPROPERTIES('EXTERNAL' = 'FALSE') </pre>
  </dl><br>
  <dl>
    <li> (1) 테이블 전체 데이터 삭제 </li>
    <pre> DROP TABLE <테이블명> </pre>
  </dl>
  <dl>
    <li> (2) 파티션 데이터만 삭제 (파티션 조건은 부등호도 가능) </li>
    <pre> ALTER TABLE <테이블명> DROP [IF EXISTS] PARTITION (<'파티션 컬럼'> = <조건>) </pre>
  </dl><hr>  
</body>
