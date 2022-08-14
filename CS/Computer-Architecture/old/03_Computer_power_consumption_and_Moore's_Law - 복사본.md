# 컴퓨터 전력 소비와 무어의 법칙

**Power = Capacitive load * Voltage ^ 2 * Frequency**



## 무어의 법칙 (Moore's Law)

- 반도체에 집적하는 트랜지스터 수는 2년마다 2배로 증가한다는 법칙
- 자연 법칙이 아닌 경험 법칙

#### 한계

- 과거에는 집적도가 오를수록 원가 절감도 이루어졌으나, 이제는 원가 절감이 불가능한 영역

- 단일 연산 유닛의 동작 속도를 높여 연산 속도를 높이는 방식은 끝났음

  => 멀티코어 프로세서의 도입



## 멀티코어 프로세서 (Multicore processors)

- 칩에 하나보다 많은 수의 프로세서를 할당
- Explicitly parallel programming을 요함
  - Instruction Level Parallelism과 비교됨
    - 하드웨어가 한번에 다중의 명령어 수행
  - 어려운 점
    - 부하 분배 (Load balancing)
    - Programming for performance
    - Optimizing communication and syhnchronization



## SPEC CPU benchmark

- **Standard Performance Evaluation Corportaion**

- 컴퓨터를 위한 표준화된 성능 벤치마크를 생산, 수립, 유지, 보증하기 위한 미국의 비영리 단체

### SPEC2006

- 각 항목의 처리 속도를 측정하고 기하평균을 내 전체 점수를 도출

- 정수 연산을 평가하는 SPECint2006
  - 인터프리터, 압축, 컴파일러, 조합 최적화 문제, 인공지능 바둑/체스, 양자 물리 컴퓨팅, 영상 처리, 이산 사건 시뮬레이션, 경로 최적화 알고리즘, XML 처리 등 12가지 항목
- 부동소수점 연산을 평가하는 SPECfp2006
  - 유체역학, 양자화학, 양자색역학, 전산유체역학, 레이 트레이싱, 음성 인식, 유한요소해석, 분자역학 등 17가지 항목