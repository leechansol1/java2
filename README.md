# 202103323 이찬솔

## 4월 18일 (8주차)

# 객체속의 this

객체속 변수 

이름 : 값 > key & value , 키 와 값 


let person1 = {
​

name : "홍길동",

cm : 180,

kg : 80,

age : 20,

birthday: "681212",

id : "123456",

eat : function(){ /*실행문*/},

uId : function(){

// this : 자기자신 객체 의미

return this.birthday+"-"+this.id;

}

};

​

객체 호출방법

객체이름.프로퍼티이름

console.log(person.name);

console.log(person["name"]);

​

객체의 파라미터를 호출하는 방법

객체이름.매소드이름()

console.log(person.eat());

​

 for in / for of

​

let key : object안에 있는 이름값

for ( 변수명 in 객체, 배열 )

​

for (let key in person) {

console.log( key+ " : "+ person[key] );

}

​

 function을 이용해서 객체 만들기

프로토타입(기본모습) > 생성자메소드

​

function Person(name,cm,kg,addr,age){

// this가 붙은 변수는 function내부의 변수에 선언한다

// this가 없는 변수는 파라미터로 받은 변수

this.name = name;

this.cm = cm;

this.kg = kg;

this.addr = addr;

this.age = age;

}
# 상속

## 객체지향 프로그래밍에서는 부모 역할의 상위 객체와 자식 역할의 하위 객체가 있습니다. 부모 객체는 자기가 가지고 있는 필드와 메소드를 자식 객체에게 물려주어 자식 객체가 사용할 수 있도록 합니다. 이것이 상속 Inheritance이다. 상속을 하는 이유는 다음과 같습니다.

• 코드의 재사용성을 높여 준다.

잘 개발된 부모 객체의 필드와 메소드를 자식이 그대로 사용할 수 있어 자식 객체에서 중복 코딩을 하지 않아도 됩니다.

 

• 유지 보수 시간을 최소화시켜 준다.

 부모 객체의 필드와 메소드를 수정하면 모든 자식 객체들은 수정된 필드와 메소드를 사용할 수 있습니다.


## 🧩 그렇다면 왜 `p = s`로 업캐스팅을 한 걸까?

이 사례는 **업캐스팅의 제한 사항을 설명하기 위한 코드**입니다.

- 실제로는 이런 식으로 업캐스팅을 사용하지는 않습니다.  
- **실제 사용 목적**은 여러 자식 클래스를 **하나의 부모 타입으로 다루기 위해서**입니다.

## ☕ 예제 코드

```java
Person[] people = new Person[3];
people[0] = new Student("홍길동");
people[1] = new Student("김영희");
people[2] = new Person("이순신");

# 4월 17일 (7주차)

## 배운내용

# 매개변수(parameter)와 전달인자(argument)

종종 매개변수(parameter)와 전달인자(argument)는 적당히 섞어서 쓰이기도 하며, 이 경우 문맥에 따라 의미를 달리 해석되기도 합니다. 하지만 엄밀히 말해서:

- **매개변수**는 함수의 정의 부분에 나열되어 있는 변수들을 의미합니다.
- **전달인자**는 함수를 호출할 때 전달되는 실제 값을 의미합니다.

이 같은 의미를 명확히 하기 위해 매개변수는 **변수(variable)**로, 전달인자는 **값(value)**으로 보는 것이 일반적입니다.

## 매개변수와 전달인자의 예

- 함수 정의: `f(x) = x * x`
  - 여기서 변수 `x`가 **매개변수**입니다.
  
- 함수 호출: `f(2)`
  - 여기서 값 `2`가 **전달인자**입니다.
 

## 매개변수의 특성

각각의 매개변수는 함수의 정의 부분에 포함되어 있는 고유한 특성입니다. 예를 들어, (대다수의 언어에서는) 입력으로 들어온 2개의 정수를 더해서 합을 계산해 주는 함수의 경우 정수 형태의 매개변수 2개가 필요합니다. 일반적으로 함수는 몇 개의 매개변수를 가지든 상관없으며, 매개변수가 하나도 없을 수도 있습니다.

- 만약 함수가 매개변수를 가질 경우, 각각의 매개변수에 대한 정의를 나열해 놓은 것을 **매개변수 목록(parameter list)**이라고 합니다.

## 전달인자 목록

반면, 전달인자는 함수가 호출될 때 제공되는 값들을 말하며, 함수 정의의 한 부분으로 바뀌지 않는 매개변수와는 달리 호출할 때마다 값이 바뀔 수 있습니다. 함수를 호출하는 부분에서 전달인자를 나열해 놓을 것을 **전달인자 목록(argument list)**이라고 합니다.


# parameter (매개변수)
# 함수의 정의 부분에 나열되어 있는 변수, 여기서는 plus 함수 정의시에 사용되는 a, b를 parameter(매개변수) 라고 한다.
def plus(a, b):
  return a + b

# argument (전달인자)
# 함수를 호출할때 전달 되는 실제 값, 여기서는 plus 라는 함수에 넣어주는 값 1, 2를 argument(전달인자)라고 한다.
result = plus(1, 2)

# 생성자 개념

## 1. 기본 생성자 (Default Constructor)
- 매개변수가 없는 생성자입니다.
- 생성자가 하나도 없을 때는 컴파일러가 자동으로 추가해줍니다.

## 2. 매개변수가 있는 생성자
- 매개변수가 있는 생성자입니다.
- 기본 생성자 없이 매개변수가 있는 생성자만 있는 경우, 생성자를 호출하면 에러가 발생하므로 기본 생성자도 항상 작성해두는 습관을 갖는 것이 좋습니다.

## cf. this()와 this의 차이

### 생성자 this()
- 생성자에서 다른 생성자를 호출할 때 사용합니다.
- 같은 클래스 안에 있는 생성자를 호출할 때 사용하며, 클래스 이름 대신 `this`를 사용합니다.
- 반드시 첫 번째 줄에서만 사용 가능합니다.

### 참조변수 this
- 참조변수 `this`는 인스턴스 자신을 가리키는 용도입니다.
- 생성자와 인스턴스 메서드에서 사용 가능하며, 클래스 메서드에서는 사용 불가능합니다.
- 지역 변수와 인스턴스 변수를 구별할 때 사용합니다.
  - 인스턴스 변수: `this.var`

## 결론
- 생성자 `this()`와 참조변수 `this`는 전혀 다른 것이므로 헷갈리지 않도록 주의해야 합니다.

### 코드 예시
    class Person {
    String name;
    int age;

     //기본 생성자
    public Person() {
        this.name = "이름 없음";
        this.age = 0;
    }

     //매개변수 생성자
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

     //복사 생성자
    public Person(Person other) {
        this.name = other.name;
        this.age = other.age;
    }

    public void displayInfo() {
        System.out.println("이름: " + name + ", 나이: " + age);
    }
    }

public class Main {
    public static void main(String[] args) {
        //기본 생성자 사용
        Person person1 = new Person();
        person1.displayInfo();

        //매개변수 생성자 사용
        Person person2 = new Person("홍길동", 25);
        person2.displayInfo();

        //복사 생성자 사용
        Person person3 = new Person(person2);
        person3.displayInfo();
    }
    }

# 객체 소멸자와 Garbage Collector

## Garbage Collector
- 참조하지 않는 배열이나 객체는 Garbage Collector가 힙 영역에서 자동적으로 소멸시킵니다.
- Garbage Collector는 객체를 소멸하기 직전에 마지막으로 객체 소멸자 `finalize()`를 실행합니다.

## 소멸자
- `Object`의 `finalize()` 메서드는 기본적으로 실행 내용이 없습니다.
- 객체가 소멸되기 전에 마지막으로 사용했던 자원(데이터 연결, 파일 등)을 닫거나 중요한 데이터를 저장하고 싶다면 `Object`의 `finalize()`를 재정의할 수 있습니다.

#### 예제
```java
public class Counters {
    private int no;

    public Counters(int no) {
        this.no = no;
    }

    @Override
    protected void finalize() throws Throwable {
        // finalize()를 오버라이딩
        System.out.println(no + "번 객체의 finalize()가 실행됨");
    }
    }
    

# 4월 10일 (6주차)

## 배운 내용

#### 캡슐화 (Encapsulation)
- 객체의 데이터(필드)와 동작(메소드)을 하나로 묶고, 실제 구현 내용을 외부에 감추는 것.
- 외부 객체는 객체 내부의 구조를 알지 못하며, 객체가 노출해서 제공하는 필드와 메소드만 이용할 수 있음.

#### 객체 지향 프로그래밍 (OOP)
- 모든 데이터를 객체(object)로 취급하며, 이러한 객체가 프로그래밍의 중심이 됨.
- 객체란 실생활에서 인식할 수 있는 사물로 설명할 수 있음.
- 객체의 상태(state)와 행동(behavior)을 구체화하는 프로그래밍.

#### 클래스 (Class)
- 자바에서 클래스란 객체를 정의하는 틀 또는 설계도.
- 클래스는 객체의 상태를 나타내는 필드(field)와 객체의 행동을 나타내는 메소드(method)로 구성됨.
- 필드: 클래스에 포함된 변수(variable).
- 메소드: 특정 작업을 수행하기 위한 명령문의 집합.

#### 인스턴스 (Instance)
- 클래스를 사용하기 위해 해당 클래스 타입의 객체를 선언하는 과정.
- 이렇게 선언된 객체를 인스턴스라고 하며, 메모리에 할당된 객체를 의미함.
- 자바에서는 하나의 클래스로부터 여러 개의 인스턴스를 생성할 수 있음.

## 3월 27일 (4주차)

### 배운 내용

- **식별자**: 코드 내의 변수, 함수, 속성을 식별하는 문자열. 대소문자 구별, 유니코드 글자, $, _, 숫자(0-9)로 구성되지만 숫자로 시작할 수 없음.
- **참조형**: 기본 자료형을 기초로 하여 만들어진 자료형. 자바에서 제공하는 String, Array, Map, Set 등이 포함됨.
- **Object**: 모든 Class와 Enum은 Object 클래스를 상속. Interface는 Object를 상속하지 않음.
- **String**: 기본 자료형이 아닌 char의 배열로 구현된 참조 자료형. 문자열에 유용한 메서드를 제공.

### 코드 예시
```java
public class Bar {
    public static void main(String[] args) {
        final double PI = 3.14;
        double radius = 10.2;
        double circleArea = radius * radius * PI; // 원의 면적 계산
        // 원의 면적을 화면에 출력
        System.out.print("반지름 " + radius + ", ");
        System.out.println("원의 면적 = " + circleArea);
    }
}
  ㅇ 비트 단위 논리 연산자 
     -  ~  :  (비트 단위 부정)
     -  &  :  (비트 단위 논리곱)
     -  |  :  (비트 단위 논리합)
     -  ^  :  (비트 단위 XOR)

     * 例) 반가산기  :  합(sum) = (a ^ b), 캐리(carry) = (a & b)

     * [C언어] 단순 비트 처리를 위한 자료형으로, 통상 unsigned char (1 바이트)을 많이 사용


  ㅇ 비트 간의 시프트 연산자
     - (비트) << (이동 수)  :  (좌로 1 비트 이동, left shift)
     - (비트) >> (이동 수)  :  (우로 1 비트 이동, right shift)

     * 비트 시프트는, 2의 거듭제곱 연산시 매우 효율적임
        . 좌로 시프트(left shift)는 2의 거듭제곱으로 곱하기
           .. 1 << 1  =>  1 x 21 = 2  :  (0001)  =>  (0010) 
           .. 2 << 1  =>  2 x 21 = 4  :  (0010)  =>  (0100)
           .. 3 << 2  =>  3 x 22 = 12  :  (0011)  =>  (1100)
        . 우로 시프트(right shift)는 2의 거듭제곱으로 나누기
           .. 12 >> 2  =>  12 ÷ 22 = 3  :  (1100)  =>  (0011)
        . 결국, 2의 거듭제곱을 계산할 때, 
           .. 상수 시간(시간복잡도 : O(1))에 수행되므로, 곱셈,나눗셈에 비해 매우 빠르게 됨 
 

  ㅇ (기타) (zero-fill right shift) (자바,자바스크립트 등)
     - (비트) >>> (이동 수)  :  (우로 이동시키고, 좌의 빈 자리를 0으로 채움)

     * 例) 8 >>> 2  =>  (1000) -> (0010)


## 3월 20일(3주차)
*배운내용
##자바 서치를 이용해 파일을 찾아낼수 있다
-프로젝트디렉토리에서 프로젝트 안에 프로젝트가 들어갈 수 있다 하지만 그러면 파일이 꼬인다
-워킹 디렉토리안에 여러개가 들어갈수 있다. 
-프로젝트 이름을 입력할게 할 수 있다
-자바 컴파일러는 자바 프로그래밍 언어로 작성된 소스 코드를 바이트 코드로 변환하는 프로그램입니다. 자바는 플랫폼 독립적인 언어이므로, 컴파일된 바이트 코드는 여러 운영 체제와 하드웨어에서 실행할 수 있습니다. 이를 통해 자바는 **"Write Once, Run Anywhere"**라는 슬로건을 가지고 있습니다.
##자바 개요 (Java Overview)
-자바(Java)는 객체 지향 프로그래밍(OOP) 언어로, 1995년에 **썬 마이크로시스템즈(Sun Microsystems)**에서 개발되었습니다. 현재는 **오라클(Oracle)**이 자바의 관리와 발전을 담당하고 있습니다. 자바는 강력한 기능과 안정성으로 인해 다양한 응용 프로그램, 웹 애플리케이션, 모바일 앱 등에서 널리 사 
 용 됩니다.
-플랫폼 독립성 (Platform Independence): 자바는 "Write Once, Run Anywhere"라는 철학을 가지고 있습니다. 즉, 자바로 작성된 프로그램은 한 번 컴파일하면, 모든 운영 체제에서 실행 가능합니다. 이는 자바 컴파일러가 바이트 코드로 변환하기 때문인데, 이 바이트 코드는 JVM에서 실행되므로 다양한 플랫 
 폼  에서 호환됩니다.

## 3월 19일(3주차)
#### READ.md 파일 편집
* 이름 학번h1 제일 위에 기제
* 날짜(주차)
* 배운내용 & 코드
* 최근 날짜가 제일 위로 올라오게.
## 이찬솔 202103323
2025.03.18
## 문법 연습

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Your branch is up to date with 'origin/main'.
#
# Changes to be committed:
#	modified:   README.md
#
