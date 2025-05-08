# 📘 이찬솔 (202103323)

---

## ✅ 10주차 (5월 8일)

## 🧩 추상 클래스

### 🔹 추상 메서드 (abstract method)
- `abstract` 키워드로 선언된 메서드  
- **메서드의 구현 없이 선언만 존재함**
- ✅ 예시:
  ```java
  abstract public String getName(); // 추상 메서드

  abstract public String fail() { return "Good Bye"; } // 추상 메서드 아님. 컴파일 오류

abstract class Shape {
    public Shape() { ... }
    public void edit() { ... }
    abstract public void draw(); // 추상 메서드
}
class Fault { 
    // 오류: 추상 메서드를 가지고 있으므로 abstract로 선언되어야 함
    abstract public void f(); 
}

## 자바의 패키지와 모듈이란?

---

### ● 패키지(package)
- 서로 관련된 클래스와 인터페이스를 컴파일한 **클래스 파일들을 묶어 놓은 디렉터리**
- 하나의 응용프로그램은 **한 개 이상의 패키지로 작성**
- 패키지는 **`.jar` 파일로 압축**할 수 있음

---

### ● 모듈(module)
- 여러 **패키지와 이미지 등의 자원**을 모아 놓은 **컨테이너**
- 하나의 모듈을 하나의 **`.jmod` 파일에 저장**

---

### ● Java 9부터 모듈화 도입
- **플랫폼의 모듈화**  
  : Java 9부터 자바 API의 모든 클래스들(자바 실행 환경)을 패키지 기반에서 모듈들로 완전히 재구성

- **응용프로그램의 모듈화**  
  : 클래스들은 패키지로 만들고, 다시 패키지를 모듈로 만듦  
  → 모듈 프로그래밍은 어렵고 복잡. **기존 방식으로 프로그램 작성**
