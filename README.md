# JavaMethodStudy

2023-05-25

자바를 스프링 쓸 때 말고 안쓰니까

뇌가 텅 비었다... 코더가 될 뻔했다...

내가 멍청한 만큼 많이 써보고 잘 외워보자...

# 1일차 - 문자열

### 파이썬은 선녀였다..

#### String

- Java나 Python이나 String은 불변이다. (이건 암호화 과제할 때 데여서 너무 잘 알음)
- String pool을 통해 String을 관리함으로써 Java는 Runtime에서 Heap 영역의 많은 메모리를 절약할 수 있다.
- String이 불변이 아니라면 보안상의 문제를 야기한다.
- String이 불변이기 때문에 멀티 쓰레딩 환경에서 안전(thread-safe)하다.
- Java는 String의 hashcode를 생성 단계에서부터 캐싱한다. (이건 진짜 모르겠음)

#### StringBuilder

- 이걸 모르고 있었다니 죽는게 맞다.

#### StringTokenizer 

- readline()을 입력받은 값을 공백 단위로 구분해, nextToken()을 통해 순서대로 호출할 수 있다.
- 아니 왜 split() 안쓰지? StringTokenizer가 속도가 더 빠르다...

#### Buffer 

- 예외처리를 생활화하자

#### 
