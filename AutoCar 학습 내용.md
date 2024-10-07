* Pilot 메서드

Car = Pilot.AutoCar()
: Car 객체 생성

Car.setSpeed(50)
: 속도 설정

Car.steering 
: 조향 (범위 : -1 ~ 1)

Car.forward()
: 전진

Car.backward()
: 후진

=================

Car.camPan(n)
: 카메라 좌우 조정 (범위 : 0 ~ 180)

Car.camTilt(n)
: 카메라 상하 조정 (범위 : -30 ~ 200)

Car.joystick()
: 조이스틱

=================

Car.getGyro(axis)
: 자이로

Car.getAccel(axis)
: 가속도 측정

=================

LiDAR 기본

connect()
: LiDAR 연결

startMotor()
: LiDAR 스캐닝 모터 시작

stopMotor()
: LiDAR 스캐닝 모터 정지

getVectors()
: 1회전 스캔 벡터값 
* 벡터값 타입 = 튜플Degree, Distance, Quality

getXY()
: 1회전 스캔한 좌표값을 리턴

getMap(size, limit_distanc)
: 1회전 스캔값을 2차원 맵으로 반환
* size : 맵사이즈 (default : 300, 300)
limit_distanc : 맵 표현 최대 거대 (default : 12000)

* 머신러닝 & 딥러닝

< 학습 >

1. 지도 학습 : 문제와 정답을 알려주고 학습 (예측, 분류)

2. 비지도 학습 : 정답 미제공 학습 (군집, 규칙)

3. 강화 학습 : 오류를 줄일 수록 보상을 증가

< 데이터 set >

1. 학습 데이터 : 학습에 사용되는 데이터

2. 검증 데이터 : 학습 시 성능평가에 사용되는 데이터

3. 시험 데이터 : 학습 후 평가나 테스트로 예측의 최종에 평가되는 데이터

< 회귀 >

1. Regression(회귀) : 상관관계(독립변수 & 종속변수)

y = Wx + b (y : 종속변수, W : 회귀계수(기울기, 가중치), x : 독립변수, b : 절편)

비용 함수 = 손실함수 : cost(w) = (H(x) - y)
정답 y와 H(x)(예측값) = Wx + b의 차리를 비용이라고 함
비용 = 정답 - 예측값
