# 🧮 kotlin-calculator-precourse 🧮

> 입력한 문자열에서 숫자를 추출하여 더하는 계산기를 구현한다.
***

## ❗ 요구 사항

- **쉼표(,) 또는 콜론(:)** 을 구분자로 가지는 문자열을 전달하는 경우 **구분자를 기준으로 분리한 각 숫자의 합**을 반환한다.
    - 예: `"" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6`
- 앞의 기본 구분자(쉼표, 콜론) 외에 **커스텀 구분자**를 지정할 수 있다. 커스텀 구분자는 **문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자**를 커스텀 구분자로 사용한다.
    - 예: `"//;\n1;2;3"과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.`
- 사용자가 **잘못된 값을 입력**할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.

## ✅ 기능 명세

### 입력

- [X] 문자열을 입력받을 수 있다.
    - `camp.nextstep.edu.missionutils.Console`의 `readLine()` 사용

### 출력

- [X] 계산 안내 문구를 출력할 수 있다.
    - `덧셈할 문자열을 입력해 주세요.`
- [ ] 계산 결과를 출력할 수 있다.
    - `결과 : <결과값>`

### 계산

- [X] 쉼표(,) 또는 콜론(:)으로 기준으로 숫자를 구분해낼 수 있다.
- [X] 커스텀 구분자를 식별할 수 있다.
    - [ ] 커스텀 구분자를 기준으로 숫자를 구분해낼 수 있다.
- [X] 숫자를 더해 결과값을 구할 수 있다.

### 예외

- [ ] 사용자가 잘못된 값을 입력한 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션을 종료시킬 수 있다.
    - [ ] 구분자가 아닌 값을 담은 문자열이 입력될 경우 예외를 발생시킨다.
    - [ ] 커스텀 구분자 자리에 문자가 두 개 이상 입력될 경우 예외를 발생시킨다.
    - [ ] 커스텀 구분자 자리에 숫자가 입력될 경우 예외를 발생시킨다.
    - [ ] 커스컴 구분자 형식이 알맞지 않게 입력될 경우 예외를 발생시킨다.
    - [ ] 커스텀 구분자가 문자열 앞부분이 아닌 곳에 입력될 경우 예외를 발생시킨다.
- [ ] 빈 문자열이 입력됐을 경우 0을 결과값으로 반환한다.
    - [ ] 구분자만 있는 문자열이 입력됐을 경우 0을 결과값으로 반환한다.