# Essence-Of-Java-
## 객체 지향 언어 = 프로그래밍 언어 + 객체 지향 개념(규칙)

### 객체 지향 개념(규칙) - > 규칙이니까 외울 수 밖에 없다.
자바의 정석 6장+7장(다형성)까지 반복 학습한다.

---

## **클래스의 정의
   -** 클래스란 객체를 정의해 놓은 것

## 클래스의 용도
   - 클래스는 객체를 생성하는데 사용

---

## 객체의 정의
   - 실제로 존재하는 것. 사물 또는 개념

## 객체의 정의
   - 객체가 가지고 있는 기능과 속성에 따라 다름

---

## 클래스는 객체를 만들기 위한 설계도

### 예) 제품 설계도 (클래스)     제품      (객체)
     붕어빵 가게 (클래스)     붕어빵   (객체)

---

# 객체의 구성요소 - 속성과 기능

## 객체 = 속성(변수) + 기능(매서드)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/03f2934d-350f-409e-828a-b2c1f2f78f86/Untitled.png)

---

# 객체와 인스턴스

## 객체 : 모든 인스턴스를 대표하는 일반적 용어
인스턴스 : 특정 클래스로부터 생성된 객체(예 : Tv인스턴스)

**사실상 같은 말이라고 봐도 무방하다** 

## 인스턴스화(제품생성)
클래스(설계도) ——————————> 인스턴스(객체)(제품)

### 클래스를 작성했으면 따로 객체(제품)을 만들어야 우리가 사용할 수 있다.

---

# 정리

## Q. 클래스가 왜 필요한가?
A. 객체를 생성하기 위해

---

## Q. 객체가 왜 필요한가?
A. 객체를 사용하기 위해

---

## Q. 객체를 사용한다는 것은?
A. 객체가 가진 속성(변수)과 기능(매서드)을 사용하려고

## 하나의 소스 파일에 여러 클래스 작성

---

## 올바른 작성 예

---

### Hello2.java (소스파일)

public class Hello2 {}
            class Hello3 {}

public class가 있는 경우, 소스파일의 이름은 반드시 public class의 이름과 일치해야한다.

---

### Hello2.java (소스파일)

class Hello2 {}
class Hello3 {}

public class가 하나도 없는 경우
소스파일의 이름은 “Hello2.java”, “Hello3.java” 둘 다 가능하다.

---

## 잘못된 작성 예

---

### Hello2.java (소스파일)

public class Hello2 {}
~~public~~ class Hello3 {}

하나의 소스파일에 둘 이상의 public class가 존재하면 안된다.
각 클래스를 별도의 소스파일에 나눠서 저장 하거나
둘 중의 한 클래스에 public을 붙이지 않아야 한다.

---

### Hello3.java (소스파일)

public class Hello2 {}
            class Hello3 {}

소스파일의 이름이 public class의 이름과 일치하지 않는다.
소스파일의 이름을 “Hello2.java”로 변경해야 맞다.

---

### hello2.java (소스파일)

public class Hello2 {}
            class Hello3 {}

소스파일의 이름이 public class의 이름과 일치하지 않는다.
대소문자를 구분하므로 대소문자까지 일치해야한다.

---

# 정리

## Q. 하나의 소스파일에 여러개의 클래스를 생성하기 위한 규칙은?
A. 소스파일의 이름과 public class의 이름이 같아야한다.
     하나의 소스파일에 둘 이상의 public class가 존재하면 안된다.

![스크린샷 2022-12-20 오후 7.46.56.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4fbf891a-9d5e-4e6e-8945-e9a654769f82/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-12-20_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.46.56.png)

### 자바는 대소문자를 구분하기때문에 소스파일의 이름과 클래스의 이름이
대소문자까지 완벽하게 같도록 해야한다.

## 객체의 생성과 사용

---

## 1. 객체의 생성

### 클래스명 변수명;

클래스의 객체를 참조하기 위한 참조변수를 선언

### 변수명 = new 클래스명( );

클래스의 객체를 생성 후, 객체의 주소를 참조변수에 저장

### Tv t; (리모콘)

Tv클래스 타입의 참조변수 t를 선언

### t = new Tv ( );

Tv인스턴스를 생성한 후, 생성된 Tv인스턴스의 주소를 t에 저장

---

### 객체를 다루려면 참조변수(리모콘)이 필요하고
=(대입연산자)를 이용해 객체(Tv인스턴스)와 참조변수(리모콘)을 연결해 주어야한다.

---

## 2. 객체의 사용

### t.channel = 7;

t라는 참조변수에 연결되어있는 객체의 channel을 7로 지정해준다 *여기서는 Tv객체

### t.channelDown( );

t라는 참조변수에 연결되어있는 객체의 channelDown이라는 매서드를 사용하는 것(매서드 호출)

---

# 객체 생성,사용의 순서

## 1. 클래스 작성

```java
class Tvclass {
    String color;
    boolean power;
    int channel;

    void power() {power = !power;}
    void channelUp() {++channel;}
    void channelDown() {--channel;}
}
```

## 2. 객체 생성

```java
public class Tv {
    public static void main(String arg[]) {
        Tvclass t = new Tvclass();
}
```

## 3. 객체 사용

```java
public class Tv {
    public static void main(String arg[]) {
        Tvclass t = new Tvclass();
        t.channel = 7;
        t.channelDown();
        System.out.println("현재 채널은" + t.channel + "입니다");
    }
}
```

# 객체 배열

---

### 객체  배열 == 참조변수 배열

```jsx
Tv[] tvarr = new Tv[3];
```

길이가 3인 Tv타입의 참조변수 배열을 생성해준다.
위 문장을 그림으로 그리면 아래와 같다.

![스크린샷 2022-12-21 오후 3.42.12.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c9bd09de-d8d9-4dc4-a304-0d83813ad815/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-12-21_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3.42.12.png)

### 배열 생성시 초기값은 null이기 때문에 아무것도 들어있지않다

---

![스크린샷 2022-12-22 오전 9.33.32.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61f17d28-db17-49b6-a491-8576a757ea93/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-12-22_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_9.33.32.png)

### 위 문장을 간단히 바꾸면

```java
Tv[] tvArr = { new Tv(), new Tv(), new Tv() };
```

### 객체를 생성하여 각 참조변수에 저장해준다
(참조변수 배열이지만 객체가 저장된 샘)

---

# 정리

## 객체 배열 == 참조변수 배열

## 배열 생성시 초기값은 null이니까
tvArr[0] = new tv(); 이런식으로 배열에 객체를 직접 넣어줘야한다.

# 클래스의 정의

---

## 클래스 == 설계도
클래스 == 데이터(변수) + 함수(매서드)
클래스 == 사용자정의 타입

---

### 1. 변수       하나의 데이터를 저장할 수 있는 공간
2. 배열      같은 종류의 여러 데이터를 하나로 저장할 수 있는 공간
3. 구조체  서로 관련된 여러 데이터(타입 관계X)를 하나로 저장할 수 있는 공간
4. 클래스  데이터와 함수의 결합 (구조체 + 함수(매서드))

---

### 클래스 (구조체 + 함수)

타입관계없이 서로 관련된 데이터를 하나로 저장할 수 있는 구조체
이러한 데이터와 관련된 함수를 하나로 저장할 수 있는 클래스

---

### 사용자 정의 타입(클래스)

원하는 타입을 직접 만들 수 있다

서로 관련된 데이터를 하나로 묶어서 객체지향적인 코드로 만들 수 있음

예를들어 시간을 관리하는 변수를 만들고싶은데 없으니까 클래스로 만들어준다.

```java
class Time {
    int hour;
    int minute;
    int second;
}
```

```java
Time t = new Time();

        t.hour = 12;
        t.minute = 34;
        t.second = 56;
        
        System.out.println("현재 시각은" + t.hour + "시" +
													t.minute + "분" + t.second + "초 입니다");
결과 : 현재 시각은12시34분56초 입니다
```



# 선언위치에 따른 변수의 종류

---

## 클래스는 크게 두개의 영역으로 나뉘어진다

## 1. 클래스영역

클래스영역에서는 선언문만 사용 가능하다.
1. 인스턴스변수(instance variable) (インスタンスヴァリアブル)
생성시기 : 클래스가 메모리에 올라갈 때

```java
int iv;
```

2. 클래스변수(class variable) (クラスヴァリアブル) - static변수, 공유변수
static + instance variable = class variable
생성시기 : 인스턴스가 생성되었을 때

```java
static int cv;
```

---

## 2. 메서드 영역

```java
// 선언 + 메서드 시작~끝 = 메서드 정의
void method() // 메서드 선언
    { // 메서드 시작
        int lv = 0; // local variable
    } // 메서드 끝
```

지역변수(local variable) (ローカルヴァリアブル) == 매개변수
생성시기 : 변수 선언문이 수행되었을 때

---

## 이렇게 생각하면 편하다!!
객체 = 인스턴스변수(instance variable)를 묶은 것

# 클래스 변수와 인스턴스 변수

클래스 변수와 인스턴스 변수의 차이점은 무엇일까?
아래의 예와 같이 알아보자

---

![스크린샷 2022-12-22 오후 7.14.28.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2d6331c-c0bb-4e6a-ae24-3842a8ebb52c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-12-22_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.14.28.png)

위와같이 한장의 카드라는 객체가 있다고 생각하면 카드의 속성 즉 변수는 무엇이 있을까?

카드의 숫자, 카드의 무늬, 카드의 폭, 카드의 높이 등등..있을것이다.

```java
class Card {
    String kind; // 무늬
    int number; // 숫자

    static int width = 100; // 폭
    static int height = 250; // 높이
}
```

저번장에서 이야기했듯이 객체는 instance variable(인스턴스 변수)들로 묶여져있다.

---

**인스턴스 변수**는 개별적인 속성을 가진다 카드에서 무늬, 숫자는 카드마다 다르다
즉 개별적인 값을 가져야하는 속성은 **인스턴스 변수**가된다.

---

**클래스 변수**는 공통 속성을 가진다 카드에서 카드의 폭, 높이는 모두 같다
즉 모든 인스턴스가 공통으로 갖는 속성에는 static이 붙어 **클래스 변수**가된다.

---

변수에 접근하기

```java
class Main {
    public static void main(String[] args) {

        Card c = new Card();

        c.kind = "HEART";
        c.number = 5;

        ~~c.width = 200;~~   ->  Card.width = 200; **// 객체생성 없이 사용가능**
~~~~        ~~c.height = 300;~~  ->  Card.height = 300;
    }
}
```

kind(모양)과number(숫자)는 개별속성을 가지는 인스턴스 변수이기 때문에
참조변수 c를 이용해 접근하면된다.

---

마찬가지로 width(폭)과height(넓이)도 참조변수 c를 사용가능하지만 권장하지않는다.
위 코드와같이 참조변수가 아닌 (클래스이름.변수이름) ← 이렇게 사용하는것이 좋다.

---

```java
Card c1 = new Card(); 주소값[0x100]
Card c2 = new Card(); 주소값[0x200]
```

위와 같이 객체를 두개 만들어주었다.
c1과 c2는 서로 다른 주소값을 가지고
개별적인 속성 instance variable(인스턴스 변수)들이 각각 저장되어있다.

### 하지만 !!

공통속성을 가진 class variable(클래스 변수)는 공통적인주소를 가진다.
만약에 width라는 class variable을 400으로 변경하게되면
c1, c2모두 400으로 변경된다.

---

```java
class Main {
    public static void main(String[] args) {
        System.out.println("Card.width = " + Card.width);
        System.out.println("Card.height = " + Card.height);

        Card c1 = new Card();
        c1.kind = "Heart";
        c1.number = 7;

        Card c2 = new Card();
        c2.kind = "Spade";
        c2.number = 4;

        System.out.println("c1은 " + c1.kind + ", " + c1.number + "이며, 폭은 ("
                          + Card.width + ") 넓이는 (" + Card.height + ") 입니다.");
        System.out.println("c2은 " + c2.kind + ", " + c2.number + "이며, 폭은 ("
                          + Card.width + ") 넓이는 (" + Card.height + ") 입니다.");
        System.out.println("widtg와 height를 각각 50, 80으로 변경합니다.");
        
        Card.width = 50; // ClassVariable은 공통속성이니까
        Card.height = 80; // c1, c2 한번에 바뀐다.

        System.out.println("c1은 " + c1.kind + ", " + c1.number + "이며, 폭은 ("
                          + Card.width + ") 넓이는 (" + Card.height + ") 입니다.");
        System.out.println("c2은 " + c2.kind + ", " + c2.number + "이며, 폭은 ("
                          + Card.width + ") 넓이는 (" + Card.height + ") 입니다.");
    }
}
결과
Card.width = 100
Card.height = 250
c1은 Heart, 7이며, 폭은 (100) 넓이는 (250) 입니다.
c2은 Spade, 4이며, 폭은 (100) 넓이는 (250) 입니다.
widtg와 height를 각각 50, 80으로 변경합니다.
c1은 Heart, 7이며, 폭은 (50) 넓이는 (80) 입니다.
c2은 Spade, 4이며, 폭은 (50) 넓이는 (80) 입니다.
```

# 메서드의 선언부와 구현부

---

## 메서드란?

### 1. 문장들을 묶어놓은 것
     - 작업단위로 문장들을 묶어서 이름 붙인 것
2. 값(입력)을 받아서 처리하고, 결과를 반환(출력)
     - 함수의 객체지향개념 버전이라고 생각하면 편하다.

함수와 메서드의 차이점을 굳이 꼽자면
메서드는 반드시 클래스에 들어있어야하고 메서드는 클래스에 독립적이다.

---

## 메서드의 장점

- 코드의 중복을 줄일 수 있다.
- 코드의 유지보수가 쉽다.
- 코드를 재사용할 수 있다.
- 코드가 간결해서 이해하기 쉬워진다.

---

## 메서드의 작성

- 반복적으로 수행되는 여러 문장을 메서드로 작성
- 하나의 메서드는 한 가지 기능만 수행하도록 작성
- 유지보수시 더 용이해진다.
- 코드를 최소의 의미있는 작업단위로 나눠놔야 재사용률이 높아진다.

---

## 메서드는 선언부와 구현부로 이루어져있다.

```java
반환타입 메서드이름 (타입 변수명, 타입 변수명, ...) <- 선언부
				{
구현부-> // 호출한 메서드로 결과를 반환한다.
				}
```

# 메서드호출

---

### 메서드를 호출하는 방법
 - 메서드이름(값, 값2, …작업에 필요한 값들);

```java
public class ez {
    public static void main(String[] args) {
        you t = new you();
        System.out.println(t.add(47, 3));
    }
}
class you {
    int add(int a, int b) {
        int result = a + b;
        return result;
    }
}
결과
50
```

위 코드의 add메서드 앞에붙은 타입에 주목하자
현재 int로 되어있는데 이건 int로 값을 반환하겠다는 의미이다.

### 즉 반환하는 값이 있다면 작업에 필요한 값도 있다는 말이다.
add(int a, int b)로 값을 받아온다.

---

```jsx
public class ez {
    public static void main(String[] args) {
        you t = new you();
				t.printhello();
    }
}
class you {
		void printhello() {
				System.out.println("Hello");
		}
}
결과
"Hello"
```

이번에는 printhello메서드 앞에붙은 void타입에 주목하자
void는 반환하는 값이 없다는 의미이다.
그저 아래있는 알고리즘을 실행할 뿐이다.

### 즉 반환하는 값이 없으니 작업에 필요한 값도 없다.

---

# 호출 스택(call stack)

---

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6b3021dc-be3e-478d-b3c1-320ddf60cdbd/Untitled.png)

### 스택(stack) : 밑이 막힌 상자. 위에 차곡차곡 쌓인다.

---

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/be5a68d6-7e0b-4735-ab19-bfcea62ed3ec/Untitled.png)

### 꺼낼때는 제일 위에있는것(2)이 먼저 꺼내지게된다.

---

## 호출 스택(call stack)
 - 메서드가 작업을 하는데 필요한 메모리가 제공되는 공간
 - 메서드가 호출되면 호출스택에 메모리 할당, 종료되면 해제

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b3cdcbb0-ef98-490d-a742-dbfe6f929914/Untitled.png)

### 아래 있는 메서드(main)가 위의 메서드(println)을 호출한 것

위 그림에 메인 메서드가 호출되어 스택에 올라가있다.
main( ) 메서드가 println( ) 메서드를 호출시 main위에 println이 올라가게된다.

---

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4a388d65-aca8-4f2c-8cef-cac8a3de00aa/Untitled.png)

### 맨 위의 메서드 하나만 실행 중, 나머지는 대기중

main메서드가 println에게 일을 시키게되면 main메서드는 대기상태가되고 println은 실행된다.

---

![스크린샷 2022-12-24 오전 6.42.05.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/829c69d4-c60d-4402-86e5-459dad014208/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-12-24_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_6.42.05.png)

println이 종료되면 메모리상에서 사라진다

---

# 기본,참조형 매개변수

---

## 기본형 매개변수
 - 변수의 값을 읽기만 할 수 있다.(read only)

---

```java
class Data { int x; }

class Ex6_6 {
    public static void main(String[] args) {
        Data d = new Data();
        d.x = 10;
        System.out.println("main() : x = " + d.x);

        change(d.x);
        System.out.println("After change(d.x)");
        System.out.println("main() : x = " + d.x);
    }
    static void change(int x) { // 기본형 매개변수
        x = 1000;
        System.out.println("change() : x = " + x);
    }
}
```

위 코드만을 보고 프로그램 진행 순서,
스택메모리에 어떻게 저장되고 삭제되는지 그림으로 그릴 수 있어야한다.
아래는 프로그램 진행 순서 동영상

[1.mp4](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2888ed46-2e6b-4edc-b8b2-7d80361a8166/1.mp4)

[2.mp4](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cb90ca04-468f-4946-8938-305ff845932b/2.mp4)

---

## 참조형 매개변수
 - 변수의 값을 읽고 변경할 수 있다.(read & write)

```java
class Data { int x; } // 3.

class Ex6_6 {
    public static void main(String[] args) {
        Data d = new Data(); // 1.
        d.x = 10; // 2.
        System.out.println("main() : x = " + d.x); // 4.

        change(d); // 5.
        System.out.println("After change(d.x)"); // 9.
        System.out.println("main() : x = " + d.x); // 10.
    }
    static void change(Data d) { //6 // 참조형 매개변수
        d.x = 1000; // 7.
        System.out.println("change() : x = " + x); // 8.
    }
}
```

여기선 메서드의 매개변수로 Data클래스의 리모콘 d를 참조형 매개변수로 사용하여
메서드에서 Data클래스의 변수에 접근할 수 있는 것이다.

---

## 참조형 반환타입

```java
class Data { int x; }

class Ex6_6 {
    public static void main(String[] args) {
        Data d = new Data();
        d.x = 10;

        Data d2 = copy(d);
        System.out.println("d.x = " + d.x);
        System.out.println("d2.x = " + d2.x);
    }
    static Data copy(Data d) {
        Data tmp = new Data();

        tmp.x = d.x;

        return tmp;
    }
}
```

---

```java
class Bar {
    
    Foo getFooObj() {
        
        return new Foo();
    }
}

class Foo {
    int x = 3;
}

public class MyProject {
    public static void main(String[] args) {
        Foo f1 = (new Bar()).getFooObj();
    }
}
```

1. Bar객체가 샌성된다.
2. . 을 이용하여 Bar클래스의 getFooObj메서드를 호출한다.
3. Foo 객체가 생성된다.
4. 반환형이 클래스타입이기 때문에 Foo객체의 주소값을 반환한다.
5. Foo객체의 주소값이 f1참조변수에 저장된다.
6. Bar객체는 접근할 수 있는 참조변수가 없으니 가비지컬렉터에의해 잡아먹힌다.

# this( )

- 생성자에서 다른 생성자 호출할 때 사용
- 다른 생성자 호출시 첫 줄에서만 사용가능

```java
class Car2 {
	String color;
	String gearType;
	int door;
	
	Car2() {
		this("white", "auto", 4);
	}

	Car2(String color) {
		this(color, "auto", 4);
	}

	Car2(String color, String gearType, int door) {
		this.color = color;
		this.gearType = gearType;
		this.door = door;
	}
}
```

### this( )는 생성자이름(매개변수); 와 같은 역할을 한다.

---

## 참조변수 this (위와 전혀다른 문법)

- 인스턴스 자신을 가리키는 참조변수
- 인스턴스 메서드(생성자 포함)에서 사용가능
- 지역변수(lv)와 인스턴스 변수(iv)를 구별할 때 사용

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a0e531d6-d905-4435-97c8-3d1a6e4cd06b/Untitled.png)

원래 this가 붙어야하지만 같은 클래스이기 때문에 생략된 것이다.

지역변수String color와 인스턴스 변수color는 서로 다르기 때문에
구별을 해줘야한다(이름이 같은경우 햇갈리니까)

# 상속(Inheritane)

- 기존의 클래스로 새로운 클래스를 작성하는 것.(코드의 재사용)
- 두 클래스를 부모와 자식으로 관계를 맺어주는 것.

---

### 상속으로 클래스를 작성하는 법

```java
class 자식클래스 extends 부모클래스 {
	// ...
}

class Parent { } // 부모클래스

class Child extends Parent {
  // ...
}
```

---

### 상속의 특징

- 자손은 조상(부모의 부모)의 모든 멤버를 상속받는다. (생성자, 초기화블럭 제외)
- 자손의 멤버 개수는 조상보다 적을 수 없다. (같거나 많다.)

```java
class Parent {
	int age;
}

class Child extends Parent { }
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d3b94a85-5fb7-458b-a51f-1d7ee21b28d5/Untitled.png)

Child클래스는 멤버가 하나도 없었지만 부모에게 상속받아 age멤버가 하나 생겼다.

---

- 자손의 변경은 조상에 영햘을 미치지 않는다.

```java
class Parent {
	int age;
}

class Child extends Parent {
	void play() {
			System.out.println("놀자");
		}
}
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b7040a7a-16f5-49c3-b390-cde63681be32/Untitled.png)

Parent의 멤버는 1개 Child는 원래 가지고있던
멤버메서드 1개 + 상속받은 멤버1개를 더해 2개가 된다. (부모에게는 영향X)

---

### 상속을 받는경우・안받는 경우

```java
class Point {
	int x;
	int y;
}
```

2차원 좌표를 찍는 class가 있다고 가정해보자
3차원 좌표를 찍는 class를 만드는 방법은?

### 상속을 받지않고 만들기

```java
class Point3D {
	int x;
	int y;
	int z;
}
```

상속을 받지않고 새로운 클래스에 새로운 변수를 지정해준다.

Point 클래스의 영향을 받지 않음

### 상속을 받고 만들기

```java
class Point3D extends Point {
	int z;
}
```

Point클래스를 상속받아 int x, int y를 가져온다
Point3D클래스에서는 int z만 선언해주면 x,y,z의 멤버가 완성된다.

Point 클래스(부모)의 영향을 받음

---

### 예시

```java
public class nana {
    public static void main(String[] args) {
        SmartTv stv = new SmartTv();
        stv.channel = 10;
        stv.channelUp();
        System.out.println(stv.channel);
        stv.displayCaption("Hello");
        stv.caption = true;
        stv.displayCaption("SEEBAR"); 
    }
}

class Tv {
    boolean power;
    int channel;

    void power() { power = !power; }
    void channelUp() { ++channel; }
    void channelDown() { --channel; }
    
}

class SmartTv extends Tv {
    boolean caption;

    void displayCaption(String text) {
        if (caption) {
            System.out.println(text);
        }
    }
}
결과
11
SEEBAR
```

# 포함(composite)

- 클래스의 멤버로 참조변수를 선언하는 것

```java
class Circle {
	int x;
	int y;
	int r;
}
```

```java
class Point {
	int x;
	int y;
}

class Circle {
	Point c = new Point();
	int r;
}
```

위 두개의 코드의 Circle 클래스의 구성요소는 같다고 볼수있다.

아래의 코드는 Circle클래스에 Point클래스가 포함되어있는 것이다.

---

# 클래스 간의 관계 결정하기

포함관계  ‘~은 ~를 가지고 있다.(has - a)’

```java
class Circle {
	point c = new Point();
	int r;
}
```

상속관계 ‘~은 ~이다.(is - a)’

```java
class Circle extends Point {
	int r;
}
```

대부분 포함관계를 사용한다.
상속은 여러 제약이있어 꼭 필요할때만 사용한다.

### 단일 상속(Single Inheritance)

java는 단일상속(하나의 부모)만 허용한다

---

### 다중상속처럼 작성하고싶으면?

- 비중이 높은 클래스 하나만 상속관계로, 나머지는 포함관계로 한다.

---

### Object클래스 - 모든 클래스의 조상

- 부모가 없는 클래스는 자동적으로 Object클래스를 상속받게 된다.

```java
class Tv {

}

class SmartTv extends Tv {

}
```

```java
class Tv extends Object {

}

class SmartTv extends Tv {

}
```

위 두 코드는 같다.
모든 클래스는 Object클래스에 정의된 11개의 메서드를 상속받는다.
toString(), equals(Object obj), hashCode(), 등등.. 

```java
class Mypoint extends Object {

}

class Circle extends Object {
    Mypoint p;
    int r;

    Circle() {
        p = new Mypoint();
    }
}

public class nana {
    public static void main(String[] args) {
        Circle c = new Circle();
        System.out.println(c);
        Circle c2 = new Circle();
        System.out.println(c2.toString());
    }
}
결과
Circle@2f92e0f4
Circle@28a418fc
```

toString()과 참조변수를 출력하면 같은 기능을 한다.

## 오버라이딩(overrideing)

- 상속받은 조상의 메서드를 자신에 맞게 변경하는 것

---

```java
class Point {
	int x;
	int y;
	
	String getLocation() {
		return "x :"  + x + ", y :" + y;
	}
}

class Point3D extends Point {
	int z;
	
	String getLocation() {
		return "x :"  + x + ", y :" + y + ", z :" + z;
	}
}

public class nana {
    public static void main(String[] args) {
        Point3D p = new Point3D();
        p.x = 3;
        p.y = 5;
        p.z = 7;
        System.out.println(p.getLocation());
    }
}
결과
x: 3, y: 5, z: 7
```

Point3D클래스에서 getLocation 메서드를 선언해주었다.
오버라이딩의 조건중 하나로 조상의 메서드와 선언부가 일치해야 한다.
내용은 추가, 혹은 변경해주어야 한다.

---

## 오버라이딩의 조건

1. 선언부가 조상 클래스의 메서드와 일치해야 한다.
2. 접근 제어자를 조상 클래스의 메서드보다 좁은 범위로 변경할 수 없다.
3. 예외는 조상 클래스의 메서드보다 많이 선언할 수 없다.

## 참조변수 super

- 객체 자신을 가리키는 참조변수. 인스턴스 메서드(생성자)내에만 존재
- 조상의 멤버를 자신의 멤버와 구별할 때 사용

this.x ← 내 멤버 / super.x ← 조상 멤버

---

## super() - 조상의 생성자

```java
class Point {
    int x, y;

    Point(int x, int y) {
        this.x = x;
        this.y = y;
    }
}

class Point3D extends Point {
    int z;

    Point3D(int x, int y, int z) {
        super(x, y);
        this.z = z;
    }
}
```

자손클래스에서 조상클래스의 멤버변수를 초기화해주고싶을 때
super()를 이용해 조상의 생성자를 호출하여 초기화해주도록 하자.
this.x = x; 와 같이 초기화하면 에러

---

- 생성자의 첫 줄에 반드시 생성자를 호출해야 한다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/429cb2fe-a765-47da-a220-888a6a282b10/Untitled.png)

기본생성자는 꼭 생성해주자 생성자 첫 줄에 생성자를 호출하지않으면
자동으로 super()가 들어가게되는데 위 그림에서는
Point3D클래스의 생성자에서 생성자를 호출하지않았기에 super()가
자동으로 호출된다 super()는 부모생성자() 와 의미가 같기때문에
Point클래스의 기본 생성자를 찾게된다 하지만 Point클래스에 기본생성자가 지금
정의되어있지않아 오류가 발생하는 것이다.

# 패키지(package)

- 서로 관련된 클래스의 묶음
- 클래스는 클래스 파일(*.class), 패키지는 폴더. 하위 패키지는 하위 폴더
- 클래스의 실제 이름(full name)은 패키지를 포함.(java.lang.String)
rt.jar는 클래스들을 압축한 파일(JDK설치경로에 위치)

---

### 패키지의 선언

- 패키지는 소스파일의 첫 번째 문장으로 단 한번 선언
- 같은 소스 파일의 클래스는 모두 같은 패키지에 속하게 된다.
- 패키지 선언이 없으면 이름없는(unnamed) 패키지에 속하게 된다.

---

### import문

- 클래스를 사용할 때 패키지이름을 생략할 수 있다.
- 컬파일러에게 클래스가 속한 패키지를 알려준다.

```java
import java.util.*;
java패키지안의 util패키지안에 모든클래스를 import
```

---

### static import문

- static멤버를 사용할 때 클래스 이름을 생략할 수 있게 해준다.

```java
import static java.lang.Integer.*;     // Integer클래스의 모든 static메서드
import static java.lang..Math.random;  // Math.random()만 괄호X
import static java.lang.System.out;    // System.out을 out만으로 참조가능
```

---

```java
import static java.lang.System.out;
import static java.lang.Math.*;

public class nana {
    public static void main(String[] args) {
        // System.out.println(Math.random());
        out.println(random());
        
        // System.out.println("Math.PI : " + Math.PI);
        out.println("Math.Pi : " + PI);
    }
}
```

위처럼 패키지를 import static 해주었다면 안에있는 기능만 사용해주면된다.
이처럼 import를 시켜주는 이유는 코딩을 하다보면 코드가 길어지는데
그때마다 일일이 클래스이름을 적어주면 미관상에도 안좋고 가독성이 떨어지기 때문이다.

## 제어자(modifier)

- 클래스와 클래스의 멤버(멤버변수, 메서드)에 부가적인 의미 부여

---

### 접근제어자

- public, protected, (default), private

### 그          외

- static, final, abstract, native, transient, synchronized, volatile, strictfp

---

- 하나의 대상에 여러 제어자를 같이 사용가능(접근 제어자는 하나만)

```java
public class nana {
    public static final int WIDTH = 200;
    public static void main(String[] args) {
        System.out.println("WIDTH = " + WIDTH);   
    }
}
```

## 접근제어자(access modifier)

- private      - 같은 클래스 내에서만 접근이 가능하다.
- (default)   - 같은 패키지 내에서만 접근이 가능하다.
- protected - 같은 패키지 내에서, 그리고 다른 패키지의 자손클래스에서 접근이 가능하다.
- public       - 접근 제한이 전혀 없다.

public > protected > (default) > private

default는 아무것도 안붙히면 붙는다.

---

```java
class MyProject {
    private   int prv; // 같은 클래스
              int dft; // 같은 패키지
    protected int prt; // 같은 패키지 + 자손(다른 패키지)
    public    int pub; // 접근제한 없음.

    public void printMembers() {
        System.out.println(prv);
        System.out.println(dft);
        System.out.println(prt);
        System.out.println(pub);
    }
}

public class MyPro {
    public static void main(String[] args) {
        MyProject p = new MyProject();
        System.out.println(p.prv); // 같은 클래스X 접근 불가
        System.out.println(p.dft); // 접근 가능
        System.out.println(p.prt); // 접근 가능
        System.out.println(p.pub); // 접근 가능
        
    }
}
```

---

패키지 1 

```java
package pkg1;

public class MyProject {
    private   int prv; // 같은 클래스
              int dft; // 같은 패키지
    protected int prt; // 같은 패키지 + 자손(다른 패키지)
    public    int pub; // 접근제한 없음.

    public void printMembers() {
        System.out.println(prv);
        System.out.println(dft);
        System.out.println(prt);
        System.out.println(pub);
    }
}

public class MyPro {
    public static void main(String[] args) {
        MyParent p = new MyParent();
        System.out.println(p.prv);
        System.out.println(p.dft);
        System.out.println(p.prt);
        System.out.println(p.pub);
        
    }
}
```

패키지 2

```java
package pkg2;

import pkg1.MyProject;

class MyChild extends MyProject {
    public void printMembers() {
        System.out.println(prv); // 접근 불가
        System.out.println(dft); // 접근 불가
        System.out.println(prt); // 자손클래스니까 접근가능
        System.out.println(pub); // 어디든 가능
    }
}

public class test {
    public static void main(String[] args) {
        MyProject p = new MyProject();
        System.out.println(p.prv); // 접근 불가
        System.out.println(p.dft); // 접근 불가
        System.out.println(p.prt); // 자손이 아니라 접근 불가
        System.out.println(p.pub); // 어디든 가능

    }
}
```

# 캡슐화

### 접근 제어자를 사용하는 이유

 - 외부로부터 데이터를 보호하기 위해서
 - 외부에는 불필요한, 내부적으로만 사용되는, 부분을 감추기 위해서

```java
public class MyProject {
    public int hour;  0 ~ 24
    public int minute;0 ~ 59
    public int second;0 ~ 59
}

class a {
    public static void main(String[] args) {
        MyProject t = new MyProject();
        t.hour = 25;
    }
}
```

시간, 분, 초를 저장하는 instance variable을 만들었다.
시간, 분, 초는 무슨일이있어도 범위를 넘어가서는 안된다.
public은 어떤경우에도 접근이 가능하기때문에 아래와같이 hour가 25로 바뀌어 버린다.
이러한 데이터를 보호하는 것을 캡슐화라고 한다.

```java
public class MyProject {
    private int hour;
    private int minute;
    private int second;

    public int getHour() { return hour; }

    public void setHour(int hour) {
        if (hour < 0 || hour > 23) return; // 조건만족 시 hour변경하지않고
																														//return
        this.hour = hour;
    }
}
```

위와같이 접근제어자를 private로 설정해주면
다른 클래스에서 직접 접근이 불가능하고 메서드를 통해 간접 접근해야한다.

---

# 캡슐화

### 접근 제어자를 사용하는 이유

 - 외부로부터 데이터를 보호하기 위해서
 - 외부에는 불필요한, 내부적으로만 사용되는, 부분을 감추기 위해서

```java
public class MyProject {
    public int hour;  0 ~ 24
    public int minute;0 ~ 59
    public int second;0 ~ 59
}

class a {
    public static void main(String[] args) {
        MyProject t = new MyProject();
        t.hour = 25;
    }
}
```

시간, 분, 초를 저장하는 instance variable을 만들었다.
시간, 분, 초는 무슨일이있어도 범위를 넘어가서는 안된다.
public은 어떤경우에도 접근이 가능하기때문에 아래와같이 hour가 25로 바뀌어 버린다.
이러한 데이터를 보호하는 것을 캡슐화라고 한다.

```java
public class MyProject {
    private int hour;
    private int minute;
    private int second;

    public int getHour() { return hour; }

    public void setHour(int hour) {
        if (hour < 0 || hour > 23) return; // 조건만족 시 hour변경하지않고
																														//return
        this.hour = hour;
    }
}
```

위와같이 접근제어자를 private로 설정해주면
다른 클래스에서 직접 접근이 불가능하고 메서드를 통해 간접 접근해야한다.

---

## 참조변수의 형변환

---

```java
class MyProject {
    public static void main(String[] args) {
        Car car = null;
        FireEngine fe = new FireEngine();
        FireEngine fe2 = null;

        fe.water();
        car = fe; // car = (Car)fe; 에서 형변환 생략됨
        fe2 = (FireEngine)car; // 조상타입 -> 자손타입 형변환 필수
        fe2.water();
    }
}

class Car {
    String color;
    int door;

    void drive() {
        System.out.println("drive, brrr");
    }

    void stop() {
        System.out.println("stop!");
    }
}

class FireEngine extends Car {
    
    void water() {
        System.out.println("물 발사");
    }
}
```

### 자손타입 → 조상타입 자동형변환 가능

car = fe; 에서 car에 fe가 가리키는 FireEngine객체의 주소값을 가리키려면
fe를 Car타입(조상타입)으로 형변환 해주어야 하는데 이때 형변환은 생략가능하다.

### 조상타입 → 자손타입 자동형변환 불가능

fe2 = (FireEngine)car; 에서 car는 원래 자료형이 Car이고 fe가 가리키는
FireEngine객체를 가리키다가 자손타입으로 형변환되어 fe2에
car가 가리키는 FireEngine객체의 주소값을 가지게된다
이 fe2는 자료형이 FireEngine이기때문에 water에 접근가능하다.

### instanceof 연산자

 - 참조변수의 형변환 가능여부 확인에 사용. 가능하면 true 반환

```java
void doWork(Car c) {
    if (c instanceof FireEngine) { // 1. 형변환이 가능한지.
    FireEngine fe = (FireEngine)c; // 2. 형변환
    fe.water ();
    　・・・・・・・
    FireEngine fe = new FireEngine();
    System.out.println(fe instanceof Object);    // true
    System.out.printIn(fe instanceof Car);       // true
    System.out.printIn(fe instanceof FireEngine);// true
    Object obj = (Object)fe; // Ok
    Car    c   = (Car)fe;    // Ok
```

형변환은 형제클래스끼리는 불가능하다
FireEngine의 부모는 Car Car의 부모는 Object인데
instanceof는 이 참조변수가 가리키는게 이 클래스가 맞느냐? 라는 의미다.
fe가 Car를 가리킨다는 것은 FireEngine이 Car에게 상속받았기때문에 true라는 결과가 나온다.

---

### 참조변수의 형변환을 왜 하냐?

 - 참조변수를 변경함으로써 사용할 수 있는 멤버의 갯수를 조절하기 위해서

### instanceof연산자는 언제 사용하냐?

 - 참조변수를 형변환하기 전에 형변환 가능여부를 확인할때
 
## 매개변수의 다형성

다형성의 장점
  1.  다형적 매개변수
  2. 하나의 배열로 여러종류 객체 다루기

```java
다형성
Tv t = new SmartTv();
----------------------------------
참조변수의 형변환 - 사용가능한 멤버갯수 조절
----------------------------------
instanceof 연산자 - 형변환 가능여부 확인
```

참조형 매개변수는 메서드 호출시, 자신과 같은 타입 또는 자손타입의 인스턴스를 넘겨줄 수 있다.

```java
class Product {
    int price;
    int bonusPoint;

    Product(int price) {
        this.price = price;
        bonusPoint = (int)(price/10.0);
    }
}

class Tv1 extends Product {
    Tv1() {
        super(100);
    }

    public String toString() {return "Tv";}
}

class Computer extends Product {
    Computer() {super(200);}
    public String toString() {return "Computer";}
}

class Buyer {
    int money = 1000;
    int bonusPoint = 0;

    void buy(Product p) {
        if(money < p.price) {
            System.out.println("잔액이 부족합니다.");
            return;
        }
        money -= p.price;
        bonusPoint += p.bonusPoint;
        System.out.println(p + "을 구입하셨습니다.");
    }
}

public class Myproject {
    public static void main(String[] args) {
        Buyer b = new Buyer();

				b.buy(new Tv1());
				b.buy(new Computer());

        System.out.println("남은돈 : " + b.money + "만원입니다.");
        System.out.println("현재 보너스점수는 : " + b.bonusPoint + "점입니다.");
   }
}
결과
Tv을 구입하셨습니다.
Computer을 구입하셨습니다.
남은돈 : 700만원입니다.
현재 보너스점수는 : 30점입니다.
```

1. Buyer클래스의 buy메서드를 호출 인자값으로 Tv1객체를 넣는다.
2. Tv1클래스의 생성자는 Product의 생성자를 호출해 p.price의 값이 100이 됨
3. 1000 -= 100, 0 += 10이되고 p + 문자열 출력에 p는 toString의 return값이 출력된다.
4. Computer도 위 내용과 동일한 로직

---

```java
Buyer b = new Buyer();
b.buy(new Tv1());

Product p = new Tv1();
b.buy(p)
```

같다.

## 매개변수의 다형성

다형성의 장점
  1.  다형적 매개변수
  2. 하나의 배열로 여러종류 객체 다루기

```java
다형성
Tv t = new SmartTv();
----------------------------------
참조변수의 형변환 - 사용가능한 멤버갯수 조절
----------------------------------
instanceof 연산자 - 형변환 가능여부 확인
```

참조형 매개변수는 메서드 호출시, 자신과 같은 타입 또는 자손타입의 인스턴스를 넘겨줄 수 있다.

```java
class Product {
    int price;
    int bonusPoint;

    Product(int price) {
        this.price = price;
        bonusPoint = (int)(price/10.0);
    }
}

class Tv1 extends Product {
    Tv1() {
        super(100);
    }

    public String toString() {return "Tv";}
}

class Computer extends Product {
    Computer() {super(200);}
    public String toString() {return "Computer";}
}

class Buyer {
    int money = 1000;
    int bonusPoint = 0;

    void buy(Product p) {
        if(money < p.price) {
            System.out.println("잔액이 부족합니다.");
            return;
        }
        money -= p.price;
        bonusPoint += p.bonusPoint;
        System.out.println(p + "을 구입하셨습니다.");
    }
}

public class Myproject {
    public static void main(String[] args) {
        Buyer b = new Buyer();

				b.buy(new Tv1());
				b.buy(new Computer());

        System.out.println("남은돈 : " + b.money + "만원입니다.");
        System.out.println("현재 보너스점수는 : " + b.bonusPoint + "점입니다.");
   }
}
결과
Tv을 구입하셨습니다.
Computer을 구입하셨습니다.
남은돈 : 700만원입니다.
현재 보너스점수는 : 30점입니다.
```

1. Buyer클래스의 buy메서드를 호출 인자값으로 Tv1객체를 넣는다.
2. Tv1클래스의 생성자는 Product의 생성자를 호출해 p.price의 값이 100이 됨
3. 1000 -= 100, 0 += 10이되고 p + 문자열 출력에 p는 toString의 return값이 출력된다.
4. Computer도 위 내용과 동일한 로직

---

```java
Buyer b = new Buyer();
b.buy(new Tv1());

Product p = new Tv1();
b.buy(p)
```

같다.

## 여러 종류의 객체를 배열로 다루기

 - 조상타입의 배열에 자손들의 객체를 담을 수 있다. (하나의 배열에 여러종류 객체 저장)

```java
class Product {
    int price;
    int bonusPoint;

    Product(int price) {
        this.price = price;
        bonusPoint = (int)(price/10.0);
    }
}

class Tv1 extends Product {
    Tv1() { super(100); }

    public String toString() {return "Tv";}
}

class Computer extends Product {
    Computer() {super(200);}

    public String toString() {return "Computer";}
}

class Audio extends Product {
    Audio() { super(50); }

    public String toString() {return "Audio";}
}

class Buyer {
    int money = 1000;
    int bonusPoint = 0;
    Product[] cart = new Product[10];
    int i = 0;

    void buy(Product p) {
        if(money < p.price) {
            System.out.println("잔액이 부족합니다.");
            return;
        }
        money -= p.price;
        bonusPoint += p.bonusPoint;
        cart[i++] = p; (111)
        System.out.println(p + "을 구입하셨습니다.");
    }

    void summary() {
        int sum = 0;
        String itemList = "";

        for(int i = 0; i <cart.length; i++) {
            if(cart[i]==null) break;
            sum += cart[i].price;
            itemList += cart[i] + ", ";
        }
        System.out.println("구입하신 물품의 총금액은 " + sum + "만원입니다.");
        System.out.println("구입하신 제품은 " + itemList + "입니다.");
    }
}
public class Myproject {
    public static void main(String[] args) {
        Buyer b = new Buyer();

				b.buy(new Tv1());
				b.buy(new Computer());
        b.buy(new Audio());
        b.summary();
   }
}
결과
Tv을 구입하셨습니다.
Computer을 구입하셨습니다.
Audio을 구입하셨습니다.
구입하신 물품의 총금액은 350만원입니다.
구입하신 제품은 Tv, Computer, Audio, 입니다.
```

Product(조상)타입의 배열을 생성해 자손 객체를 저장해보러햔다.

(111)부분에서 cart[0]번째에 Tv1객체가 저장된다
그리고 Tv1을 구입했다는 문자를 출력해준다 다른 클래스들도 이 과정을 거친다

---

마지막으로 summary메서드를 실행하는데
배열의 값만큼 반복하도록 반복문을 만들어주고
sum변수에 cart에 저장된 각 개체의 price(가격)을 더해준다
String타입의 itemList변수에 cart의 toString을 불러와서 저장해 구매한 제품목록을 만들어준다.

---

위 코드에서는 배열이 0~9까지있는데 객체를 3개만 저장하기때문에
cart[3]은 null값이 저장되어있다. null을 만나면 break를 해 반복문을 마쳐준다.

---

## 추상 클래스(abstract class)

- 미완성 설계도. 미완성 메서드를 갖고 있는 클래스

```java
abstract class Player { // 미완성 클래스
    abstract void play(int pos); // 추상 메서드 
    abstract void stop(); // 추상 메서드는 { } 몸통이 없다 미완성이니 어찌보면 당연함
}
```

- 다른 클래스 작성에 도움을 주기 위한 것. 인스턴스 생성 불가

```java
~~Player p = new Player()~~;  // 추상 클래스의 인스턴스(객체)는 생성 불가능
```

- 상속을 통해 추상 메서드를 완성해야 인스턴스 생성가능

```java
abstract class Player {
    abstract void play(int pos);
    abstract void stop();
}

class AudioPlayer extends Player {
    void play(int pos) { System.out.println("실행"); } // 몸통을 만드는것을 "구현"이라고 함
    void stop() { System.out.println("정지"); } 

    AudioPlayer ap = new AudioPlayer();
}
```

## 추상클래스의 작성

- 여러 클래스에 공통적으로 사용될 수 있는 추상클래스를 바로 작성하거나
기존클래스의 공통 부분을 뽑아서 추상클래스를 만든다.

```java
abstract class Unit {
    int x, y;
    abstract void move(int x, int y);
    void stop() {}
}

class Marine extends Unit {
    void move(int x, int y) {}
    void stimpack() {}
}

class Tank extends Unit {
    void move(int x, int y) {}
    void changeMode() {}
}

class Dropship extends Unit {
    void move(int x, int y) {}
    void load() {}
    void unload() {}
}

public class Myproject {
    public static void main(String[] args) {
        Unit[] group = new Unit[3];
        group[0] = new Marine();
        group[1] = new Tank();
        group[2] = new Dropship();
        
        for(int i = 0; i < group.length; i++) {
            group[i].move(100, 200);
        }
    }
}
```

각 유닛은 이동한다는 공통점을 가지고있다. move라는 추상메서드를 만들어
한번에 관리해주면 코드가 간결해지고 가시성이 높아진다.

