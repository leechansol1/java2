# 📘 이찬솔 (202103323)

---

## ✅ 11주차 (5월 15일)

📘 Java Wrapper 클래스 활용 및 박싱/언박싱 정리
✅ 예제 6-5 : Wrapper 클래스 활용
java
복사
편집
// Character 사용
System.out.println(Character.toLowerCase('A')); // 'A'를 소문자로 변환
char c1 = '4', c2 = 'F';
if (Character.isDigit(c1))                     // c1이 숫자면 true
    System.out.println(c1 + "는 숫자");
if (Character.isAlphabetic(c2))                // c2가 영문자면 true
    System.out.println(c2 + "는 영문자");

// Integer 사용
System.out.println(Integer.parseInt("28"));        // 문자열 "28" → 정수
System.out.println(Integer.toString(28));          // 정수 → 문자열
System.out.println(Integer.toBinaryString(28));    // 2진수 문자열로 변환
System.out.println(Integer.bitCount(28));          // 2진수에서 1의 개수
Integer i = Integer.valueOf("28");                 
System.out.println(i.doubleValue());               // 정수 → double 변환

// Double 사용
Double d = Double.valueOf("3.14");
System.out.println(d.toString());                  // double → 문자열
System.out.println(Double.parseDouble("3.14"));    // 문자열 → 실수

// Boolean 사용
boolean b = (4 > 3);                                // true
System.out.println(Boolean.toString(b));           // boolean → 문자열
System.out.println(Boolean.parseBoolean("false")); // 문자열 → boolean
📌 출력 결과
nginx
복사
편집
a
4는 숫자
F는 영문자
28
28
11100
3
28.0
3.14
3.14
true
false
💬 개념 설명
Wrapper 클래스는 기본 자료형을 객체처럼 다룰 수 있게 해주는 클래스입니다.

Character, Integer, Double, Boolean 등이 이에 해당합니다.

각 클래스는 문자열 변환, 타입 검사 등 유용한 메서드를 제공합니다.

✅ 박싱(Boxing)과 언박싱(Unboxing)
java
복사
편집
// 명시적 박싱
Integer ten = Integer.valueOf(10); // int → Integer

// 명시적 언박싱
int n = ten.intValue(); // Integer → int

// 자동 박싱 (JDK 1.5 이상)
Integer ten = 10; // 내부적으로 Integer.valueOf(10) 처리

// 자동 언박싱
int n = ten; // 내부적으로 ten.intValue() 처리
💬 개념 설명
박싱(Boxing): 기본 타입(int 등)을 **Wrapper 객체(Integer 등)**로 감싸는 것

언박싱(Unboxing): Wrapper 객체에서 기본 값을 꺼내는 것

자동 박싱/언박싱은 JDK 1.5부터 자동 처리되어 코드가 간결해집니다.

📌 시각적 요약
scss
복사
편집
[10]  → Integer.valueOf(10) → [Integer 객체]
[Integer 객체] → intValue() → [10]
