Swift에서의 참조 방식은 주로 두 가지로 나뉩니다: 강한 참조(Strong Reference)와 약한 참조(Weak Reference). 이 두 참조 방식은 객체 간의 참조 관계와 메모리 관리에 영향을 미칩니다.

### 1. 강한 참조 (Strong Reference):
- **기본 참조 방식:** Swift에서의 참조는 기본적으로 강한 참조입니다.
- **특징:** 한 객체가 다른 객체를 강하게 참조하면, 참조된 객체는 참조를 유지하는 한 메모리에서 해제되지 않습니다.
- **사용:** 대부분의 경우에 적합하며, 참조 카운트가 증가하여 객체가 참조되는 동안 메모리에서 유지됩니다.

```swift
class Person {
    var name: String
    init(name: String) {
        self.name = name
    }
}

var person1: Person? = Person(name: "Alice")
var person2: Person? = person1

// person1과 person2가 동일한 객체를 강한 참조
```

### 2. 약한 참조 (Weak Reference):
- **특징:** 약한 참조는 참조된 객체의 참조 카운트를 증가시키지 않습니다. 객체가 참조를 유지하는 동안 메모리에서 해제될 수 있습니다.
- **활용:** 순환 참조를 방지하거나, 참조 대상이 메모리에서 해제될 수 있는 경우에 사용됩니다.
- **사용:** `weak` 키워드를 사용하여 선언합니다.

```swift
class Apartment {
    var unit: String
    weak var tenant: Person?
    
    init(unit: String) {
        self.unit = unit
    }
}

var apartment: Apartment? = Apartment(unit: "2A")
var person: Person? = Person(name: "Bob")

apartment?.tenant = person  // 약한 참조로 설정
person = nil  // Person 객체가 메모리에서 해제되면, apartment의 tenant는 자동으로 nil이 됨
```

약한 참조를 사용하면 객체 간의 강한 참조 순환을 방지할 수 있으며, 순환 참조로 인한 메모리 누수를 피할 수 있습니다.



**Strong 참조와 weak 참조의 차이점**

Strong 참조와 weak 참조의 차이점은 다음과 같습니다.

| 특징 | Strong 참조 | Weak 참조 |
|---|---|---|
| 인스턴스의 참조 수를 증가시킬지 여부 | 증가 | 증가하지 않음 |
| 인스턴스가 메모리에서 해제되는 시점 | 참조 수가 0이 되면 해제됨 | 참조 수가 0이 되더라도 해제되지 않음 |
| 사용 용도 | 인스턴스를 소유하고 싶거나, 인스턴스의 메서드나 프로퍼티에 액세스해야 하는 경우 | 인스턴스를 소유하지 않고 참조만 하고 싶거나, 순환 참조를 방지하려는 경우 |

**Strong 참조와 weak 참조의 사용 예**

Strong 참조는 다음과 같은 경우에 사용합니다.

* 인스턴스를 소유하고 싶다면, 즉 인스턴스를 생성하고 메모리에서 해제하는 책임을 진다면 strong 참조를 사용합니다.
* 인스턴스의 메서드나 프로퍼티에 액세스해야 한다면, 즉 인스턴스의 상태를 변경하거나 인스턴스의 메서드를 호출해야 한다면 strong 참조를 사용합니다.

Weak 참조는 다음과 같은 경우에 사용합니다.

* 인스턴스를 소유하지 않고 참조만 하고 싶다면, 즉 인스턴스의 메모리 관리에 책임을 지지 않는다면 weak 참조를 사용합니다.
* 순환 참조를 방지하려면, 즉 두 개 이상의 인스턴스가 서로를 참조하여 메모리 누수가 발생하는 것을 방지하려면 weak 참조를 사용합니다.

[목록](../README_link.md)