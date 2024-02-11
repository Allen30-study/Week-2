## 가드문으로 옵셔널 문자열을 안전하게 래핑 해제하는 함수 만들기
```swift
func doGuard(word str: String?) -> String {
    guard let unwrapping = str else {
        print("this is nil")
        return "nil"
    }
    
    return unwrapping
}
```