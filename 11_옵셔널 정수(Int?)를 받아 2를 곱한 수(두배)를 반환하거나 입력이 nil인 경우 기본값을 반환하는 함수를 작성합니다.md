## 옵셔널 정수(Int?)를 받아 2를 곱한 수(두배)를 반환하거나 입력이 nil인 경우 기본값을 반환하는 함수를 작성합니다.
```swift
func testOpt(_ a: Int?) -> Int {
    let value = a ?? 0
    if value != 0 {
        return value * 2
    }
    return value
}
```