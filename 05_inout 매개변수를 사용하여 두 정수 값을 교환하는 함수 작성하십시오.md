## inout 매개변수를 사용하여 두 정수 값을 교환하는 함수 만들기

```swift
func swapNumbers(a: inout Int, b: inout Int) {
    let temp = a
    a = b
    b = temp

    print("a = \(a), b = \(b)")
}

// inout 파라미터로 구현한 함수는 반드시 변수를 전달해야 한다.
var num1 = 1
var num2 = 4
swapNumbers(a: &num1, b: &num2)
```