# 202103323 이찬솔
## 3월 27일(4주차)
* 배운내용
식별자는 코드 내의 변수, 함수, 혹은 속성을 식별하는 문자열입니다.
JavaScript에서, 식별자는 대소문자를 구별하며 유니코드 글자, $, _, 숫자(0-9)로 구성할 수 있지만, 숫자로 시작할 수는 없습니다.

참조형은 기본 자료형을 기초로 하여 만들어진 자료형이다. 대표적으로 자바에서 제공하는 String, Array, Map, Set 등과 같은 클래스(Class)와 인터페이스(Interface), 열거형(Enum)이 여기에 해당한다. 추가적으로 필요에 따라 사용자가 참조형 타입을 정의할 수도 있다.

Object
모든 Class와 Enum은 Object 클래스를 상속한다. 다시말해 Object는 모든 Class와 Enum의 일반화된 타입이라는 것이다. 여기서 주의할 점은 Interface는 Object를 상속하지 않는다는 사실이다. 이와 관련된 내용은 자바 api 문서 Tree에 잘 드러나 있다.

자바 api 문서에는 제공하는 모든 Class, Interface, Enum 등의 상세 스펙을 정의하고 있다. 이 사이트는 자바를 깊이 이해하는데 많은 도움을 주므로 자주 방문하면 좋다. 다만 자바 버전에 따라 api구현이 상이하므로 주의해야 한다.

String
String은 기본 자료형이 아니라는 사실은 익히 잘 알려져 있다. String은 char의 배열로 구현된 참조 자료형이다.

C/C++의 경우는 문자열을 사용하기 위해서 실제로 char형의 배열을 직접 사용한다.

자바가 C/C++과 달리 String형을 따로 제공하는 이유는 문자열에 유용한 메서드를 제공하기 위해서이다. charAt, concat, equals, indexOf, split와 같은 메서드를 이용하면 문자열을 쉽게 조작할 수 있다.

식별자는 코드의 일부이지만 문자열은 데이터이기 때문에, 식별자와 문자열은 다릅니다. JavaScript에서 식별자를 문자열로 변환하는 방법은 없지만, 어떤 경우 문자열을 분석해 식별자로 사용할 수 있습니다.

public class Bar {
    Run|Debug
  public static void main(String[]args) {
    final double PI = 3.14;
    double radius = 10.2;
    double circleArea = radius*radius*PI; // 원의 면적 계산
    // 원의 면적을 화면에 출력한다
    System.out.print("반지름" + radius+", ");
    System.out.println("원의 면적 = " + circleArea");
  }
}
## 3월 20일(3주차)
*배운내용 자바 서치를 이용해 파일을 찾아낼수 있다
프로젝트디렉토리에서 프로젝트 안에 프로젝트가 들어갈 수 있다 하지만 그러면 파일이 꼬인다
워킹 디렉토리안에 여러개가 들어갈수 있다. 
프로젝트 이름을 입력할게 할 수 있다
  자바 컴파일러는 자바 프로그래밍 언어로 작성된 소스 코드를 바이트 코드로 변환하는 프로그램입니다. 자바는 플랫폼 독립적인 언어이므로, 컴파일된 바이트 코드는 여러 운영 체제와 하드웨어에서 실행할 수 있습니다. 이를 통해 자바는 **"Write Once, Run Anywhere"**라는 슬로건을 가지고 있습니다.
  자바 개요 (Java Overview)
자바(Java)는 객체 지향 프로그래밍(OOP) 언어로, 1995년에 **썬 마이크로시스템즈(Sun Microsystems)**에서 개발되었습니다. 현재는 **오라클(Oracle)**이 자바의 관리와 발전을 담당하고 있습니다. 자바는 강력한 기능과 안정성으로 인해 다양한 응용 프로그램, 웹 애플리케이션, 모바일 앱 등에서 널리 사용됩니다.
플랫폼 독립성 (Platform Independence): 자바는 "Write Once, Run Anywhere"라는 철학을 가지고 있습니다. 즉, 자바로 작성된 프로그램은 한 번 컴파일하면, 모든 운영 체제에서 실행 가능합니다. 이는 자바 컴파일러가 바이트 코드로 변환하기 때문인데, 이 바이트 코드는 JVM에서 실행되므로 다양한 플랫폼에서 호환됩니다.
## 3월 19일(3주차)
#### READ.md 파일 편집
* 이름 학번h1 제일 위에 기제
* 날짜(주차)
* 배운내용 & 코드
* 최근 날짜가 제일 위로 올라오게.
## 이찬솔 202103323
2025.03.18
ㅈㄷㅂㄷㅈㅂㄷ

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# Your branch is up to date with 'origin/main'.
#
# Changes to be committed:
#	modified:   README.md
#
