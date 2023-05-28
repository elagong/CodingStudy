## https://github.com/elagong/AlgorithmStudy

# JavaMethodStudy

2023-05-25

자바를 스프링 쓸 때 말고 안쓰니까

뇌가 텅 비었다... 코더가 될 뻔했다...

내가 멍청한 만큼 많이 써보고 잘 외워보자...

# 1일차 - 문자열

#### 파이썬은 선녀였다..

##### String

- Java나 Python이나 String은 불변이다. (이건 암호화 과제할 때 데여서 너무 잘 알음)
- String pool을 통해 String을 관리함으로써 Java는 Runtime에서 Heap 영역의 많은 메모리를 절약할 수 있다.
- String이 불변이 아니라면 보안상의 문제를 야기한다.
- String이 불변이기 때문에 멀티 쓰레딩 환경에서 안전(thread-safe)하다.
- Java는 String의 hashcode를 생성 단계에서부터 캐싱한다. (이건 진짜 모르겠음)

##### StringBuilder

- 이걸 모르고 있었다니 죽는게 맞다.

##### StringTokenizer 

- readline()을 입력받은 값을 공백 단위로 구분해, nextToken()을 통해 순서대로 호출할 수 있다.
- 아니 왜 split() 안쓰지? StringTokenizer가 속도가 더 빠르다...
- 공백이면 StringTokenizer, 정규식 처리가 필요하면 split() 쓰자.

##### Buffer 

- 예외처리를 생활화하자

# 2일차 - 백준 문제풀기

#### 파이썬은 신이다.

##### https://www.acmicpc.net/step/1

- 단계별 문제 1회차 (1번~15번)
- BufferedReader / BufferedWriter 잘 쓰기 -> parseInt / String.valueOf.()
- 5번 문제 나눗셈) 연산을 할 때, double형은 double형으로 나눠주자. 기본적인 걸 까먹네..
- 갑자기 입출력이 너무 궁금해서 출력 시의 내부로직을 까봤다. 콘솔에 있는 숫자는 과연 int 형일까? 라는 의문과 함께..
  - System 클래스 내의 static 필드 중 out 은 PrintStream 타입의 변수로 선언되어 있다.
  - ```java 
    public static final PrintStream out = null; 
  - 위 처럼 null로 초기화 되어있지만, System.out은 PrintStream의 객체로 설정된다.
  - PrintStream 객체에는 println() 같은 출력 메서드가 구현되어있다.
  - ```java 
    public void print(boolean b) {
        write(String.valueOf(b));
    }
  - 위 처럼 int, long, boolean, float와 같은 모든 type은 최종적으로 String으로 변환된다.
  - 결론 : 콘솔에 있는 모든 출력문은 String이다.
