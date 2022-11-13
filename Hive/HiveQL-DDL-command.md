<header>
  <h2> HiveQL DDL(Data Definition Language) 정리 </h2>
</header>

<body>
  
  <dl>
    <li> 테이블 생성 </li>
<pre>
CREATE EXTERNAL TABLE IF NOT EXISTS [테이블명] (        --(T)테스트
  ERR_DATE                   STRING               COMMENT   ['컬럼 COMMENT'] 
, IDX                        BIGINT               COMMENT   ['컬럼 COMMENT']
, LOAD_AVERAGE_1MIN          DECIMAL(N1, N2)      COMMENT   ['컬럼 COMMENT'] 
 )
COMMENT ['테이블 COMMENT']
ROW FORMAT DELIMITED FIELDS TERMINATED BY '\u0002'
STORED AS ORC
LOCATION  ['경로'] 
TBLPROPERTIES ('ORC.COMPRESS'='SNAPPY')
</pre>
  </dl>

  <dl>
    <li> 파티션 생성 </li>
<pre> ALTER TABLE [테이블명] ADD IF NOT EXISTS PARTITION  (['파티션 컬럼'] = [조건]) </pre>
  </dl>  
  
  <dl>
    <li> 테이블 삭제 </li>
    <pre> (1) ALTER TABLE [테이블명] SET TBLPROPERTIES('EXTERNAL' = 'FALSE') </pre>
    <pre>
(2-1) 테이블 전체 삭제
DROP TABLE [테이블명]

(2-2) 파티션만 삭제
ALTER TABLE [테이블명] DROP IF EXISTS PARTITION (['파티션 컬럼'] = [조건])
</pre>
  </dl>  
  
  <dl>
    <li> 테이블명 변경 </li>
<pre> ALTER TABLE RENAME [BEFORE-테이블명] RENAME TO [NEW-테이블명]; </pre>
  </dl>    
  
   <dl>
    <li> 파일경로 위치 변경 </li>
<pre> ALTER TABLE [테이블명] SET LOCATION ['경로'] </pre>
  </dl>    
  
   <dl>
    <li> 프로퍼티 COMMENT 수정 </li>
<pre> ALTER TABLE [테이블명] SET TBLPROPERTIES ('COMMENT = ["NEW-COMMENT"]') </pre>
  </dl>    
    
   <dl>
    <li> 프로퍼티 LOCATION 수정 </li>
<pre> ALTER TABLE [테이블명] SET TBLPROPERTIES ('LOCATION = ["경로"]') </pre>
  </dl>    
    
</body>




