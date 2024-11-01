# java-lotto-precourse

### 사용자로부터 로또 구입 금액을 입력 받는다.
- 로또 1장의 가격은 1,000원이다.
- 입력은 1,000원 단위로 받는다.
- [예외]
    - 금액이 1,000원으로 나누어 떨어지지 않는 경우
    - 금액이 정수가 아닌 경우
    - 금액이 음수인 경우
    - 금액이 0인 경우
    - 금액이 비어있는 경우

### 사용자로부터 당첨 번호를 입력 받는다.
- 입력 받은 번호는 쉼표(,)를 기준으로 구분한다.
- 당첨 번호는 6개를 받도록 한다.
- 당첨 번호는 중복될 수 없다.
- 당첨 번호는 정수로만 입력이 가능하다.
- 당첨 번호는 1 ~ 45의 범위를 가진다.
- [예외]
    - 당첨 번호의 구분자를 잘못 입력한 경우
    - 당첨 번호가 6개가 아닌 경우
    - 중복된 당첨 번호를 입력 받은 경우
    - 당첨 번호가 정수가 아닌 경우
    - 당첨 번호가 1 ~ 45의 범위를 벗어난 경우
    - 당첨 번호가 비어있는 경우

### 사용자로부터 보너스 번호를 입력 받는다.
- 보너스 번호는 1개를 받도록 한다.
- 보너스 번호는 당첨 번호와 중복될 수 없다.
- 보너스 번호는 정수로만 입력이 가능하다.
- 보너스 번호는 1 ~ 45의 범위를 가진다.
- [예외]
  - 1개의 번호 외에 다른 문자가 입력된 경우
  - 보너스 번호가 당첨 번호와 중복된 경우
  - 보너스 번호가 정수가 아닌 경우
  - 보너스 번호가 1 ~ 45의 범위를 벗어난 경우
  - 보너스 번호가 비어있는 경우

### 로또 발매기를 구현한다. 
- 사용자로부터 입력 받은 금액만큼 로또를 생성한다.
- 생성된 로또의 번호를 모두 출력한다. (ex. [8, 21, 23, 41, 42, 43])
    - 생성된 로또의 당첨 번호는 오름차순으로 정렬한다.
- 사용자로부터 당첨 번호와 보너스 번호를 입력받는다.
    - 입력된 각 임의의 수는 중복되지 않도록 한다.
    - 입력 받은 번호는 오름차순으로 정렬하여 저장한다.
- 당첨 기준에 따른 당첨 금액을 정의한다.
    - 1등: 6개 번호 일치 / 2,000,000,000원
    - 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
    - 3등: 5개 번호 일치 / 1,500,000원
    - 4등: 4개 번호 일치 / 50,000원
    - 5등: 3개 번호 일치 / 5,000원 
- 당첨 통계를 출력하도록 한다.
    - 일치하는 번호의 개수를 출력한다.
    - 2등 당첨의 경우 보너스 번호 일치 여부도 함께 출력한다.
    - 당첨 기준에 따른 당첨 금액을 출력한다.
    - 당첨 개수를 출력한다.
- 총 수익률을 출력하도록 한다. 
    - 수익률은 소수점 둘째 자리에서 반올림한다. (ex. 100.0%, 51.5%, 1,000,000.0%)
- 예외 상황 시 에러 문구를 출력한다.
    - 에러 문구는 "[ERROR]"로 시작해야 한다. (ex. [ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.)
- [예외]
    - 사용자로부터 잘못된 입력을 받은 경우 (해당 부분부터 다시 입력 받는다.)

### 각 입력 검증 및 예외 처리를 구현한다. (예외 발생 시 IllegalArgumentException 발생시킨 후 해당 부분부터 재입력)
- Exception이 아닌 IllegalArgumentException, IllegalStateException 등과 같은 명확한 유형을 처리한다.

### 기능 및 예외 처리 확인을 위한 테스트 케이스를 작성한다.