# 📘 이찬솔 (202103323)

---

## ✅ 12주차 (5월 22일)

## ✅ Java에서 난수 생성 방법 요약

### 📌 1. `Math` 클래스의 `random()` 메서드 사용

- `Math.random()`은 **0.0 이상 1.0 미만**의 실수형 난수를 생성합니다.
- 예시: `1~100` 사이의 정수 난수를 10개 생성

```java
for(int x = 0; x < 10; x++) {
    int n = (int)(Math.random() * 100 + 1); // 1부터 100까지의 정수
    System.out.println(n);
}

Random r = new Random();
int n = r.nextInt();       // 전체 정수 범위에서 랜덤
int m = r.nextInt(100);    // 0 이상 100 미만의 정수 (즉, 0~99)

🔁 Math와 Random의 차이점 비교
항목	Math.random()	Random 클래스
리턴 타입	double	다양한 타입 가능 (int, boolean 등)
사용 방식	static 메서드 호출	객체 생성 후 메서드 호출
범위 조절	직접 계산 필요	파라미터로 간편 지정 가능
