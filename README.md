# 📘 이찬솔 (202103323)

---

## ✅ 13주차 (5월 29일)

### 🌟 JFrame이란?
JFrame은 Java Swing 라이브러리에서 제공하는 클래스로, 기본 윈도우 창을 생성할 때 사용됩니다. Java GUI 애플리케이션의 시작점이라고 볼 수 있습니다.

java
복사
편집
import javax.swing.JFrame;

public class MyWindow {
    public static void main(String[] args) {
        JFrame frame = new JFrame("나의 첫 창");
        frame.setSize(400, 300);             // 창 크기 설정
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  // 닫기 버튼 동작 설정
        frame.setVisible(true);              // 창을 화면에 표시
    }
}
✅ 주요 메서드 요약
메서드	설명
setTitle(String title)	창의 제목 설정
setSize(int width, int height)	창의 가로, 세로 크기 설정
setVisible(boolean b)	창을 보이게 할지 여부 설정
setDefaultCloseOperation(int operation)	창 닫을 때의 동작 설정
add(Component comp)	창에 컴포넌트 추가

💡 참고 사항
JFrame은 AWT의 Frame을 확장한 클래스입니다.

Swing 컴포넌트는 기본적으로 더블 버퍼링(Double Buffering) 처리가 되어 있어 깜빡임이 적습니다.

레이아웃 매니저를 설정해 컴포넌트 배치 방식을 조정할 수 있습니다.
