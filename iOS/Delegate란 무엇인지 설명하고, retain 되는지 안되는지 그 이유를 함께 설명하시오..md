delegate란 객체 지향 프로그래밍에서 하나의 객체가 모든 일을 처리하는 것이 아니라 처리해야 할 일 중 일부를 다른 객체에게 넘기는 것을 의미한다.

retain(유지하다) : 메모리가 해제되지 않아서 낭비되는 현상을 의미 (Memory Leak, 메모리 누수)
Delegate는 객체 간의 작업이여서 참조 값을 사용하기 때문에 retain 현상이 일어난다.

## 해결 방법
weak : 약한 참조
unowned : 약한 참조이고 해제된 메모리 영역에 재접근하지 않는다는 확신이 있을 때


Delegate(델리게이트)는 객체 지향 프로그래밍에서 하나의 객체가 다른 객체의 대리자로 동작하는 디자인 패턴 중 하나입니다. iOS에서 Delegate는 주로 프로토콜을 통해 정의되며, 한 객체가 다른 객체에게 특정 이벤트나 동작에 대한 처리를 위임할 수 있도록 합니다.

Delegate는 일반적으로 다음과 같은 상황에서 사용됩니다:

1. **이벤트 처리**: 한 객체에서 발생한 이벤트를 다른 객체에게 알리고, 그 객체가 필요한 동작을 수행하도록 함.
  
2. **커스텀 동작**: 객체 간에 특정 동작을 위임하고자 할 때, 예를 들어 특정 메소드를 호출하거나 값을 반환받을 때.

Delegate는 프로토콜을 통해 정의되며, 해당 프로토콜을 채택한 객체는 델리게이트 역할을 수행할 수 있습니다.

Retain은 iOS에서 사용되는 메모리 관리 기법 중 하나로, 객체가 메모리에서 해제되지 않도록 유지하는 것을 의미합니다. Delegate에 대한 retain 여부는 일반적으로 strong(또는 retain)으로 선언됩니다.

**예시:**

```swift
protocol MyDelegate: class {
    func didReceiveData(data: Any)
}

class MyObject {
    weak var delegate: MyDelegate?
}

// 사용 예시
let myObject = MyObject()
let viewController = MyViewController()

myObject.delegate = viewController
```

위의 예시에서 `MyObject`는 `MyDelegate` 프로토콜을 따르는 델리게이트를 가지고 있습니다. `delegate` 속성은 `weak`로 선언되어 있어서 강한 순환 참조를 방지하기 위해 델리게이트 객체에 대한 강한 참조를 유지하지 않습니다.

Retain을 사용하지 않는 이유는 일반적으로 델리게이트를 강한 참조로 유지하게 되면 순환 참조가 발생할 수 있기 때문입니다. 즉, 객체 A가 델리게이트 객체 B를 강한 참조로 가지고 있고, 객체 B가 다시 객체 A를 참조하는 경우 두 객체 간의 강한 순환 참조가 발생할 수 있습니다. 이는 메모리 누수를 초래할 수 있으므로, 대부분의 경우에는 `weak`를 사용하여 순환 참조를 방지합니다.

[목록](../README_link.md#ios)
