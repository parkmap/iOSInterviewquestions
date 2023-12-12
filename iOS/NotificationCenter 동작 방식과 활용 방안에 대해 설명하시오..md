"NotificationCenter"는 iOS 및 macOS 운영 체제에서 사용되는 중앙 집중식 이벤트 및 메시지 전송 시스템입니다. NotificationCenter를 사용하면 앱 내에서 이벤트가 발생할 때 다른 부분에 알리고, 이에 대한 반응을 취할 수 있습니다. NotificationCenter의 주요 동작 방식과 활용 방안은 다음과 같습니다:

### NotificationCenter 동작 방식:

1. **등록 및 발송 (Posting):**
   - 특정 이벤트가 발생하면 해당 이벤트를 NotificationCenter에 등록된 옵저버들에게 알리는 것을 "발송"이라고 합니다.
   - 이벤트는 "Notification"이라는 객체로 표현되며, 고유한 식별자(이벤트 이름)와 함께 발송됩니다.

2. **옵저버 등록 및 해제:**
   - 옵저버(Observer)는 특정 이벤트에 대한 관심을 표명한 객체입니다.
   - 옵저버는 NotificationCenter에 등록되고, 특정 이벤트가 발생하면 알림을 받을 수 있습니다.
   - 등록된 옵저버는 필요에 따라 해제할 수 있습니다.

3. **센터 (Center):**
   - NotificationCenter는 이벤트를 관리하고, 등록된 옵저버에게 이벤트를 전달하는 중앙 집중식 시스템입니다.
   - 각 이벤트에 대해 유일한 식별자를 사용하여 구분합니다.

### NotificationCenter 활용 방안:

1. **통신 및 데이터 전달:**
   - 다른 부분 간에 데이터를 전달할 필요가 있을 때 NotificationCenter를 사용하여 간단하게 정보를 전송할 수 있습니다.
   - 예를 들어, 사용자가 로그인하면 로그인 상태를 알리는 이벤트를 발송하고, 다른 부분에서는 이를 감지하여 UI를 갱신할 수 있습니다.

2. **모듈 간 통합:**
   - 앱이 여러 모듈로 나뉘어져 있을 때, 각 모듈 간에 상태 변경을 알리고 통합하기 위해 NotificationCenter를 사용할 수 있습니다.
   - 예를 들어, 주문이 완료되면 주문 처리 모듈이 이를 NotificationCenter를 통해 알리고, 결제 모듈에서는 이를 감지하여 결제 완료 화면을 표시할 수 있습니다.

3. **UI 갱신:**
   - 모델의 상태가 변경될 때 NotificationCenter를 사용하여 UI를 업데이트할 수 있습니다.
   - 예를 들어, 데이터가 로드되면 데이터 로드 완료를 알리고, UI에서는 이를 감지하여 화면을 갱신합니다.

4. **이벤트 기반 프로그래밍:**
   - NotificationCenter를 사용하면 이벤트 기반 프로그래밍을 쉽게 구현할 수 있습니다.
   - 특정 상황이나 사용자 동작에 대한 이벤트를 정의하고, 해당 이벤트에 대한 옵저버를 등록하여 이벤트에 대한 행동을 정의할 수 있습니다.

NotificationCenter는 느슨한 결합(Loose Coupling)을 제공하며, 앱의 유연성과 확장성을 향상시키는 데 도움을 줍니다.



아래는 Swift 언어를 사용한 간단한 NotificationCenter의 예제 코드

```swift
import Foundation

// NotificationCenter에 등록할 클래스
class UserManager {
    static let shared = UserManager()
    
    // 사용자 로그인 상태를 나타내는 변수
    var isLoggedIn: Bool = false {
        didSet {
            // 사용자 로그인 상태가 변경되면 "UserLoggedIn" 이벤트를 발송
            NotificationCenter.default.post(name: Notification.Name("UserLoggedIn"), object: nil)
        }
    }
}

// 로그인 상태 변경을 감지하는 클래스
class UIController {
    init() {
        // NotificationCenter에 "UserLoggedIn" 이벤트에 대한 옵저버 등록
        NotificationCenter.default.addObserver(self, selector: #selector(handleUserLoggedIn), name: Notification.Name("UserLoggedIn"), object: nil)
    }
    
    // "UserLoggedIn" 이벤트가 발생했을 때 호출되는 메서드
    @objc func handleUserLoggedIn() {
        if UserManager.shared.isLoggedIn {
            print("UI를 업데이트합니다. 사용자가 로그인했습니다.")
        } else {
            print("UI를 업데이트합니다. 사용자가 로그아웃했습니다.")
        }
    }
}

// 테스트
let userManager = UserManager.shared
let uiController = UIController()

// 사용자 로그인 상태 변경
userManager.isLoggedIn = true
userManager.isLoggedIn = false
```



[목록](../README_link.md#ios)
