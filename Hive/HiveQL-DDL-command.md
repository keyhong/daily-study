<header>
  <h2> HiveQL DDL(Data Definition Language) 정리 </h2>
</header>

<body>
  <dl>
    <li> 테이블 생성 </li>
<pre>
CREATE EXTERNAL TABLE IF NOT EXISTS [테이블명] (        --(T)테스트
  ERR_DATE                   STRING               COMMENT   '일자' 
, ERR_TIME                   STRING               COMMENT   '시간' 
, DAG                        STRING               COMMENT   '대그' 
, TASK                       STRING               COMMENT   '태스크' 
, IDX                        BIGINT               COMMENT   '초 단위' 
, LOAD_AVERAGE_1MIN          DECIMAL(6, 2)        COMMENT   '시스템부하율 1분 평균' 
, ERR_TYPE                   STRING               COMMENT   '에러 종류' 
 )
COMMENT '테스트'
ROW FORMAT DELIMITED FIELDS TERMINATED BY '\u0002'
STORED AS ORC
LOCATION  '/mapr/mapr.daegu.go.kr/DW/mig.db' 
TBLPROPERTIES ('ORC.COMPRESS'='SNAPPY')
</pre>
  </dl>

  <dl>
    <li> 파티션 생성 </li>
<pre> ALTER TABLE [테이블명] ADD PARTITION(PT_STDR_YM = 202201) </pre>
  </dl>  
  
  <dl>
    <li> 테이블 삭제 </li>
    <pre> (1) ALTER TABLE [테이블명] SET TBLPROPERTIES('EXTERNAL' = 'FALSE'); </pre>
    <pre>
(2-1) 테이블 전체 삭제
DROP TABLE [테이블명]

(2-2) 파티션만 삭제
ALTER TABLE [테이블명] DROP IF EXISTS PARTITION ( [파티션 컬럼]=[조건] )
</pre>
  </dl>  
  
  <dl>
    <li> 파티션 생성 </li>
<pre> ALTER TABLE [테이블명] ADD PARTITION(PT_STDR_YM = 202201) </pre>
  </dl>    
  
  
  
  
  
  
</body>

-- 
(1) ALTER TABLE [테이블명] SET TBLPROPERTIES('EXTERNAL' = 'FALSE');
(2-1) 테이블 전체 삭제

(2-2) 파티션만 삭제
ALTER TABLE [테이블명] DROP IF EXISTS PARTITION(PT_STDR_DE= '')

-- 테이블 이름 변경
ALTER TABLE RENAME [BEFORE-테이블명] RENAME TO [NEW-테이블명];

-- 파일경로 위치 변경
ALTER TABLE [테이블명] SET LOCATION 'maprfs:/DM/soss.db/DW_PCEL_TMZN_SXDS_AGGR_TY_STT'

-- 프로퍼티 COMMENT 수정
ALTER TABLE [테이블명] SET TBLPROPERTIES ('COMMENT = "대구PCELL기준정보"')

-- 프로퍼티 LOCATION 수정
ALTER TABLE [테이블명]SET TBLPROPERTIES ('LOCATION = "MAPRFS:/DM/SOSS.DB/DG_PCEL_STDR_INFO"')



