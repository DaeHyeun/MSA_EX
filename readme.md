MSA 예제개발

1. front_Server에서 더하기,빼기 요청
2. 요청받은 gateway_Server는 산술식을 구분하여 해당 gRPC서버에 요청
3. 요청받은 grpc서비스는 계산을 하여 MQ에서 전달 
4. 전달받은 MQ는 약수구하기 Grpc서비스에 전송
5. 약수를 구하고 다시 gataway_Server로 전송
6. 최종 클라이언트는 gateway에게 받은 정보를 화면에 출력

MSA Sample 서비스 아키텍처 구성   
 - 두 가지 서비스 (합산, 차감) - gRPC  
 - API Gateway - REST Controller(java)  
 - Client 서비스 요청 - Webpage(HTML/CSS/JavaScript)  
 - Promise,stub이용 
