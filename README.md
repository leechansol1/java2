# 📘 이찬솔 (202103323)

---

## ✅ 14주차 (6월 5일)

# 🖱️ 마우스 리스너 달기와 `MouseEvent` 객체 활용

## ✔️ 마우스 리스너 달기

- 마우스 리스너는 컴포넌트에 다음과 같이 등록합니다:

```java
component.addMouseListener(myMouseListener);

component.addMouseMotionListener(myMouseMotionListener);
# 🖱️ 마우스 리스너 달기와 `MouseEvent` 객체 활용
java
복사
편집
component.addMouseMotionListener(myMouseMotionListener);
✔️ MouseEvent 객체 활용
마우스 포인터의 위치 (컴포넌트 내 상대 좌표)를 얻기 위한 메서드:

int getX()

int getY()

java
복사
편집
public void mousePressed(MouseEvent e) {
    int x = e.getX(); // 마우스가 눌러진 x 좌표
    int y = e.getY(); // 마우스가 눌러진 y 좌표
}
✔️ 마우스 클릭 횟수 확인
클릭 횟수를 확인하기 위한 메서드:

int getClickCount()

java
복사
편집
public void mouseClicked(MouseEvent e) {
    if (e.getClickCount() == 2) {
        // 더블클릭 처리 루틴
    }
}
