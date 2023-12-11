iOS 앱이 시작할 때 `main.c` 파일에 있는 `UIApplicationMain` 함수가 호출되고, 여기서 앱의 핵심 객체가 생성됩니다. `UIApplicationMain` 함수는 앱의 핵심 객체와 앱의 실행 흐름을 관리하는 주요 객체들을 초기화하고 설정하는 역할을 합니다.

주요 생성되는 객체는 다음과 같습니다:

1. **UIApplication:**
   - 앱 객체를 나타냅니다. 앱의 전반적인 생명주기 및 상태를 관리합니다. UIApplication 객체는 앱의 초기화, 상태 변화, 백그라운드 실행, 상호 작용 등을 담당합니다.

2. **AppDelegate:**
   - `@UIApplicationMain` 어노테이션이 지정된 클래스 (일반적으로 `AppDelegate` 클래스)의 인스턴스가 생성됩니다. AppDelegate는 UIApplicationDelegate 프로토콜을 구현하는데, 앱의 상태 변화 및 이벤트에 대한 응답을 담당합니다. 예를 들어, 앱이 시작될 때, 백그라운드로 전환될 때, 종료될 때 등의 이벤트에 대한 처리가 이곳에서 이루어집니다.

3. **Main Event Loop:**
   - `UIApplicationMain` 함수는 앱의 주 이벤트 루프를 설정합니다. 이 이벤트 루프는 사용자의 입력 및 시스템 이벤트를 감지하고, 적절한 핸들러에 전달하여 앱의 동작을 제어합니다.

`main.c` 파일은 일반적으로 개발자가 직접 수정하지 않습니다. 대부분의 경우에는 `@UIApplicationMain` 어노테이션을 사용하여 `main` 함수의 진입점을 자동으로 생성하는 방식을 사용합니다. 이를 통해 개발자는 대부분의 초기화 작업을 AppDelegate에서 처리하고, 앱의 실행 흐름을 관리할 수 있습니다.

[목록](../README_link.md)
