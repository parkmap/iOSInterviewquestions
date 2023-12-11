`@main`은 Swift 5.3 버전 이후 도입된 어노테이션으로, 앱의 진입점을 나타내는 역할을 합니다. `@main` 어노테이션은 특정 타입을 나타내는 엔트리 포인트로 지정하면 해당 타입의 `main()` 함수가 앱의 시작점으로 사용됩니다.

예를 들어, iOS 앱에서는 `@main` 어노테이션을 사용하여 `UIApplicationMain` 함수를 호출하는 것이 일반적입니다. 다음은 iOS 앱의 진입점을 설정하는 예제입니다:

```swift
import UIKit

@main
class AppDelegate: UIResponder, UIApplicationDelegate {
    // AppDelegate의 내용은 여기에 작성됩니다.
}

// 나머지 앱 코드는 필요에 따라 추가됩니다.
```

위 코드에서 `@main` 어노테이션은 `main.swift` 파일이나 `@UIApplicationMain` 어노테이션 없이도 `AppDelegate` 클래스의 `main()` 함수를 앱의 진입점으로 사용하도록 합니다. `@UIApplicationMain` 대신에 Swift 5.3 이상에서는 `@main`을 사용하는 추세가 높아졌습니다.

주의: `@main`은 Swift 패키지 매니페스트에서 사용되는 것과는 다른 맥락에서 사용됩니다. Swift 패키지의 경우 `@main`은 진입점을 정의하는 데 사용됩니다.

## 참고
1. [@main: Type-Based Program Entry Points](https://github.com/apple/swift-evolution/blob/main/proposals/0281-main-attribute.md)

[목록](../README_link.md)
