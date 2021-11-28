### `자바 프로그래밍 Next Step` 학습을 위한 Repository 입니다 😊
- 책을 읽으면서 2장부터 하나하나 정리해보려고 합니다.
- `2021.11.28 (일요일)` 시작
---
### `JUnit` 라이브러리 적용하기
<img width="1440" alt="스크린샷 2021-11-28 오후 9 31 12" src="https://user-images.githubusercontent.com/79444040/143767957-2161723a-04df-4006-bac9-9e147b1ae937.png">
<img width="1440" alt="스크린샷 2021-11-28 오후 9 32 05" src="https://user-images.githubusercontent.com/79444040/143767988-679fec4f-9dbd-413d-8c7b-47ffbc003f81.png">

1. 최상단 폴더에서 새로운 디렉토리를 생성하고, 생성된 폴더를 test 디렉토리로 설정한다.
2. 테스트 하고 싶은 클래스에서 (맥 기준) Command + Shift + T 단축키를 이용해서 JUnit 라이브러리를 선택하면 끝 !


#### `JUnit`을 활용해 코드 테스트하기
- main() 메소드를 활용한 테스트에서는 테스트 시 콘솔 값을 수동으로 확인하고 하나의 메서드 테스트에만 집중하지 못하는 등 여러 문제점들이 많다.
- JUnit을 활용하면 main() 메소드를 활용한 테스트의 문제점을 해결할 수 있다.

```java
결과 값을 눈으로 확인할 수 있는 예제 코드

import org.junit.Test;

public class CalculatorTest {
  @Test
  public void add() {
    Calculator cal = new Calculator();
    System.out.println(cal.add(6, 3));
  }
  
  @Test
  public void subtract() {
    Calculator cal = new Calculator();
    System.out.println(cal.subtract(6, 3));
  }
}  

출력 결과
9
3

테스트 메소드 작성 시 JUnit5 부터는 접근제어자를 붙이지 않고도 작성할 수 있다.
하지만 일단 책의 예제대로 따라가보려고 한다.
```

```java
결과 값을 눈으로 확인하는 것이 아닌 프로그램을 통해 자동화하는 예제 코드

import static org.junit.Assert.assertEquals;

import org.junit.Test;

public class CalculatorTest {
  @Test
  public void add() {
    Calculator cal = new Calculator();
    assertEquals(9m cal.add(6, 3));
  }
  
  @Test
  public void subtract() {
    Calculator cal = new Calculator();
    assertEquals(9m cal.subtract(6, 3));
  }
}

출력결과는 보이지 않지만 인텔리제이 기준 초록불이 뜨면 성공이다.

```
