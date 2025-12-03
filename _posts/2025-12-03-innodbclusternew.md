layout : single
title : " InnoDB Cluster with MySQL 8.4 에 대한 포스팅입니다."



**InnoDB Cluster 구성도 **

![스크린샷 2025-12-03 오후 1.58.26](../images/2025-12-03-innodbclusternew/스크린샷 2025-12-03 오후 1.58.26.png)



MySQL 8.4 에서 변경된 부분은 크게 없지만 옵션 설정부분이 변경된 부분이 있습니다.  InnoDB Cluster는 MySQL Router, MySQL Shell, Gruop Replication 으로 구성되어 있습니다.

**MySQL Router**  

R/W 포트 (6446, 64460) 로 Primary 멤버에 대한 자동 라우팅

R/O 포트(6447, 64470) 로 Secondary 멤버에 대한 자동 라우팅

Auto Port: 6450 (8.2 + )



**MySQL Shell**

JavaScript, Python 및 SQL 지원

도큐먼트 스토아와 함께 관계형 모델 지원  (X 프로토콜 및 MySQL 프로토콜 지원)

**InnoDB Cluster 생성 및 관리 API 제공**

운영에 필요한 여러가지 유틸리티 제공( ex. Dump Loading Utility)

명령어, 배치 스크립트 지원



**MySQL Group Replication**

자동으로 서버 페일오버, 그룹 멤버쉽 관리, 데이터 복제 등을 담당하는 핵심 컴포넌트

InnoDB 스토리지 엔진과 통합되어  GTID 기반으로 복제 제공
