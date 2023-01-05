# kafka 3.3.1 version 기준   
   <dl>
    <li> 토픽 리스트 조회 </li>
<pre>
./kafka_2.13-3.3.1/bin/kafka-topics.sh --list --bootstrap-server [IP]:[PORT]
</pre>
  </dl><hr>

   <dl>
    <li> 토픽 삭제 </li>
<pre>
1. ./kafka_2.13-3.3.1/config/server.properties 파일에 "delete.topic.enable=true" 추가
2. ./kafka_2.13-3.3.1/bin/kafka-topics.sh --delete --bootstrap-server [IP]:[PORT] --topic [TOPIC_NAME]
</pre>
  </dl><hr>
