## 옵셔널 정수(Int?)를 취하고 switch 문에서 옵셔널 패턴을 사용하여 nil인 경우와 nil이 아닌 경우를 모두 처리하는 함수를 작성하십시오.
```swift
let x: Int? = nil

// 1. switch
switch x {
case let .some(value):
    print("this has a value: \(value)")
case .none:
    print("this is nil")
}

// 2. if-let
if let value = x {
    print("this has a value: \(value)")
} else {
    print("this is nil")
}

// 3. ??
let value = x ?? 0

print("this has a value: \(value)")

// 4. guard
guard let value = x else {
    print("this is nil")
    return
}

print("this has a value: \(value)")
```