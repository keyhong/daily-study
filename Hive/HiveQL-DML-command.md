   <dl>
    <li> 파티션 정보 보기 </li>
    <pre> SHOW PARTITIONS [테이블명] </pre>
  </dl><hr>
  
   <dl>
    <li> 테이블 통계 정보 </li>
    <pre> ANALYZE TABLE [테이블명] PARTITION ([파티션] = [조건]) COMPUTE STATISTICS </pre>
  </dl><hr>

   <dl>
    <li> 파티션별 테이블 총 개수 보기 </li>
    <pre> SELECT [파티션명], COUNT(*) FROM [테이블명] GROUPBY [파티션명] ORDER BY 1 </pre>
  </dl><hr>

-- 

