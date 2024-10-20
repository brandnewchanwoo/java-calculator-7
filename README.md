# java-calculator-precourse

우아한테크코스 웹 백엔드 7기 1주 차 프리코스 과제입니다.

---

# 문자열 덧셈 계산기

입력한 문자열에서 숫자를 추출하여 더하는 계산기입니다.

## 기능 목록

- 문자열 덧셈 계산
  - 쉼표(`,`) 또는 콜론(`:`)을 구분자로 가지는 문자열이 전달될 경우 구분자를 기준으로 분리한 각 수의 합이 반환됩니다.
  - 예: `""` => 0, `"1,2"` => 3, `"1,2,3"` => 6, `"1,2:3"` => 6
- 커스텀 구분자 지정
  - 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있습니다. 문자열 앞부분의 `"//"`와 `"\n"` 사이에 위치하는 문자를 커스텀 구분자로 사용합니다.
  - 예: `"//;\n1;2;3"`이 입력될 경우 커스텀 구분자는 세미콜론(`;`)이며, 결과 값은 6이 반환되어야 합니다.
- 잘못된 문자열 예외 처리
  - 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션이 종료됩니다.

> [!NOTE]
> 양수만 추출됩니다. 따라서 다음과 같은 문자열은 잘못된 값입니다.
> 
> `"-1,2,3"`