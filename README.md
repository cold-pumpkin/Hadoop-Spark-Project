# Hadoop-Spark-Project
2018 빅데이터 분석 개발자 양성과정 - 4th 프로젝트 (Hadoop, Spark-sql)

>Linux x64, CentOS-7, JDK-1.8.0, Spark-2.3.0, Hadoop-3.1.0
      
  **1. 프로젝트 목표/개요**
- Kaggle의 "Death in the United State" Dataset을 선정하여 이를 통해 사망의 영향을 미치는 환경 요소들 분석

**2. 프로젝트 과정**
- 빅데이터 수집 단계에서는 Kaggle의 “Death in the United States” Dataset을 csv파일로 다운로드
- csv 파일을 리눅스 파일 시스템에서 하둡 파일 시스템으로 업로드
- 하둡 분산 파일 시스템을 통해 데이터를 여러 노드에 분산하여 병렬로 처리
- Spark-SQL을 이용해 데이터 집계와 해석 
  - 사회적으로 보호 받아야하는 영유아, 산모, 범죄로 인한 사망자를 백인과 흑인이라는 인종적 기준을 활용

**3. 프로젝트 구조**
  - Linux를 이용해 Virtual machine인 Master, Slave1, Slave2, Slave3를 만들고 각각 CentOS를 설치
  - Master에는 하드디스크 총 10대(OS설치용 2대, 하둡 파일시스템용 8대) 구성
  - Slave에는 하드디스크가 총 9대 (OS설치용 1대, 하둡 파일시스템용 8대) 구성
  - 하둡 클러스터 구축을 위해 JDK와 Hadoop을 설치
  - Master는 NameNode로 Slave는 DataNode로 설정
  - Slave3의 경우 파일시스템이미지 backup을 위해 추가적으로 Secondary NameNode로 설정
  
**4. 분석 결과 및 향후 분석 계획**
   - 영유아, 산모, 범죄로 인한 살해 사망의 경우 흑인의 사망 비율이 백인 보다 최소 2배에서 최대 7배까지 높은 것을 확인  
   -> 백인에 비해 흑인에 대한 사회적 차원의 보호가 부족
   - 미국의 구조적 차원에서 문제를 제기 할 수 있을 것이라고 생각
      1. 교육 기회의 불평등
      2. 경제 불균형
      3. 사회적 차별
      
      
