iOS의 Scene Delegate는 iOS 13부터 소개된 개념으로, 앱의 여러 화면을 나타내는 각각의 "scene"에 대한 이벤트를 처리하는 데 사용됩니다. 기본적으로 앱은 하나의 화면(하나의 scene)만을 가지고 있었지만, iPad에서의 멀티태스킹 및 여러 창 지원을 비롯한 다양한 기기 및 환경에서의 앱 다양성을 지원하기 위해 도입되었습니다.

Scene Delegate는 앱의 생명주기 이벤트를 관리하고 각각의 scene에 대한 설정 및 동작을 정의합니다. iOS 13 이상에서는 `AppDelegate`와 함께 사용되며, `AppDelegate`가 전역적인 앱 생명주기를 관리하는 반면, `Scene Delegate`는 각각의 화면(scene)에 대한 생명주기를 관리합니다.

일반적으로 `Scene Delegate`는 다음과 같은 주요 메서드를 구현합니다:

1. `scene(_:willConnectTo:options:)`: Scene이 처음 생성될 때 호출되며, 해당 scene의 초기 설정 및 화면 구성을 수행합니다.

2. `sceneDidDisconnect(_:)`: Scene이 시스템에 의해 더 이상 필요하지 않게 되면 호출됩니다. 이 메서드에서는 리소스 정리 등의 작업을 수행할 수 있습니다.

3. `sceneDidBecomeActive(_:)`: Scene이 활성화되고 사용자의 인터랙션을 수신할 수 있는 상태가 되면 호출됩니다.

4. `sceneWillResignActive(_:)`: Scene이 비활성화되기 전에 호출되며, 사용자의 인터랙션이 더 이상 받아들여지지 않을 것임을 나타냅니다.

5. `sceneDidEnterBackground(_:)`: Scene이 백그라운드로 전환되면 호출되며, 여기에서 앱이 백그라운드에서 실행될 때 수행해야 하는 작업을 처리할 수 있습니다.

6. `sceneWillEnterForeground(_:)`: Scene이 포그라운드로 전환되기 전에 호출되며, 필요한 경우 여기에서 추가 설정을 수행할 수 있습니다.

`Scene Delegate`를 통해 앱은 여러 화면에서 일어나는 이벤트를 조율하고 관리할 수 있으며, 멀티태스킹과 같은 다양한 기능을 효과적으로 구현할 수 있습니다.

[목록](../README_link.md#ios)
