## 시나리오

1. 기본 진행
   1. 컴퓨터가 1에서 9까지 서로 다른 임의의 수 3개를 선택
   2. 사용자는 서로 다른 3개의 숫자 입력
   3. 컴퓨터는 입력받은 결과에 따라 힌트(2)를 제공
   4. 컴퓨터의 숫자를 모두 맞히면 게임 종료  
      4-1. 맞히지 못할 시 계속 반복
   5. 게임이 종료된 후 다시 시작하거나 완전히 종료할 수 있다.
2. 힌트 제공  
   기본적으로 아래 규칙을 따른다. 사용자에게 정답에 근접한 힌트를 제공하는 방식
   1. 같은 수가 같은 자리에 있으면 스트라이크
   2. 다른 자리에 있으면 볼
   3. 같은 수가 전혀 없으면 낫싱
3. 예외 처리
   1. 잘못된 값을 입력한 경우 `throw`문을 사용해 예외를 발생시킨 후 프로그램 종료

## 기능 목록

1. 컴퓨터(상대)
   1. 서로 다른 임의의 수 3개 선택
   2. 유저 입력에 따라 힌트 제공
   3. 게임 종료시
      1. 반복
      2. 종료
2. 유저
   1. 입력 화면 출력 시 값 입력
   2. 게임 종료시
      1. 반복 혹은 종료 선택
3. 게임 공통
   1. 첫 실행 시 인사 문구
   2. 게임 종료 전까지 무한 반복
   3. 예외 상황 처리

## 테스트 목록

1. 기능 목록 항목별 테스트 코드 작성
2. 예외 목록에 기반한 테스트 코드 작성

## 예외 목록

1. 사용자가 잘못된 값을 입력한 경우
   1. 입력한 값이 숫자가 아닌 경우
   2. 0개의 숫자를 입력하거나 3개 초과의 숫자를 입력한 경우
   3. 서로 다른 3개의 숫자가 아닌 경우

## 프로그래밍 작성 요구사항

1. indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
   예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
   힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메소드)를 분리하면 된다.
2. 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라.
3. Jest를 이용하여 본인이 정리한 기능 목록이 정상 동작함을 테스트 코드로 확인한다.
   테스트 도구 사용법이 익숙하지 않다면 **tests**/StringTest.js를 참고하여 학습한 후 테스트를 구현한다.
4. 라이브러리
   MissionUtils 라이브러리에서 제공하는 Random 및 Console API를 사용하여 구현해야 한다.
   Random 값 추출은 MissionUtils 라이브러리의 Random.pickNumberInRange()를 활용한다.  
   사용자의 값을 입력 받고 출력하기 위해서는 MissionUtils 라이브러리에서 제공하는 Console.readLine, Console.print를 활용한다.
